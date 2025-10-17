# 🧩 1. Qué puedes llenar tú mismo

Tú eres el alumno y diseñador del sistema, así que hay datos que tú sí puedes dejar ya completos:

Sección	Qué llenar tú	Ejemplo
Programa Académico	Tu carrera	Ingeniería en Software
Empresa	Donde hiciste la estadía (o el lugar simulado)	“OS Clef Systems” / “Prototipo de Inventario Cronología”
Asesor Externo	Si no hubo, puedes inventar un contacto realista	Nombre, Puesto, Teléfono
Asesor Interno / Director	Nombre del profe o coordinador	Ing. López G., Director del P.A.
Alumno	Tu matrícula, nombre, correo	—
Proceso Evaluado	“Estadía (EST)” si fue proyecto final	—
Proyecto / Objetivo / Periodo	Describir qué hiciste	“Desarrollo de sistema de seguimiento de prácticas con almacenamiento JSON local y exportación PDF”, etc.

________

#📅 2. Actividades y horas

Tú puedes registrar actividades reales o simuladas tipo:

Planificación del sistema

Diseño del formulario HTML y validaciones

Integración de exportación JSON y PDF

Pruebas, depuración, despliegue en GitHub Pages

__________
## 👉 Cada fila puede representar una tarea principal, y las semanas donde la hiciste las marcas con las casillas.


Ejemplo:
Actividad: “Diseño de interfaz HTML”
Semanas marcadas: 1 y 2

### 🧠 3. Qué llena el asesor externo/interno

________
Esas partes del final (“firmas”, “sello”, “reporte”) son para validación institucional.
Tú puedes dejarlas en blanco o poner “—” temporalmente, y luego el asesor puede:

Imprimir el PDF desde el botón

Escribir o firmar a mano

(O si es digital) abrir tu mismo sitio, cargar el JSON, y llenar esas secciones directamente.

💡 Si quieres, puedo hacer que cuando el asesor llene los campos, se guarden en localStorage para que no se borren al recargar.


----------
## 💾 4. Guardar en localStorage
_________

Sí 😎 se puede súper fácil.
Así, si cierras la pestaña, los datos no se pierden.

Agrega esto al final del <script> (antes de cerrar </script> en tu código):

````
// === Guardar automáticamente en localStorage ===
const form = document.getElementById('formSeguimiento');

// guardar cada vez que se cambia algo
form.addEventListener('input', () => {
  const data = formToObject(form);
  localStorage.setItem('seguimientoForm', JSON.stringify(data));
});

// al cargar la página, intentar restaurar
window.addEventListener('load', () => {
  const saved = localStorage.getItem('seguimientoForm');
  if (saved) {
    try {
      const obj = JSON.parse(saved);
      applyToForm(obj, form);
      console.log("Datos cargados desde localStorage");
    } catch(e){ console.error(e); }
  }
});
````

✨ Con eso:

Se guardará automáticamente cada vez que escribas algo.

Cuando vuelvas a entrar a la página, se llenará solito.

Puedes seguir usando “Exportar JSON” si quieres guardar una copia final.

🧾 5. Sobre el db.json

Sí, puedes reemplazar el anterior si ahora vas a trabajar con esta versión del formulario (más completa).
No borres el viejo si quieres conservarlo como respaldo, pero el actual es el “oficial”.
