# 🚀 Pasos Finales para Publicar en Google Workspace Marketplace

## 📊 Estado Actual: 96% Completado

```
✅ Código funcionando              100%
✅ Documentación legal             100%
✅ GitHub Pages activo             100%
✅ Assets visuales                 100%
⏳ Google Cloud Platform            0% ← EMPEZAR AQUÍ
⏳ Video demo                       0%
⏳ Marketplace listing              0%
```

---

## 🎯 Resumen Ejecutivo

**Tiempo total restante:** 6-8 horas de trabajo
**Costo:** $5 USD (one-time registration fee)
**Tiempo de revisión Google:** 3-7 días después de enviar

---

## 📋 PASO 1: Google Cloud Platform Setup (2-3 horas)

### 1.1 Crear Proyecto GCP

1. **Ir a:** https://console.cloud.google.com/
2. **Login** con tu cuenta de Google
3. **Click en el selector de proyectos** (arriba izquierda)
4. **Click "New Project"**
5. **Configurar:**
   ```
   Project name: Calculadora Sin Formulas
   Project ID: calculadora-sin-formulas-XXXXX (se genera automático)
   Location: No organization
   ```
6. **Click "Create"**
7. **Esperar 30 segundos** a que se cree el proyecto
8. **Seleccionar el proyecto** desde el selector

---

### 1.2 Habilitar APIs Necesarias

#### API 1: Google Sheets API

1. **Ir a:** https://console.cloud.google.com/apis/library
2. **Buscar:** "Google Sheets API"
3. **Click en "Google Sheets API"**
4. **Click "Enable"**
5. **Esperar** a que se habilite (30 segundos)

#### API 2: Google Workspace Marketplace SDK

1. **Ir a:** https://console.cloud.google.com/apis/library/appsmarket-component.googleapis.com
2. **Click "Enable"**
3. **Esperar** a que se habilite

#### API 3: Google Apps Script API

1. **Ir a:** https://console.cloud.google.com/apis/library/script.googleapis.com
2. **Click "Enable"**
3. **Esperar** a que se habilite

---

### 1.3 Configurar OAuth Consent Screen

1. **Ir a:** https://console.cloud.google.com/apis/credentials/consent
2. **Seleccionar:** "External" (para usuarios públicos)
3. **Click "Create"**

#### Página 1: OAuth consent screen

```
App name: Calculadora Sin Fórmulas
User support email: [tu-email@gmail.com]
App logo: https://baletron.github.io/calculadora-sin-formulas/assets/logo-128.png

Application home page: https://baletron.github.io/calculadora-sin-formulas/
Application privacy policy link: https://baletron.github.io/calculadora-sin-formulas/privacy.html
Application terms of service link: https://baletron.github.io/calculadora-sin-formulas/terms.html

Authorized domains:
- github.io

Developer contact information:
- [tu-email@gmail.com]
```

4. **Click "Save and Continue"**

#### Página 2: Scopes

5. **Click "Add or Remove Scopes"**
6. **Buscar y seleccionar estos scopes:**
   ```
   https://www.googleapis.com/auth/spreadsheets.currentonly
   https://www.googleapis.com/auth/script.container.ui
   ```
7. **Click "Update"**
8. **Click "Save and Continue"**

#### Página 3: Test users

9. **Por ahora, skip** (Click "Save and Continue")

#### Página 4: Summary

10. **Revisar todo**
11. **Click "Back to Dashboard"**

---

### 1.4 Crear OAuth Client ID

1. **Ir a:** https://console.cloud.google.com/apis/credentials
2. **Click "Create Credentials"**
3. **Seleccionar:** "OAuth client ID"
4. **Configurar:**
   ```
   Application type: Web application
   Name: Calculadora Sin Formulas Web Client

   Authorized JavaScript origins:
   - https://script.google.com

   Authorized redirect URIs:
   - https://script.google.com/macros/d/{SCRIPT_ID}/usercallback
   (Reemplazar {SCRIPT_ID} con tu ID real de Apps Script)
   ```

#### ¿Cómo obtener tu SCRIPT_ID?

