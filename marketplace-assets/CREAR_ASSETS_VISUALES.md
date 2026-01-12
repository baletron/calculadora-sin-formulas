# 🎨 Guía Completa: Crear Assets Visuales

## 🎯 Objetivo
Crear todos los assets necesarios para publicar en Google Workspace Marketplace.

---

## 📋 Checklist de Assets

### Logos
- [ ] logo-128.png (128x128px, PNG transparente)
- [ ] logo-32.png (32x32px, PNG transparente)

### Screenshots
- [ ] screenshot-1.png (1280x800px) - Panel Lateral
- [ ] screenshot-2.png (1280x800px) - Calculadora de Columnas
- [ ] screenshot-3.png (1280x800px) - Laboratorio de Texto
- [ ] screenshot-4.png (1280x800px) - Super Buscador
- [ ] screenshot-5.png (1280x800px) - Suma Condicional

### Banners
- [ ] promo-440x280.png (440x280px)
- [ ] promo-1400x560.png (1400x560px)

---

## 🎨 PARTE 1: LOGOS

### Concepto del Logo

**Identidad del proyecto:**
- 🧮 Calculadora (principal)
- 📊 Hojas de cálculo (contexto)
- ⚡ Velocidad/instantáneo
- 🎯 Simplicidad (sin fórmulas)

**Colores:**
- Azul Google: `#1a73e8`
- Púrpura: `#667eea` a `#764ba2`
- Blanco: `#ffffff`

### Diseño 1: Logo Principal (RECOMENDADO)

**Descripción:**
- Calculadora estilizada con símbolo de spreadsheet
- Gradiente azul-púrpura
- Minimalista y moderno

**Crear en Canva:**

