# 🏉 Plataforma de Rifa Beneficencia - Club Huirapuca

Plataforma web de gestión, auditoría económica y generación de talonarios imprimibles para el **Bono Contribución a beneficio del Rugby Infantil y Prejuveniles del Club Huirapuca** (Concepción, Tucumán).

---

## 🚀 Módulos del Sistema

1. **`index.html` (Portal Principal)**: Landing page con accesos directos a los módulos de auditoría y al generador de talonarios.
2. **`gestion.html` (Sistema de Gestión & Auditoría)**:
   - Sincronización automática con la base de datos `data/db.json` del repositorio en GitHub.
   - Botón **`☁️ Publicar en GitHub`** para guardar cambios directamente mediante la **API de GitHub (REST)** haciendo commits automáticos.
   - Asignación de rangos de boletos por vendedor / categoría.
   - Registro de datos del comprador y número de teléfono.
   - Control de recaudación total en tiempo real ($).
   - **Verificador de Ganador Instantáneo**: Herramienta de auditoría para corroborar al comprador, vendedor y estado de pago al momento del sorteo.
   - Exportación de padrón completo a Excel (CSV) y respaldos en formato JSON.
3. **`data/db.json` (Base de Datos)**: Archivo JSON en la raíz del repositorio donde se guarda todo el padrón de boletos y vendedores.
4. **`talonario.html` (Generador de Talonarios Imprimibles en A4)**:
   - Formato A4 listo para imprenta (4 boletos por hoja con troquel de corte).
   - Marca de agua continua de seguridad.
   - Escudo oficial en vector.

---

## ☁️ Sincronización de Base de Datos con la API de GitHub

La plataforma incluye integración nativa con la API de GitHub:
- **Lectura**: Al abrir la web en cualquier teléfono o PC, se consulta automáticamente el archivo `data/db.json` de GitHub para tener siempre los últimos datos.
- **Escritura (Commits automáticos)**: Haciendo clic en el botón **`⚙️ GitHub API`** en la web, introduces un **Token de Acceso Personal (PAT)** de tu cuenta de GitHub. Con esto, cualquier cambio que guardes y publiques enviará un `commit` directo al repositorio de GitHub actualizando la base de datos para todos los administradores.

---

## 🛠️ Guía Paso a Paso para Subir a GitHub y Activar GitHub Pages

### Paso 1: Crear un nuevo repositorio en GitHub
1. Ingresa a tu cuenta de [GitHub](https://github.com/) y haz clic en el botón **`+`** (arriba a la derecha) -> **`New repository`**.
2. Nombre del repositorio: `rifa-huirapuca`
3. Asegúrate de seleccionarlo como **Public** (Público).
4. Haz clic en **`Create repository`**.

### Paso 2: Subir los archivos al repositorio
Si tienes Git instalado en tu computadora:
```bash
git init
git add .
git commit -m "Inicializar plataforma de Rifa Club Huirapuca"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/rifa-huirapuca.git
git push -u origin main
```
*O si prefieres no usar la consola:*
En la página de tu repositorio recién creado en GitHub, haz clic en **`uploading an existing file`**, arrastra la carpeta completa con todos los archivos (`index.html`, `gestion.html`, `talonario.html`, `sello_huirapuca.jpg`, carpeta `data/`) y haz clic en **`Commit changes`**.

### Paso 3: Activar GitHub Pages (Sitio Web Gratis)
1. Dentro de tu repositorio en GitHub, ve a la pestaña **`Settings`** (Configuración).
2. En el menú de la izquierda, haz clic en **`Pages`**.
3. En la sección **Build and deployment** -> **Source**, selecciona **`Deploy from a branch`**.
4. En **Branch**, selecciona **`main`** y la carpeta **`/(root)`**, luego haz clic en **`Save`**.

En un par de minutos, GitHub te dará la URL pública de tu web:
👉 `https://TU_USUARIO.github.io/rifa-huirapuca/`

---

## 🏆 Créditos
Desarrollado para el **Club Huirapuca - Concepción, Tucumán**.
*Sorteo: 12 de Septiembre de 2026 - En VIVO por Facebook Oficial.*