1. Abrir tu proyecto en Apps Script Editor
2. **Ir a:** Project Settings (⚙️ icono izquierda)
3. **Copiar:** Script ID
4. Ejemplo: `1a2b3c4d5e6f7g8h9i0j1k2l3m4n5o6p7q8r9s0`

5. **Click "Create"**
6. **Copiar y guardar:**
   - Client ID: `XXXXX.apps.googleusercontent.com`
   - Client Secret: `XXXXX`

---

### 1.5 Conectar Apps Script con GCP

1. **Abrir:** https://script.google.com/
2. **Abrir tu proyecto:** "Calculadora Sin Formulas"
3. **Click en:** ⚙️ Project Settings (izquierda)
4. **Scroll down** a "Google Cloud Platform (GCP) Project"
5. **Click "Change project"**
6. **Pegar:** Tu GCP Project Number (NO el ID, sino el NUMBER)

#### ¿Cómo obtener el Project Number?

1. **Ir a:** https://console.cloud.google.com/home/dashboard
2. **Ver "Project Info" card**
3. **Copiar:** Project Number (número de 12 dígitos)
4. Ejemplo: `123456789012`

7. **Click "Set Project"**
8. **Verificar** que aparezca conectado

---

### 1.6 Actualizar appsscript.json (Opcional)

Si quieres agregar el Client ID al proyecto:

```json
{
  "timeZone": "America/Bogota",
  "dependencies": {},
  "exceptionLogging": "STACKDRIVER",
  "runtimeVersion": "V8",
  "oauthScopes": [
    "https://www.googleapis.com/auth/spreadsheets.currentonly",
    "https://www.googleapis.com/auth/script.container.ui"
  ],
  "webapp": {
    "access": "MYSELF",
    "executeAs": "USER_DEPLOYING"
  },
  "addOns": {
    "common": {
      "name": "Calculadora Sin Fórmulas - Google Sheets Tools",
      "logoUrl": "https://baletron.github.io/calculadora-sin-formulas/assets/logo-128.png",
      "layoutProperties": {
        "primaryColor": "#1a73e8",
        "secondaryColor": "#667eea"
      },
      "homepageTrigger": {
        "runFunction": "abrirPanelLateral",
        "enabled": true
      },
      "universalActions": [
        {
          "label": "Abrir Calculadora Sin Fórmulas",
          "runFunction": "abrirPanelLateral"
        }
      ],
      "useLocaleFromApp": true
    },
    "sheets": {
      "homepageTrigger": {
        "runFunction": "abrirPanelLateral",
        "enabled": true
      }
    }
  }
}
```

---

## 🎥 PASO 2: Crear Video Demo (1-2 horas)

### 2.1 Preparar Grabación

**Herramientas recomendadas:**
- **Loom** (más fácil): https://www.loom.com/ - Gratis hasta 5 minutos
- **OBS Studio** (profesional): https://obsproject.com/ - Gratis y open source
- **Windows Game Bar**: `Win + G` (ya instalado en Windows)

**Configuración de grabación:**
```
Resolución: 1920x1080 (Full HD)
Frame rate: 30 FPS
Duración: 1-3 minutos (ideal: 2 minutos)
Formato: MP4
```

---

### 2.2 Guión del Video (2 minutos)

#### 0:00-0:15 | Intro (15 seg)
```
[Pantalla: Logo + Título]
"Calculadora Sin Fórmulas - 15+ herramientas para Google Sheets"
"Realiza operaciones avanzadas sin escribir una sola fórmula"
```

#### 0:15-0:45 | Herramienta 1: Calculadora de Columnas (30 seg)
```
[Mostrar Google Sheets con datos de ejemplo]
- Columna A: Productos
- Columna B: Precio
- Columna C: Cantidad

[Abrir add-on]
- Extensiones → Calculadora Sin Fórmulas
- Click en "Calculadora de Columnas"

[Configurar operación]
- Seleccionar Columna B (Precio)
- Operación: × (multiplicar)
- Seleccionar Columna C (Cantidad)
- Click "Aplicar"

[Resultado]
- Nueva columna D con Total calculado
- Sin fórmulas, valores directos
```

