# inventario-cronologia

----

# inventario-cronologia

---------
_________


Sistema de Inventario con Control de Caducidades y Cronología de Actividades semanales (1–15)  

Este proyecto ofrece un seguimiento detallado de lotes en inventario, alertas de caducidad, búsquedas avanzadas y registro cronológico de actividades semanales. Ideal para entornos académicos y pequeñas empresas que requieran monitorear stock, fechas de caducidad y generar reportes automáticos.

---------

## Tabla de Contenidos

1. [Características Principales](#características-principales)  
2. [Tecnologías](#tecnologías)  
3. [Quick Start](#quick-start)  
4. [Estructura del Proyecto](#estructura-del-proyecto)  
5. [Uso](#uso)  
6. [Configuración Adicional](#configuración-adicional)  
7. [Roadmap / Mejoras Futuras](#roadmap--mejoras-futuras)  
8. [Contribuir](#contribuir)  
9. [Licencia](#licencia)  
10. [Contacto](#contacto)  

---

## Características Principales

- Gestión de inventario por lotes  
- Control de fechas de caducidad con alertas programadas (email, push, Slack)  
- Escaneo de códigos de barras / QR con QuaggaJS (WebRTC)  
- Búsquedas filtradas por producto, lote, precio y caducidad  
- Cronología de actividades semanales (1–15), con marcado programado/ejecutado  
- Importación de datos desde CSV/Excel y exportación a JSON, PDF, XLSX  
- Dashboard con gráficas de stock vs. caducidad (Chart.js)  
- UI responsive “mobile first” basada en SCSS modular  
- PWA: modo offline, sincronización y manifest.json  
- Autenticación basada en roles (JWT): admin, manager, usuario  
- API REST (Node.js/Express o Serverless) con SQLite o MongoDB Atlas  

---

## Tecnologías

- Frontend  
  - HTML5 semántico  
  - JavaScript (ES6+)  
  - SCSS modular  
  - Chart.js para visualización  
  - QuaggaJS para escaneo de códigos  
  - Service Worker / PWA  

- Backend (opcional)  
  - Node.js + Express  
  - Serverless (Netlify Functions / Vercel)  
  - SQLite embebido o MongoDB Atlas  
  - JWT para autenticación  

- Herramientas  
  - npm / Yarn  
  - ESLint + Prettier  
  - Jest (tests unitarios)  
  - Cypress (E2E)  
  - GitHub Actions (CI/CD)  
  - Docker (contenedores)  

---

## Quick Start

1. Clona el repositorio  
   ```bash
   git clone https://github.com/ozclef/inventario-cronologia.git
   cd inventario-cronologia
   ```

2. Instala dependencias  
   ```bash
   npm install
   ```

3. Compila SCSS (watch mode)  
   ```bash
   npm run build:css
   ```

4. Inicia servidor local  
   ```bash
   npm run serve
   ```

5. Abre `http://localhost:3000` en tu navegador  

---

## Estructura del Proyecto

```
inventario-cronologia/
├─ public/
│  ├─ index.html
│  └─ manifest.json
├─ src/
│  ├─ scss/
│  │  ├─ _variables.scss
│  │  ├─ _mixins.scss
│  │  ├─ _components.scss
│  │  └─ main.scss
│  ├─ js/
│  │  ├─ script.js
│  │  ├─ api.js
│  │  └─ utils.js
│  └─ images/
├─ data/
│  └─ plantilla.json
├─ tests/
│  ├─ unit/
│  └─ e2e/
├─ .eslintrc.js
├─ .prettierrc
├─ Dockerfile
├─ package.json
├─ README.md
└─ LICENSE
```

---

## Uso

1. **Cargar / Guardar datos**  
   - Botón **Cargar JSON**: pega tu estructura JSON y poblala en el formulario.  
   - Botón **Exportar JSON**: convierte el estado actual en JSON legible para tu repositorio.

2. **Registro Cronológico**  
   - Agrega actividades semanales con “Agregar Actividad”.  
   - Marca programación (P) y ejecución (E) por semana.

3. **Alertas de Caducidad**  
   - Configura umbral en `script.js` (por ejemplo, 7 días antes).  
   - Recibe notificaciones por email o integraciones Webhook.

4. **Escaneo de Códigos**  
   - Descomenta el método `initBarcodeScanner()` en `script.js`.  
   - Usa cámara para leer barcode/QR y ubica lote en inventario.

5. **Dashboard**  
   - Abre `dashboard.html` para ver gráficas de stock vs. caducidad.

---

## Configuración Adicional

- Variables de entorno (`.env`) para API y servicios de notificación  
- Claves SMTP o tokens de Slack/Telegram  
- Credenciales de MongoDB Atlas (si aplica)  

---

## Roadmap / Mejoras Futuras

- Integración con ERP (QuickBooks, Odoo)  
- Módulo de predicción de demanda (ML)  
- Estadísticas avanzadas en BigQuery  
- Gamificación: badges y ranking de “0 caducidades”  
- Internacionalización (i18n) con i18next  

---

## Contribuir

1. Haz fork de este repositorio  
2. Crea tu rama feature: `git checkout -b feature/tu-mejora`  
3. Commit de tus cambios: `git commit -m "feat: descripción breve"`  
4. Push a tu rama: `git push origin feature/tu-mejora`  
5. Abre un Pull Request describiendo tu mejora  

Lee el archivo [CONTRIBUTING.md](CONTRIBUTING.md) para más detalles.  

---

## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más información.  

---

## Contacto

Oscar Cruz Díaz — oscar.cruz@example.com  
Repositorio: https://github.com/ozclef/inventario-cronologia  
Proyecto Politécnica de Tlaxcala — Sistema de Gestión de la Calidad  

---

¡Gracias por tu interés! Siéntete libre de sugerir mejoras o reportar issues.


# inventario-cronologia

Sistema de Inventario con Control de Caducidades y Cronología de Actividades semanales (1–15)  

Este proyecto ofrece un seguimiento detallado de lotes en inventario, alertas de caducidad, búsquedas avanzadas y registro cronológico de actividades semanales. Ideal para entornos académicos y pequeñas empresas que requieran monitorear stock, fechas de caducidad y generar reportes automáticos.

---

## Tabla de Contenidos

1. [Características Principales](#características-principales)  
2. [Tecnologías](#tecnologías)  
3. [Quick Start](#quick-start)  
4. [Estructura del Proyecto](#estructura-del-proyecto)  
5. [Uso](#uso)  
6. [Configuración Adicional](#configuración-adicional)  
7. [Roadmap / Mejoras Futuras](#roadmap--mejoras-futuras)  
8. [Contribuir](#contribuir)  
9. [Licencia](#licencia)  
10. [Contacto](#contacto)  

---

## Características Principales

- Gestión de inventario por lotes  
- Control de fechas de caducidad con alertas programadas (email, push, Slack)  
- Escaneo de códigos de barras / QR con QuaggaJS (WebRTC)  
- Búsquedas filtradas por producto, lote, precio y caducidad  
- Cronología de actividades semanales (1–15), con marcado programado/ejecutado  
- Importación de datos desde CSV/Excel y exportación a JSON, PDF, XLSX  
- Dashboard con gráficas de stock vs. caducidad (Chart.js)  
- UI responsive “mobile first” basada en SCSS modular  
- PWA: modo offline, sincronización y manifest.json  
- Autenticación basada en roles (JWT): admin, manager, usuario  
- API REST (Node.js/Express o Serverless) con SQLite o MongoDB Atlas  

---

## Tecnologías

- Frontend  
  - HTML5 semántico  
  - JavaScript (ES6+)  
  - SCSS modular  
  - Chart.js para visualización  
  - QuaggaJS para escaneo de códigos  
  - Service Worker / PWA  

- Backend (opcional)  
  - Node.js + Express  
  - Serverless (Netlify Functions / Vercel)  
  - SQLite embebido o MongoDB Atlas  
  - JWT para autenticación  

- Herramientas  
  - npm / Yarn  
  - ESLint + Prettier  
  - Jest (tests unitarios)  
  - Cypress (E2E)  
  - GitHub Actions (CI/CD)  
  - Docker (contenedores)  

---

## Quick Start

1. Clona el repositorio  
   ```bash
   git clone https://github.com/ozclef/inventario-cronologia.git
   cd inventario-cronologia
   ```

2. Instala dependencias  
   ```bash
   npm install
   ```

3. Compila SCSS (watch mode)  
   ```bash
   npm run build:css
   ```

4. Inicia servidor local  
   ```bash
   npm run serve
   ```

5. Abre `http://localhost:3000` en tu navegador  

---

## Estructura del Proyecto

```
inventario-cronologia/
├─ public/
│  ├─ index.html
│  └─ manifest.json
├─ src/
│  ├─ scss/
│  │  ├─ _variables.scss
│  │  ├─ _mixins.scss
│  │  ├─ _components.scss
│  │  └─ main.scss
│  ├─ js/
│  │  ├─ script.js
│  │  ├─ api.js
│  │  └─ utils.js
│  └─ images/
├─ data/
│  └─ plantilla.json
├─ tests/
│  ├─ unit/
│  └─ e2e/
├─ .eslintrc.js
├─ .prettierrc
├─ Dockerfile
├─ package.json
├─ README.md
└─ LICENSE
```

---

## Uso

1. **Cargar / Guardar datos**  
   - Botón **Cargar JSON**: pega tu estructura JSON y poblala en el formulario.  
   - Botón **Exportar JSON**: convierte el estado actual en JSON legible para tu repositorio.

2. **Registro Cronológico**  
   - Agrega actividades semanales con “Agregar Actividad”.  
   - Marca programación (P) y ejecución (E) por semana.

3. **Alertas de Caducidad**  
   - Configura umbral en `script.js` (por ejemplo, 7 días antes).  
   - Recibe notificaciones por email o integraciones Webhook.

4. **Escaneo de Códigos**  
   - Descomenta el método `initBarcodeScanner()` en `script.js`.  
   - Usa cámara para leer barcode/QR y ubica lote en inventario.

5. **Dashboard**  
   - Abre `dashboard.html` para ver gráficas de stock vs. caducidad.

---

## Configuración Adicional

- Variables de entorno (`.env`) para API y servicios de notificación  
- Claves SMTP o tokens de Slack/Telegram  
- Credenciales de MongoDB Atlas (si aplica)  

---

## Roadmap / Mejoras Futuras

- Integración con ERP (QuickBooks, Odoo)  
- Módulo de predicción de demanda (ML)  
- Estadísticas avanzadas en BigQuery  
- Gamificación: badges y ranking de “0 caducidades”  
- Internacionalización (i18n) con i18next  

---

## Contribuir

1. Haz fork de este repositorio  
2. Crea tu rama feature: `git checkout -b feature/tu-mejora`  
3. Commit de tus cambios: `git commit -m "feat: descripción breve"`  
4. Push a tu rama: `git push origin feature/tu-mejora`  
5. Abre un Pull Request describiendo tu mejora  

Lee el archivo [CONTRIBUTING.md](CONTRIBUTING.md) para más detalles.  

---

## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más información.  

---

## Contacto

Oscar Cruz Díaz — oscar.cruz@example.com  
Repositorio: https://github.com/ozclef/inventario-cronologia  
Proyecto Politécnica de Tlaxcala — Sistema de Gestión de la Calidad  

---

¡Gracias por tu interés! Siéntete libre de sugerir mejoras o reportar issues.# inventario-cronologia

Sistema de Inventario con Control de Caducidades y Cronología de Actividades semanales (1–15)  

Este proyecto ofrece un seguimiento detallado de lotes en inventario, alertas de caducidad, búsquedas avanzadas y registro cronológico de actividades semanales. Ideal para entornos académicos y pequeñas empresas que requieran monitorear stock, fechas de caducidad y generar reportes automáticos.

---

## Tabla de Contenidos

1. [Características Principales](#características-principales)  
2. [Tecnologías](#tecnologías)  
3. [Quick Start](#quick-start)  
4. [Estructura del Proyecto](#estructura-del-proyecto)  
5. [Uso](#uso)  
6. [Configuración Adicional](#configuración-adicional)  
7. [Roadmap / Mejoras Futuras](#roadmap--mejoras-futuras)  
8. [Contribuir](#contribuir)  
9. [Licencia](#licencia)  
10. [Contacto](#contacto)  

---

## Características Principales

- Gestión de inventario por lotes  
- Control de fechas de caducidad con alertas programadas (email, push, Slack)  
- Escaneo de códigos de barras / QR con QuaggaJS (WebRTC)  
- Búsquedas filtradas por producto, lote, precio y caducidad  
- Cronología de actividades semanales (1–15), con marcado programado/ejecutado  
- Importación de datos desde CSV/Excel y exportación a JSON, PDF, XLSX  
- Dashboard con gráficas de stock vs. caducidad (Chart.js)  
- UI responsive “mobile first” basada en SCSS modular  
- PWA: modo offline, sincronización y manifest.json  
- Autenticación basada en roles (JWT): admin, manager, usuario  
- API REST (Node.js/Express o Serverless) con SQLite o MongoDB Atlas  

---

## Tecnologías

- Frontend  
  - HTML5 semántico  
  - JavaScript (ES6+)  
  - SCSS modular  
  - Chart.js para visualización  
  - QuaggaJS para escaneo de códigos  
  - Service Worker / PWA  

- Backend (opcional)  
  - Node.js + Express  
  - Serverless (Netlify Functions / Vercel)  
  - SQLite embebido o MongoDB Atlas  
  - JWT para autenticación  

- Herramientas  
  - npm / Yarn  
  - ESLint + Prettier  
  - Jest (tests unitarios)  
  - Cypress (E2E)  
  - GitHub Actions (CI/CD)  
  - Docker (contenedores)  

---

## Quick Start

1. Clona el repositorio  
   ```bash
   git clone https://github.com/ozclef/inventario-cronologia.git
   cd inventario-cronologia
   ```

2. Instala dependencias  
   ```bash
   npm install
   ```

3. Compila SCSS (watch mode)  
   ```bash
   npm run build:css
   ```

4. Inicia servidor local  
   ```bash
   npm run serve
   ```

5. Abre `http://localhost:3000` en tu navegador  

---

## Estructura del Proyecto

```
inventario-cronologia/
├─ public/
│  ├─ index.html
│  └─ manifest.json
├─ src/
│  ├─ scss/
│  │  ├─ _variables.scss
│  │  ├─ _mixins.scss
│  │  ├─ _components.scss
│  │  └─ main.scss
│  ├─ js/
│  │  ├─ script.js
│  │  ├─ api.js
│  │  └─ utils.js
│  └─ images/
├─ data/
│  └─ plantilla.json
├─ tests/
│  ├─ unit/
│  └─ e2e/
├─ .eslintrc.js
├─ .prettierrc
├─ Dockerfile
├─ package.json
├─ README.md
└─ LICENSE
```

---

## Uso

1. **Cargar / Guardar datos**  
   - Botón **Cargar JSON**: pega tu estructura JSON y poblala en el formulario.  
   - Botón **Exportar JSON**: convierte el estado actual en JSON legible para tu repositorio.

2. **Registro Cronológico**  
   - Agrega actividades semanales con “Agregar Actividad”.  
   - Marca programación (P) y ejecución (E) por semana.

3. **Alertas de Caducidad**  
   - Configura umbral en `script.js` (por ejemplo, 7 días antes).  
   - Recibe notificaciones por email o integraciones Webhook.

4. **Escaneo de Códigos**  
   - Descomenta el método `initBarcodeScanner()` en `script.js`.  
   - Usa cámara para leer barcode/QR y ubica lote en inventario.

5. **Dashboard**  
   - Abre `dashboard.html` para ver gráficas de stock vs. caducidad.

---

## Configuración Adicional

- Variables de entorno (`.env`) para API y servicios de notificación  
- Claves SMTP o tokens de Slack/Telegram  
- Credenciales de MongoDB Atlas (si aplica)  

---

## Roadmap / Mejoras Futuras

- Integración con ERP (QuickBooks, Odoo)  
- Módulo de predicción de demanda (ML)  
- Estadísticas avanzadas en BigQuery  
- Gamificación: badges y ranking de “0 caducidades”  
- Internacionalización (i18n) con i18next  

---

## Contribuir

1. Haz fork de este repositorio  
2. Crea tu rama feature: `git checkout -b feature/tu-mejora`  
3. Commit de tus cambios: `git commit -m "feat: descripción breve"`  
4. Push a tu rama: `git push origin feature/tu-mejora`  
5. Abre un Pull Request describiendo tu mejora  

Lee el archivo [CONTRIBUTING.md](CONTRIBUTING.md) para más detalles.  

---

## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más información.  

---

## Contacto

Oscar Cruz Díaz — oscar.cruz@example.com  
Repositorio: https://github.com/ozclef/inventario-cronologia  
Proyecto Politécnica de Tlaxcala — Sistema de Gestión de la Calidad  

---

¡Gracias por tu interés! Siéntete libre de sugerir mejoras o reportar issues.

__________
## Plantilla de Seguimiento de Estancia/Estadía en JSON, HTML, CSS y JavaScript

A continuación tienes cuatro artefactos listos para usar o adaptar:

1. **JSON**: Esquema de datos que refleja cada campo del formato.
2. **HTML**: Estructura del formulario y tabla de actividades semanales.
3. **CSS**: Estilos básicos para una presentación limpia y responsiva.
4. **JavaScript**: Lógica para cargar/guardar el JSON y manejar la tabla de actividades.

---

## 1. JSON (Esquema de Datos)

### // "E-1", "E-2" o "EST"   // ... más actividades

```json
{
  "programaAcademico": "",
  "empresa": {
    "nombre": "",
    "razonSocial": "",
    "domicilio": "",
    "telefono": "",
    "sello": ""
  },
  "asesorExterno": {
    "nombre": "",
    "puesto": "",
    "email": "",
    "telefono": ""
  },
  "asesorInterno": {
    "nombre": "",
    "firma": ""
  },
  "directorPA": {
    "nombre": "",
    "firma": ""
  },
  "datosAlumno": {
    "matricula": "",
    "nombre": "",
    "email": ""
  },
  "procesoEvaluado": "",       
  "nombreProyecto": "",
  "objetivoProyecto": "",
  "periodoRealizacion": "",
  "actividades": [
    {
      "id": 1,
      "descripcion": "",
      "semanasProgramadas": [1, 2],
      "semanasEjecutadas": [1]
    }
  
  ],
  "revisiones": {
    "asesorExterno": {
      "primerReporte": { "firma": "", "sello": "" },
      "segundoReporte": { "firma": "", "sello": "" },
      "reporteFinal":   { "firma": "", "sello": "" }
    },
    "asesorInterno": {
      "primerReporte":   { "firma": "" },
      "segundoReporte":  { "firma": "" },
      "reporteFinal":    { "firma": "" }
    }
  },
  "observaciones": ""
}
```

---

## 2. HTML

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Seguimiento de Estancia/Estadía</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <form id="formSeguimiento">
    <h1>Formato: Seguimiento de Estancia/Estadía</h1>

    <section>
      <h2>Datos Generales</h2>
      <label>Programa Académico:
        <input type="text" name="programaAcademico" />
      </label>
      <fieldset>
        <legend>Empresa</legend>
        <label>Nombre:
          <input type="text" name="empresa.nombre" />
        </label>
        <label>Razón Social:
          <input type="text" name="empresa.razonSocial" />
        </label>
        <label>Domicilio:
          <input type="text" name="empresa.domicilio" />
        </label>
        <label>Teléfono:
          <input type="tel" name="empresa.telefono" />
        </label>
      </fieldset>
      <fieldset>
        <legend>Asesor Externo</legend>
        <label>Nombre:
          <input type="text" name="asesorExterno.nombre" />
        </label>
        <label>Puesto:
          <input type="text" name="asesorExterno.puesto" />
        </label>
        <label>Email:
          <input type="email" name="asesorExterno.email" />
        </label>
        <label>Teléfono:
          <input type="tel" name="asesorExterno.telefono" />
        </label>
      </fieldset>
      <fieldset>
        <legend>Asesor Interno</legend>
        <label>Nombre:
          <input type="text" name="asesorInterno.nombre" />
        </label>
      </fieldset>
      <fieldset>
        <legend>Director del P.A.</legend>
        <label>Nombre:
          <input type="text" name="directorPA.nombre" />
        </label>
      </fieldset>
      <fieldset>
        <legend>Alumno</legend>
        <label>Matrícula:
          <input type="text" name="datosAlumno.matricula" />
        </label>
        <label>Nombre:
          <input type="text" name="datosAlumno.nombre" />
        </label>
        <label>Email:
          <input type="email" name="datosAlumno.email" />
        </label>
      </fieldset>
      <label>Proceso Evaluado:
        <select name="procesoEvaluado">
          <option value="E-1">Estancia 1 (E-1)</option>
          <option value="E-2">Estancia 2 (E-2)</option>
          <option value="EST">Estadía (EST)</option>
        </select>
      </label>
      <label>Nombre del Proyecto:
        <input type="text" name="nombreProyecto" />
      </label>
      <label>Objetivo del Proyecto:
        <textarea name="objetivoProyecto" rows="2"></textarea>
      </label>
      <label>Periodo de Realización:
        <input type="text" name="periodoRealizacion" />
      </label>
    </section>

    <section>
      <h2>Actividad Semanal</h2>
      <table id="tablaActividades">
        <thead>
          <tr>
            <th>#</th>
            <th>Descripción</th>
            <th colspan="15">Semanas 1–15</th>
          </tr>
          <tr>
            <th></th><th></th>
            <!-- generar del 1 al 15 -->
            <script>
              for(let w=1;w<=15;w++){
                document.write(`<th>${w}</th>`);
              }
            </script>
          </tr>
        </thead>
        <tbody>
          <!-- filas dinámicas desde JS -->
        </tbody>
      </table>
      <button type="button" id="btnAgregar">Agregar Actividad</button>
    </section>

    <section>
      <h2>Revisiones</h2>
      <fieldset>
        <legend>Asesor Externo</legend>
        <label>Primer Reporte - Firma:
          <input type="text" name="revisiones.asesorExterno.primerReporte.firma" />
        </label>
        <label>Sello:
          <input type="text" name="revisiones.asesorExterno.primerReporte.sello" />
        </label>
        <!-- repetir para segundo y final -->
      </fieldset>
      <fieldset>
        <legend>Asesor Interno</legend>
        <label>Primer Reporte - Firma:
          <input type="text" name="revisiones.asesorInterno.primerReporte.firma" />
        </label>
        <!-- repetir para segundo y final -->
      </fieldset>
    </section>

    <section>
      <h2>Observaciones</h2>
      <textarea name="observaciones" rows="3"></textarea>
    </section>

    <button type="button" id="btnCargar">Cargar JSON</button>
    <button type="button" id="btnGuardar">Exportar JSON</button>
  </form>

  <script src="script.js"></script>
</body>
</html>
```

---

## 3. CSS (styles.css)

```css
* {
  box-sizing: border-box;
  font-family: sans-serif;
}

body {
  padding: 1rem;
  max-width: 1000px;
  margin: auto;
}

h1, h2 {
  margin-top: 1.5rem;
  margin-bottom: 0.5rem;
}

form section {
  margin-bottom: 2rem;
  padding: 1rem;
  border: 1px solid #ddd;
  border-radius: 4px;
}

label {
  display: block;
  margin: 0.5rem 0;
}

input[type="text"],
input[type="email"],
input[type="tel"],
select,
textarea {
  width: 100%;
  padding: 0.4rem;
  margin-top: 0.2rem;
  border: 1px solid #ccc;
  border-radius: 3px;
}

table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 1rem;
}

th, td {
  border: 1px solid #bbb;
  padding: 0.4rem;
  text-align: center;
}

button {
  margin-top: 1rem;
  padding: 0.6rem 1rem;
  border: none;
  background: #0069d9;
  color: white;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background: #0053ba;
}
```

---

## 4. JavaScript (script.js)

```javascript
// Hover: manejar la tabla de actividades y JSON

let data = null;
const tblBody = document.querySelector('#tablaActividades tbody');
const btnAgregar = document.querySelector('#btnAgregar');
const btnGuardar = document.querySelector('#btnGuardar');
const btnCargar = document.querySelector('#btnCargar');

function crearFila(act) {
  const tr = document.createElement('tr');
  tr.dataset.id = act.id;
  tr.innerHTML = `
    <td>${act.id}</td>
    <td>
      <input type="text"
        value="${act.descripcion}"
        onchange="actualizarActividad(${act.id}, 'descripcion', this.value)"
      />
    </td>
    ${Array.from({ length: 15 }, (_, i) => {
      const semana = i + 1;
      const pChecked = act.semanasProgramadas.includes(semana) ? 'checked' : '';
      const eChecked = act.semanasEjecutadas.includes(semana)   ? 'checked' : '';
      return `
        <td>
          <label>P:<input type="checkbox" ${pChecked}
            onchange="toggleSemana(${act.id}, 'Programada', ${semana}, this.checked)"
          /></label>
          <label>E:<input type="checkbox" ${eChecked}
            onchange="toggleSemana(${act.id}, 'Ejecutada', ${semana}, this.checked)"
          /></label>
        </td>`;
    }).join('')}
  `;
  return tr;
}

function renderTabla() {
  tblBody.innerHTML = '';
  data.actividades.forEach(act => tblBody.appendChild(crearFila(act)));
}

btnAgregar.addEventListener('click', () => {
  const id = data.actividades.length + 1;
  data.actividades.push({
    id, descripcion: '', semanasProgramadas: [], semanasEjecutadas: []
  });
  renderTabla();
});

function actualizarActividad(id, campo, valor) {
  const act = data.actividades.find(a => a.id === id);
  act[campo] = valor;
}

function toggleSemana(id, tipo, semana, estado) {
  const act = data.actividades.find(a => a.id === id);
  const key = tipo === 'Programada' ? 'semanasProgramadas' : 'semanasEjecutadas';
  if (estado) {
    if (!act[key].includes(semana)) act[key].push(semana);
  } else {
    act[key] = act[key].filter(s => s !== semana);
  }
}

btnGuardar.addEventListener('click', () => {
  // recolectar todo el form en el objeto data
  const form = document.getElementById('formSeguimiento');
  new FormData(form).forEach((v, k) => {
    const path = k.split('.');
    let obj = data;
    for (let i = 0; i < path.length - 1; i++) {
      obj = obj[path[i]];
    }
    obj[path[path.length - 1]] = v;
  });
  const json = JSON.stringify(data, null, 2);
  console.log(json);
  alert('JSON exportado a consola');
});

btnCargar.addEventListener('click', () => {
  const texto = prompt('Pega aquí tu JSON:');
  try {
    data = JSON.parse(texto);
    // poblar inputs
    const form = document.getElementById('formSeguimiento');
    new FormData(form).forEach((_, k) => {
      const path = k.split('.');
      let obj = data;
      for (let i = 0; i < path.length - 1; i++) {
        obj = obj[path[i]];
      }
      const val = obj[path[path.length - 1]];
      const input = form.querySelector(`[name="${k}"]`);
      if (input) input.value = val || '';
    });
    renderTabla();
  } catch (e) {
    alert('JSON inválido');
  }
});

// inicio con esquema vacío
data = {
  programaAcademico: "",
  empresa: { nombre:"", razonSocial:"", domicilio:"", telefono:"", sello:"" },
  asesorExterno: { nombre:"",