1. Ir a https://www.canva.com/
2. Crear diseño → Custom size → 512x512px
3. Agregar elementos:
   - **Fondo:** Cuadrado con bordes redondeados (radius 80px)
   - **Gradiente:** De #667eea (top-left) a #764ba2 (bottom-right)
   - **Icono central:** Calculadora + tabla (usar iconos de Canva)
   - **Color icono:** Blanco (#ffffff)
4. Exportar como PNG (fondo transparente)
5. Resize a 128x128px y 32x32px

**Alternativa: Usar código SVG**

Archivo: `logo-design.svg`

```svg
<svg width="128" height="128" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#667eea;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#764ba2;stop-opacity:1" />
    </linearGradient>
  </defs>

  <!-- Fondo redondeado con gradiente -->
  <rect width="128" height="128" rx="24" fill="url(#grad1)"/>

  <!-- Calculadora (parte superior) -->
  <rect x="28" y="28" width="72" height="36" rx="6" fill="white" opacity="0.9"/>

  <!-- Pantalla calculadora -->
  <rect x="36" y="36" width="56" height="12" rx="2" fill="#1a73e8"/>

  <!-- Botones calculadora (grid 3x2) -->
  <circle cx="44" cy="58" r="4" fill="#1a73e8"/>
  <circle cx="64" cy="58" r="4" fill="#1a73e8"/>
  <circle cx="84" cy="58" r="4" fill="#1a73e8"/>

  <!-- Tabla/Spreadsheet (parte inferior) -->
  <g opacity="0.9">
    <!-- Líneas horizontales -->
    <line x1="28" y1="76" x2="100" y2="76" stroke="white" stroke-width="2"/>
    <line x1="28" y1="88" x2="100" y2="88" stroke="white" stroke-width="2"/>
    <line x1="28" y1="100" x2="100" y2="100" stroke="white" stroke-width="2"/>

    <!-- Líneas verticales -->
    <line x1="52" y1="76" x2="52" y2="100" stroke="white" stroke-width="2"/>
    <line x1="76" y1="76" x2="76" y2="100" stroke="white" stroke-width="2"/>
  </g>

  <!-- Ícono de rayo (velocidad) - pequeño -->
  <path d="M106 22 L110 30 L106 30 L108 38 L102 30 L106 30 Z" fill="#FFD700"/>
</svg>
```

**Convertir SVG a PNG:**
1. Copiar el código SVG
2. Ir a https://svgtopng.com/
3. Pegar código
4. Descargar en 128x128 y 32x32

### Diseño 2: Logo Alternativo (Más Simple)

```svg
<svg width="128" height="128" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="grad2" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#1a73e8;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#667eea;stop-opacity:1" />
    </linearGradient>
  </defs>

  <!-- Círculo de fondo -->
  <circle cx="64" cy="64" r="60" fill="url(#grad2)"/>

  <!-- Símbolo de calculadora estilizada -->
  <text x="64" y="85" font-family="Arial, sans-serif" font-size="72" font-weight="bold"
        text-anchor="middle" fill="white">🧮</text>

  <!-- Badge "sin fórmulas" -->
  <rect x="28" y="100" width="72" height="16" rx="8" fill="white" opacity="0.9"/>
  <text x="64" y="110" font-family="Arial, sans-serif" font-size="9" font-weight="bold"
        text-anchor="middle" fill="#1a73e8">SIN FÓRMULAS</text>
</svg>
```

### Diseño 3: Logo con Iniciales

```svg
<svg width="128" height="128" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="grad3" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#667eea;stop-opacity:1" />
      <stop offset="50%" style="stop-color:#1a73e8;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#764ba2;stop-opacity:1" />
    </linearGradient>
  </defs>

  <!-- Cuadrado redondeado -->
  <rect width="128" height="128" rx="28" fill="url(#grad3)"/>

  <!-- Letras CSF (Calculadora Sin Fórmulas) -->
  <text x="64" y="80" font-family="'Roboto', sans-serif" font-size="48" font-weight="900"
        text-anchor="middle" fill="white">CSF</text>

  <!-- Subtítulo -->
  <text x="64" y="105" font-family="'Roboto', sans-serif" font-size="12"
        text-anchor="middle" fill="white" opacity="0.9">SHEETS TOOLS</text>
</svg>
```

---

## 📸 PARTE 2: SCREENSHOTS (1280x800px)

### Preparación General

1. **Abrir Google Sheets**
2. **Crear hoja con datos de ejemplo** (ver datos sugeridos abajo)
3. **Abrir tu complemento:** Extensiones → Calculadora Sin Fórmulas
4. **Configurar resolución:** Asegurar que la ventana sea 1280x800 o mayor

### Screenshot 1: Panel Lateral (PRINCIPAL)

**Objetivo:** Mostrar la lista completa de herramientas

**Pasos:**
1. Abrir el panel lateral
2. Mostrar la lista de las 15 herramientas
3. Asegurar que se vean los iconos claramente

**Captura:**
- Windows: Win + Shift + S
- Seleccionar área de 1280x800
- Asegurar que se vea:
  - Panel lateral completo (derecha)
  - Parte de la hoja (izquierda) con datos reales

**Datos de ejemplo en la hoja:**
```
| Producto    | Precio | Cantidad | Total |
|-------------|--------|----------|-------|
| Laptop      | 1200   | 5        |       |
| Mouse       | 25     | 20       |       |
| Teclado     | 75     | 10       |       |
| Monitor     | 300    | 8        |       |
| Webcam      | 50     | 15       |       |
```

**Anotaciones (opcional):**
- Flecha apuntando al panel: "15+ Herramientas"
- Círculo alrededor de una herramienta popular

### Screenshot 2: Calculadora de Columnas

**Objetivo:** Mostrar operación entre columnas con preview

**Pasos:**
1. Abrir "Calculadora de Columnas"
2. Seleccionar rango A: B2:B6 (Precio)
3. Seleccionar rango B: C2:C6 (Cantidad)
4. Operación: Multiplicar (×)
5. Nombre resultado: "Total"
6. El preview debe mostrar los resultados

**Captura:**
- Centrar en la ventana de Calculadora de Columnas
- Mostrar:
  - Inputs con rangos seleccionados
  - Operador seleccionado (×)
  - Preview con resultados calculados

**Anotar (opcional):**
- "Preview en tiempo real" apuntando a los resultados
- "Sin fórmulas necesarias"

### Screenshot 3: Laboratorio de Texto

**Objetivo:** Mostrar pipeline de transformaciones

**Datos de ejemplo:**
```
| Nombre Original      |
|---------------------|
| JUAN PÉREZ          |
|   maría garcía   |
| pedro_rodriguez     |
| ANA LÓPEZ           |
```

**Pasos:**
1. Abrir "Laboratorio de Texto"
2. Seleccionar columna con nombres
3. Agregar operaciones al pipeline:
   - Capitalizar palabras
   - Eliminar espacios extras
   - Reemplazar "_" por " "
4. Ver preview de transformación

**Captura:**
- Mostrar el pipeline completo
- Preview mostrando antes/después
- 3-4 operaciones visibles

**Anotar:**
- "Pipeline visual" apuntando a las operaciones
- "Antes → Después" en el preview

### Screenshot 4: Super Buscador Visual

**Objetivo:** Mostrar búsqueda de duplicados

**Datos de ejemplo:**
```
| ID  | Email              | Nombre      |
|-----|-------------------|-------------|
| 001 | ana@email.com     | Ana López   |
| 002 | ana@email.com     | Ana López   | ← Duplicado
| 003 | carlos@email.com  | Carlos Ruiz |
| 004 | ana@email.com     | Ana López   | ← Duplicado
| 005 | maria@email.com   | María García|
```

**Pasos:**
1. Abrir "Super Buscador Visual"
2. Seleccionar modo: "Duplicados"
3. Seleccionar columna: Email (B)
4. Ejecutar búsqueda
5. Ver resultados resaltados

**Captura:**
- Interfaz de Super Buscador
- Resultados mostrando duplicados resaltados en la hoja
- Contador: "3 duplicados encontrados"

**Anotar:**
- Círculos rojos alrededor de duplicados
- "Encontrado al instante"

### Screenshot 5: Suma Condicional Visual

**Objetivo:** Mostrar SUMIF sin fórmulas

**Datos de ejemplo:**
```
| Región | Ventas |
|--------|--------|
| Norte  | 1000   |
| Sur    | 1500   |
| Norte  | 800    |
| Este   | 1200   |
| Norte  | 600    |
| Sur    | 900    |
```

**Pasos:**
1. Abrir "Suma Condicional Visual"
2. Columna a sumar: Ventas (B)
3. Operación: Sumar
4. Condición: Región (A) = "Norte"
5. Ver resultado calculado

**Captura:**
- Interfaz con condiciones configuradas
- Preview mostrando:
  - Suma Total: 2400
  - 3 filas cumplen la condición
- Fórmula equivalente (si se muestra)

**Anotar:**
- "SUMIF visual" en el título
- Destacar el resultado grande

---

## 🎨 PARTE 3: BANNERS PROMOCIONALES

### Banner Pequeño (440x280px)

**Diseño sugerido en Canva:**

1. **Crear diseño:** 440x280px
2. **Fondo:** Gradiente de #667eea a #764ba2 (diagonal)
3. **Elementos:**
   - Logo (arriba izquierda, 60x60px)
   - Título: "Calculadora Sin Fórmulas"
     - Font: Roboto Bold, 32px
     - Color: Blanco
   - Subtítulo: "15+ Herramientas para Google Sheets"
     - Font: Roboto Regular, 16px
     - Color: Blanco 90% opacidad
   - Badges (bottom):
     - "Sin Fórmulas"
     - "Gratis"
     - "Instantáneo"
   - Icono de Google Sheets (pequeño, esquina)

**Texto exacto:**
```
🧮 Calculadora Sin Fórmulas

15+ Herramientas para Google Sheets

[Sin Fórmulas] [Gratis] [Instantáneo]
```

### Banner Grande (1400x560px)

**Diseño sugerido:**

**Layout:**
```
┌──────────────────────────────────────────────┐
│  IZQUIERDA (60%)     │    DERECHA (40%)      │
│                      │                       │
│  🧮 Calculadora      │   [Screenshot 1]      │
│  Sin Fórmulas        │                       │
│                      │   [Screenshot 2]      │
│  15+ Herramientas    │                       │
│  • Sin código        │   [Screenshot 3]      │
│  • Instantáneo       │                       │
│  • Gratis            │                       │
│                      │                       │
│  [Obtener Gratis →]  │                       │
└──────────────────────────────────────────────┘
```

**Elementos:**
- **Fondo:** Gradiente sutil (blanco a #f0f4ff)
- **Lado izquierdo:**
  - Logo grande (128px)
  - Título: "Calculadora Sin Fórmulas"
  - Subtítulo: "Google Sheets Tools"
  - Lista de características
  - Botón CTA
- **Lado derecho:**
  - 3 screenshots pequeños en mosaico
  - Mostrar diferentes herramientas

---

## 🛠️ HERRAMIENTAS RECOMENDADAS

### Para Logos

1. **Canva** (Más fácil, recomendado)
   - https://www.canva.com/
   - Templates de logos
   - Exportar PNG transparente

2. **SVG to PNG** (Para usar el código SVG)
   - https://svgtopng.com/
   - Copiar código SVG
   - Descargar en múltiples tamaños

3. **Figma** (Profesional)
   - https://www.figma.com/
   - Más control de diseño

### Para Screenshots

1. **Snipping Tool** (Windows)
   - Win + Shift + S
   - Seleccionar área exacta

2. **Awesome Screenshot** (Chrome Extension)
   - Captura con anotaciones
   - Flechas, círculos, texto

3. **ShareX** (Windows, avanzado)
   - Captura + edición
   - Gratis y potente

### Para Banners

1. **Canva** (Recomendado)
   - Templates de banners
   - Drag & drop

2. **Photopea** (Alternativa gratis a Photoshop)
   - https://www.photopea.com/
   - Online, sin instalación

### Para Optimizar Imágenes

1. **TinyPNG**
   - https://tinypng.com/
   - Reduce peso sin perder calidad
   - Necesario para que Google acepte

2. **ImageOptim** (Mac)
   - Optimización local

---

## ✅ CHECKLIST FINAL DE CALIDAD

### Logos
- [ ] Tamaño exacto: 128x128 y 32x32
- [ ] Formato PNG con transparencia
- [ ] Peso < 50KB
- [ ] Reconocible a tamaño pequeño
- [ ] Colores consistentes con marca

### Screenshots
- [ ] Dimensiones exactas: 1280x800
- [ ] Formato PNG o JPG
- [ ] Peso < 2MB cada uno
- [ ] Sin información personal visible
- [ ] Datos de ejemplo realistas
- [ ] Interfaz limpia (sin errores visibles)
- [ ] Buena calidad (no pixelados)

### Banners
- [ ] Dimensiones exactas: 440x280 y 1400x560
- [ ] Formato PNG o JPG
- [ ] Peso < 2MB
- [ ] Texto legible
- [ ] Diseño atractivo
- [ ] Colores de marca

---

## 📥 ORGANIZACIÓN DE ARCHIVOS

Guardar en: `marketplace-assets/images/`

```
marketplace-assets/
└── images/
    ├── logos/
    │   ├── logo-128.png ✅
    │   └── logo-32.png ✅
    ├── screenshots/
    │   ├── screenshot-1-panel-lateral.png ✅
    │   ├── screenshot-2-calculadora-columnas.png ✅
    │   ├── screenshot-3-laboratorio-texto.png ✅
    │   ├── screenshot-4-super-buscador.png ✅
    │   └── screenshot-5-suma-condicional.png ✅
    └── banners/
        ├── promo-440x280.png ✅
        └── promo-1400x560.png ✅
```

---

## 🚀 PRÓXIMOS PASOS DESPUÉS DE CREAR ASSETS

1. **Optimizar todas las imágenes** con TinyPNG
2. **Subir a GitHub** (carpeta assets/)
3. **Actualizar appsscript.json** con URL del logo
4. **Continuar con GCP setup**
5. **Completar Marketplace listing**

---

## ⏱️ TIEMPO ESTIMADO

- **Logos:** 30-45 minutos (usando Canva o SVG)
- **Screenshots:** 1-2 horas (preparar datos + capturar + anotar)
- **Banners:** 45-60 minutos (diseño en Canva)
- **Optimización:** 15 minutos

**Total:** 3-4 horas

---

## 💡 TIPS PRO

1. **Consistencia visual:** Usa los mismos datos de ejemplo en todos los screenshots
2. **Storytelling:** Los screenshots deben contar una historia de uso
3. **Calidad > Cantidad:** Mejor 5 screenshots excelentes que 10 mediocres
4. **Anotaciones sutiles:** Si agregas flechas/texto, que sean minimalistas
5. **Test de thumbnail:** Los screenshots se ven pequeños en Marketplace, asegura que sean claros

---

**¿Listo para crear?** Empieza con el logo usando el código SVG o Canva! 🎨