#### 0:45-1:15 | Herramienta 2: Laboratorio de Texto (30 seg)
```
[Cambiar a datos de texto]
- Columna A: Nombres sin formato
  "  juan pérez  "
  "MARÍA GARCÍA"
  "carlos lópez"

[Abrir Laboratorio de Texto]
- Click en "Laboratorio de Texto"
- Agregar transformación: "Trim" (quitar espacios)
- Agregar transformación: "Capitalize"
- Preview muestra resultados en tiempo real

[Aplicar]
- Click "Aplicar Transformaciones"
- Columna B aparece con nombres formateados perfectamente
```

#### 1:15-1:45 | Herramienta 3: Super Buscador (30 seg)
```
[Cambiar a datos con duplicados]
- Lista de productos con algunos repetidos

[Abrir Super Buscador]
- Click en "Super Buscador Visual"
- Modo: "Buscar Duplicados"
- Seleccionar columna
- Click "Buscar"

[Resultado]
- Duplicados resaltados en color
- Panel muestra: "5 duplicados encontrados"
- Lista de valores duplicados
```

#### 1:45-2:00 | Cierre (15 seg)
```
[Pantalla: Panel lateral con todas las herramientas]
"15+ herramientas disponibles"
"100% gratis y open source"
"Disponible en Google Workspace Marketplace"

[Texto en pantalla]
github.com/baletron/calculadora-sin-formulas
```

---

### 2.3 Tips de Grabación

**Antes de grabar:**
- ✅ Cerrar notificaciones (modo no molestar)
- ✅ Preparar datos de ejemplo
- ✅ Probar cada herramienta primero
- ✅ Usar mouse pointer visible
- ✅ Velocidad lenta y clara

**Durante la grabación:**
- 🎤 Narración clara (opcional)
- 🖱️ Movimientos lentos del mouse
- ⏸️ Pausas de 2 segundos entre acciones
- 📝 Agregar texto en pantalla después (opcional)

**Después de grabar:**
- ✂️ Editar partes lentas
- 🎵 Agregar música de fondo (opcional, royalty-free)
- 📝 Agregar subtítulos (opcional)
- 💾 Exportar en MP4, 1920x1080

---

### 2.4 Subir a YouTube

1. **Ir a:** https://studio.youtube.com/
2. **Click "Create" → "Upload videos"**
3. **Seleccionar tu video MP4**
4. **Configurar:**
   ```
   Title: Calculadora Sin Fórmulas - Google Sheets Add-on Demo

   Description:
   Calculadora Sin Fórmulas es un complemento gratuito para Google Sheets
   que te permite realizar operaciones avanzadas sin escribir fórmulas.

   ✨ Características:
   • 15+ herramientas integradas
   • Interfaz visual intuitiva
   • Sin fórmulas, resultados directos
   • 100% gratis y open source

   🔗 Links:
   • GitHub: github.com/baletron/calculadora-sin-formulas
   • Marketplace: [agregar cuando esté publicado]

   Tags: google sheets, spreadsheet, tools, add-on, productivity

   Visibility: Unlisted (o Public si quieres)
   ```
5. **Click "Next" → "Next" → "Publish"**
6. **Copiar URL del video**
   - Ejemplo: `https://www.youtube.com/watch?v=XXXXX`

---

## 📝 PASO 3: Completar Marketplace Listing (2-3 horas)

### 3.1 Pagar Developer Registration Fee

1. **Ir a:** https://workspace.google.com/marketplace/seller
2. **Click "Get started"** o "Register as a developer"
3. **Completar información:**
   ```
   Developer name: [Tu nombre o nombre de empresa]
   Email: [tu-email@gmail.com]
   ```
4. **Pagar $5 USD** (one-time fee, no recurrente)
5. **Esperar confirmación** (inmediato)

---

### 3.2 Crear Marketplace Listing

1. **Ir a:** https://console.cloud.google.com/marketplace
2. **Seleccionar tu proyecto GCP**
3. **Click "Publish" → "Overview"**
4. **Click "Create listing"**

---

### 3.3 Completar Formulario

#### Sección 1: Basic Information

