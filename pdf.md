# Respuestas rápidas

- El campo de **asesor externo** lo completas con tu nombre, firma y datos de contacto; sí, tú eres ese asesor.  
- Al hacer clic en **Exportar JSON**, obtienes un texto que luego puedes volver a cargar con el botón **Cargar JSON**.  
- Para generar un PDF bastará con usar el diálogo de impresión del navegador (Ctrl + P) o implementar un botón que dispare `window.print()` junto a estilos específicos de impresión.  

---

## 1. Validación y llenado de datos

- Marca como obligatorios los inputs de asesor externo (nombre, email, teléfono) con `required`.  
- Usa máscaras de entrada (por ejemplo [imaskjs](https://imask.js.org/)) para teléfono y formatos de fecha.  
- Automáticamente coloca la fecha de hoy en el campo “Fecha de recolección de datos” con JavaScript:  
  ```js
  document.querySelector('[name="fecha"]').value = new Date().toISOString().slice(0,10);
  ```

---

## 2. Carga y recarga de JSON

- El botón **Cargar JSON** ya te permite pegar el objeto exportado; solo valida con `try…catch` y muestra error si no es válido.  
- Puedes guardar el JSON en `localStorage` para persistencia entre sesiones:  
  ```js
  localStorage.setItem('seguimientoData', JSON.stringify(data));
  // al cargar:
  const saved = localStorage.getItem('seguimientoData');
  if (saved) cargarJSON(saved);
  ```

---

## 3. Impresión y PDF

- Añade una hoja de estilos `@media print` para ocultar botones, bordes de inputs y mostrar solo datos limpios.  
- Crea un botón de imprimir:  
  ```html
  <button type="button" onclick="window.print()">Imprimir PDF</button>
  ```  
- Para control total sobre el PDF, usa librerías como `html2pdf.js` o `jsPDF`:  
  ```js
  import html2pdf from 'html2pdf.js';
  html2pdf().from(document.body).save('seguimiento.pdf');
  ```

---

## 4. Extras para la versión final

- Logo y membrete de la universidad en el encabezado del PDF.  
- Sección de firmas digitales: permite subir imagen de la firma y colocarla junto al nombre.  
- Timestamp automático al exportar/imprimir.  
- Validaciones en frontend y, si tienes backend, también en el servidor.  
- Una vista “solo lectura” para compartir por enlace sin posibilidad de edición.  
- Opción de enviar el PDF por email directamente desde la app (usando un servicio SMTP o serverless).

---

Con todo esto tendrás un formato completísimo, imprimible y listo para entregar. ¡Ya casi está la versión profesional que te ganará esa beca!