```
App name: Calculadora Sin Fórmulas

Tagline (max 60 chars):
"15+ herramientas para Google Sheets sin fórmulas"

Short description (max 80 words):
Complemento gratuito para Google Sheets que permite realizar operaciones
avanzadas sin escribir fórmulas. Incluye calculadora de columnas,
transformador de texto, buscador de duplicados, suma condicional visual,
calculadora de fechas y 10+ herramientas más. Interfaz intuitiva,
resultados instantáneos, 100% open source.

Long description (max 4000 chars):
# Calculadora Sin Fórmulas

Transforma la forma en que trabajas con Google Sheets.
Calculadora Sin Fórmulas te permite realizar operaciones
complejas mediante una interfaz visual intuitiva, sin necesidad
de memorizar sintaxis de fórmulas.

## ✨ Características Principales

### 🧮 Calculadora de Columnas
Opera entre columnas visualmente: suma, resta, multiplica, divide,
potencia, módulo. Los resultados se insertan directamente como valores.

### 📝 Laboratorio de Texto
Pipeline visual de transformaciones: trim, uppercase, lowercase,
capitalize, extraer palabras, limpiar caracteres especiales.
Preview en tiempo real.

### 🔍 Super Buscador Visual
Encuentra duplicados, valores únicos, celdas vacías.
Resalta resultados con colores automáticamente.

### 📊 Suma Condicional Visual
SUMIF sin fórmulas. Configura condiciones visualmente
y obtén resultados instantáneos.

### 📅 Maestro de Fechas
Calcula diferencias entre fechas, suma días/meses/años,
extrae componentes. Sin funciones DATE() complicadas.

### Y 10+ Herramientas Más...
- Redondeo Inteligente
- Analizador Estadístico
- Combinador de Operaciones
- Importador Mágico
- Validador de Duplicados
- Y más...

## 🎯 Ideal Para

✅ Usuarios sin experiencia en fórmulas de Excel/Sheets
✅ Análisis de datos rápidos
✅ Limpieza y transformación de datos
✅ Operaciones repetitivas que requieren varias fórmulas
✅ Cualquier persona que quiera ser más productiva

## 🆓 100% Gratis y Open Source

Sin límites, sin suscripciones, sin costos ocultos.
Código fuente disponible en GitHub.

## 🔒 Privacidad

No recopilamos, almacenamos ni compartimos ningún dato.
Todos los cálculos se realizan localmente en tu navegador.
Solo requiere permisos mínimos para leer/escribir en la hoja actual.

## 📚 Soporte

Reporta bugs o solicita nuevas funcionalidades en:
github.com/baletron/calculadora-sin-formulas/issues

Category: Productivity → Spreadsheets
```

---

#### Sección 2: Graphics

**Logo:**
```
Upload: https://baletron.github.io/calculadora-sin-formulas/assets/logo-128.png
(o subir el archivo logo-128.png directamente)
```

**Screenshots (5 required):**
```
1. https://baletron.github.io/calculadora-sin-formulas/assets/screenshot-1-panel-lateral.png
2. https://baletron.github.io/calculadora-sin-formulas/assets/screenshot-2-calculadora-columnas.png
3. https://baletron.github.io/calculadora-sin-formulas/assets/screenshot-3-laboratorio-texto.png
4. https://baletron.github.io/calculadora-sin-formulas/assets/screenshot-4-buscador-visual.png
5. https://baletron.github.io/calculadora-sin-formulas/assets/screenshot-5-suma-condicional.png
```

**Promotional images:**
```
Small (440x280): https://baletron.github.io/calculadora-sin-formulas/assets/promo-440x280.png
Large (1400x560): https://baletron.github.io/calculadora-sin-formulas/assets/promo-1400x560.png
```

**Video (optional but recommended):**
```
YouTube URL: [tu URL de YouTube del paso 2]
```

---

#### Sección 3: Legal & Privacy

```
Privacy Policy URL:
https://baletron.github.io/calculadora-sin-formulas/privacy.html

Terms of Service URL:
https://baletron.github.io/calculadora-sin-formulas/terms.html

Support URL:
https://github.com/baletron/calculadora-sin-formulas/issues

Homepage URL:
https://baletron.github.io/calculadora-sin-formulas/
```

---

#### Sección 4: Pricing & Distribution

```
Pricing model: Free
Distribution: Public (available to everyone)
Regions: All regions (worldwide)
Language: Spanish (primary), English (if you want to add)
```

---

#### Sección 5: OAuth & Permissions

```
OAuth Client ID: [tu Client ID del paso 1.4]

Scopes requested:
✅ https://www.googleapis.com/auth/spreadsheets.currentonly
✅ https://www.googleapis.com/auth/script.container.ui

Justification:
"spreadsheets.currentonly: Required to read data from and write
calculated results to the active spreadsheet.

script.container.ui: Required to display the sidebar interface
with the tool selection panel and operation dialogs."
```

---

### 3.4 Enviar a Revisión

1. **Revisar todo el formulario**
2. **Click "Save as Draft"** (guardar primero)
3. **Click "Submit for Review"**
4. **Confirmar envío**

---

### 3.5 Proceso de Revisión

**Timeline:**
- Google revisa en **3-7 días hábiles**
- Pueden solicitar cambios o aclaraciones
- Una vez aprobado, se publica automáticamente

**Notificaciones:**
- Recibirás emails sobre el estado
- Revisa Google Cloud Console regularmente

**Posibles razones de rechazo:**
- Permisos OAuth excesivos (por eso usamos `.currentonly`)
- Screenshots de baja calidad
- Descripción poco clara
- Falta de Privacy Policy o Terms
- Logo que viola derechos de autor

---

## ✅ Checklist Final

### Antes de Enviar
- [ ] Proyecto GCP creado
- [ ] 3 APIs habilitadas (Sheets, Marketplace, Apps Script)
- [ ] OAuth Consent Screen configurado
- [ ] OAuth Client ID creado
- [ ] Apps Script conectado a GCP
- [ ] Video demo grabado y subido a YouTube
- [ ] Developer Registration pagada ($5 USD)
- [ ] Listing completo con todos los campos
- [ ] 5 screenshots subidos
- [ ] 2 banners promocionales subidos
- [ ] Logo subido
- [ ] Privacy Policy URL funciona
- [ ] Terms of Service URL funciona
- [ ] Support URL funciona

### Después de Enviar
- [ ] Revisar email diariamente
- [ ] Responder solicitudes de Google rápidamente
- [ ] Estar listo para hacer cambios si es necesario

---

## 🎉 ¡Publicado!

Una vez aprobado:

1. **Tu add-on aparecerá en:**
   ```
   https://workspace.google.com/marketplace/app/calculadora_sin_formulas/
   ```

2. **Los usuarios podrán:**
   - Buscarlo en Marketplace
   - Instalarlo en 1 click
   - Usarlo en cualquier hoja de cálculo

3. **Próximos pasos:**
   - Promocionar en redes sociales
   - Responder reviews de usuarios
   - Agregar nuevas funcionalidades
   - Crear versión en inglés

---

## 🆘 Troubleshooting

### "OAuth Client ID inválido"
**Solución:** Verificar que el redirect URI incluya tu SCRIPT_ID correcto

### "API not enabled"
**Solución:** Revisar que las 3 APIs estén habilitadas en GCP

### "Permission denied"
**Solución:** Verificar que el proyecto Apps Script esté conectado al proyecto GCP

### "Rechazado por permisos excesivos"
**Solución:** Ya usamos `.currentonly`, contactar soporte de Google

---

## 📞 Soporte

**Google Workspace Marketplace Support:**
https://support.google.com/googleplay/android-developer/

**Documentación oficial:**
https://developers.google.com/workspace/marketplace

**Tu repositorio:**
https://github.com/baletron/calculadora-sin-formulas

---

## 📊 Resumen de Tiempo

```
Paso 1: GCP Setup          2-3 horas
Paso 2: Video Demo         1-2 horas
Paso 3: Marketplace        2-3 horas
Revisión de Google         3-7 días
────────────────────────────────────
TOTAL DE TU TRABAJO:       6-8 horas
TOTAL HASTA PUBLICACIÓN:   7-10 días
```

---

**¡Estás a solo 6-8 horas de tener tu add-on en Google Workspace Marketplace!** 🚀

**Siguiente acción:** Ir al Paso 1.1 y crear proyecto GCP

**¡Éxito!** 🌟
