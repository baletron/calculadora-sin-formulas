# 📸 Guía Completa: Capturar Screenshots para Google Marketplace

## 🎯 Objetivo

Capturar 5 screenshots de **1280x800 pixels** mostrando las herramientas en acción.

---

## ⚙️ Configuración Previa (5 minutos)

### 1. Ajustar Resolución de Navegador

**Opción A: Usando DevTools de Chrome**
```
1. Abrir Google Sheets con tu add-on
2. Presionar F12 (DevTools)
3. Click en icono "Toggle device toolbar" (Ctrl+Shift+M)
4. Configurar:
   - Dimensions: Responsive
   - Width: 1280px
   - Height: 800px
   - Zoom: 100%
```

**Opción B: Ventana del navegador**
```
1. Presionar F11 (pantalla completa)
2. Salir con F11
3. Ajustar ventana manualmente lo más cercano a 1280x800
```

### 2. Preparar Datos de Ejemplo

Crear una hoja de cálculo con datos de prueba:

```
Copiar estos datos a Google Sheets:
```

**Hoja: "VentasProductos"**
```
A          B        C         D        E
Producto   Precio   Cantidad  Fecha    Cliente
Laptop     1200     5         2024-01-15  Juan Pérez
Mouse      25       120       2024-01-16  María García
Teclado    75       45        2024-01-17  Carlos López
Monitor    350      12        2024-01-18  Ana Martínez
Laptop     1200     3         2024-01-19  Pedro Sánchez
Mouse      25       80        2024-01-20  Laura Díaz
USB        15       200       2024-01-21  Jorge Ruiz
Monitor    350      8         2024-01-22  Sofía Torres
Teclado    75       30        2024-01-23  Miguel Ángel
Laptop     1200     7         2024-01-24  Elena Castro
```

---

## 📸 Screenshot 1: Panel Lateral (Vista General)

### Qué Mostrar
- Panel lateral abierto con todas las herramientas visibles
- Hoja de cálculo con datos de fondo
- Menú "Extensiones" desplegado (opcional)

### Pasos para Capturar

1. **Abrir Google Sheets** con tus datos de ejemplo
2. **Abrir el add-on:**
   - Extensiones → Calculadora Sin Fórmulas → Abrir Panel
3. **Posicionar:**
   - Panel lateral a la derecha completamente visible
   - Columnas A-D visibles con datos
4. **Capturar:**
   - Windows: `Windows + Shift + S` → Seleccionar área
   - Mac: `Cmd + Shift + 4`
   - O usar extensión de Chrome: "Awesome Screenshot"

### Composición Ideal
```
┌─────────────────────────────────────┐
│ Google Sheets - VentasProductos     │
├─────────────────┬───────────────────┤
│  Datos         │ Panel Lateral     │
│  A  B  C  D    │ ┌───────────────┐ │
│  Producto      │ │ 15+ Tools     │ │
│  Laptop        │ │ ● Calculadora │ │
│  Mouse         │ │ ● Laboratorio │ │
│  Teclado       │ │ ● Buscador    │ │
│  ...           │ │ ● Suma Cond.  │ │
│                │ │ ● ...         │ │
└─────────────────┴───────────────────┘
```

---

## 📸 Screenshot 2: Calculadora de Columnas

### Qué Mostrar
- Calculadora de Columnas abierta
- Operación configurada (ej: Precio × Cantidad)
- Preview de resultados visible

### Preparación de Datos

1. Tener columnas: **Precio (B)**, **Cantidad (C)**
2. Abrir: **Calculadora de Columnas**
3. Configurar:
   - Columna 1: Precio (B)
   - Operación: × (multiplicar)
   - Columna 2: Cantidad (C)
   - Columna destino: F (Total)

### Captura Perfecta

**Timing:** Capturar cuando el preview muestra:
```
Preview:
1200 × 5 = 6000
25 × 120 = 3000
75 × 45 = 3375
...
```

**Elementos Visibles:**
- Selectores de columna con valores seleccionados
- Botón de operación (×) destacado
- Preview con al menos 3 resultados
- Botón "Aplicar" visible

---

## 📸 Screenshot 3: Laboratorio de Texto

### Qué Mostrar
- Pipeline de transformaciones visible
- 2-3 transformaciones aplicadas
- Preview mostrando antes/después

### Configuración Sugerida

**Datos de entrada (Columna A):**
```
  juan pérez
  MARÍA GARCÍA
  carlos lópez
```

**Pipeline:**
1. **Trim** (eliminar espacios)
2. **Capitalize** (Primera letra mayúscula)
3. **Extraer Nombre** (primera palabra)

**Preview esperado:**
```
Antes          → Después
  juan pérez   → Juan
  MARÍA GARCÍA → María
  carlos lópez → Carlos
```

### Captura Perfecta

**Elementos Visibles:**
- Lista de transformaciones disponibles (izquierda)
- Pipeline con 2-3 pasos agregados (centro)
- Preview con resultados (derecha)
- Datos originales vs transformados

---

## 📸 Screenshot 4: Super Buscador Visual

### Qué Mostrar
- Buscador activo con resultados encontrados
- Duplicados o coincidencias resaltadas
- Panel de resultados con conteo

### Preparación

**Agregar datos con duplicados:**
```
A          B
Laptop     1200
Mouse      25
Laptop     1200  ← Duplicado
Teclado    75
Mouse      25    ← Duplicado
```

**Configurar Buscador:**
1. Abrir: **Super Buscador Visual**
2. Modo: "Buscar Duplicados"
3. Columna: A (Producto)
4. Click: "Buscar"

### Captura Perfecta

**Elementos Visibles:**
- Resultados: "3 duplicados encontrados"
- Celdas resaltadas en color
- Panel con lista de duplicados:
  ```
  ✓ Laptop (2 veces)
  ✓ Mouse (2 veces)
  ```
- Botones de acción visibles

---

## 📸 Screenshot 5: Suma Condicional Visual

### Qué Mostrar
- Configuración de condiciones
- Preview de suma calculada
- Datos que cumplen condición resaltados (opcional)

### Configuración Sugerida

**Objetivo:** Sumar total de ventas de "Laptop"

**Configurar:**
1. Abrir: **Suma Condicional Visual**
2. Rango datos: A2:C11
3. Columna condición: A (Producto)
4. Condición: "igual a"
5. Valor: "Laptop"
6. Columna a sumar: C (Cantidad)

**Resultado esperado:**
```
Suma: 15 unidades
(5 + 3 + 7 = 15 laptops vendidos)
```

### Captura Perfecta

**Elementos Visibles:**
- Selectores de rango y columna configurados
- Dropdown de condición ("igual a" seleccionado)
- Input con valor "Laptop"
- Preview grande mostrando resultado: **15**
- Mensaje: "3 filas cumplen la condición"

---

## 🛠️ Herramientas Recomendadas para Capturar

### Opción 1: Windows Built-in (GRATIS)
```
Windows + Shift + S
- Seleccionar área rectangular
- Se copia al clipboard
- Pegar en Paint/GIMP
- Save as PNG
```

### Opción 2: Extensión Chrome (MÁS FÁCIL)
```
"Awesome Screenshot" o "Nimbus Screenshot"
- Instalar desde Chrome Web Store
- Click en icono → "Capture visible part"
- Editar y agregar anotaciones
- Download PNG
```

### Opción 3: ShareX (Windows, PROFESIONAL)
```
https://getsharex.com/
- Captura con hotkey personalizado
- Auto-resize a 1280x800
- Upload automático
- Múltiples opciones de edición
```

### Opción 4: Lightshot (Windows/Mac)
```
https://app.prntscr.com/
- Click y arrastrar para capturar
- Editor integrado
- Compartir/Descargar PNG
```

---

## ✅ Checklist de Calidad

### Antes de Capturar
- [ ] Navegador en modo claro (no dark mode)
- [ ] Zoom al 100% (Ctrl+0)
- [ ] Sin notificaciones ni popups
- [ ] Datos de ejemplo preparados
- [ ] Herramienta abierta y configurada

### Durante la Captura
- [ ] Área seleccionada: 1280x800 pixels exactos
- [ ] Panel lateral completamente visible
- [ ] Preview/resultados visibles
- [ ] Textos legibles (no borrosos)
- [ ] Sin información personal sensible

### Después de Capturar
- [ ] Revisar resolución: 1280x800px
- [ ] Tamaño de archivo < 500KB (idealmente < 300KB)
- [ ] Formato: PNG (no JPG para mejor calidad)
- [ ] Nombre descriptivo:
  - `screenshot-1-panel-lateral.png`
  - `screenshot-2-calculadora-columnas.png`
  - `screenshot-3-laboratorio-texto.png`
  - `screenshot-4-buscador-duplicados.png`
  - `screenshot-5-suma-condicional.png`

---

## 🎨 Optimización Post-Captura

### Ajustar Tamaño (si no es exacto)

**Usando GIMP (gratis):**
```
1. Image → Scale Image
2. Width: 1280, Height: 800
3. Quality: Cubic (best quality)
4. Export as PNG
```

**Usando Online:**
```
https://www.iloveimg.com/resize-image
- Upload screenshot
- Custom size: 1280x800
- Download resized
```

### Comprimir (reducir tamaño de archivo)

```
https://tinypng.com/
- Subir PNG
- Descargar versión comprimida
- Reduce hasta 70% sin pérdida visual
```

---

## 📊 Comparación de Tamaños

```
Screenshot sin optimizar:    800 KB - 1.5 MB  ❌ Muy pesado
Screenshot optimizado:       200 KB - 400 KB  ✅ Perfecto
Screenshot sobre-comprimido: < 100 KB          ⚠️  Puede perder calidad
```

**Objetivo:** 200-400 KB por screenshot

---

## 🚀 Workflow Rápido (30 minutos total)

```
1. Preparar datos de ejemplo           [5 min]
2. Abrir add-on y posicionar ventana   [2 min]
3. Screenshot 1: Panel lateral         [3 min]
4. Screenshot 2: Calculadora          [5 min]
5. Screenshot 3: Laboratorio          [5 min]
6. Screenshot 4: Buscador             [5 min]
7. Screenshot 5: Suma Condicional     [5 min]
8. Revisar y optimizar todas          [5 min]

TOTAL: 35 minutos
```

---

## 🎯 Siguiente Paso

Una vez tengas los 5 screenshots:

```bash
# 1. Mover a carpeta marketplace-assets
# 2. Renombrar correctamente
# 3. Subir a GitHub

cd marketplace-assets
git add screenshot-*.png
git commit -m "Add 5 screenshots for Marketplace"
git push
```

---

## 📁 Estructura Final

```
marketplace-assets/
├── logo-128.png ✅
├── logo-32.png ✅
├── promo-440x280.png ✅
├── promo-1400x560.png ✅
├── screenshot-1-panel-lateral.png ← CAPTURAR
├── screenshot-2-calculadora-columnas.png ← CAPTURAR
├── screenshot-3-laboratorio-texto.png ← CAPTURAR
├── screenshot-4-buscador-duplicados.png ← CAPTURAR
└── screenshot-5-suma-condicional.png ← CAPTURAR
```

---

## 🆘 Troubleshooting

### "No puedo capturar exactamente 1280x800"
**Solución:** Captura más grande y resize después con GIMP/iloveimg

### "Preview no se ve en screenshot"
**Solución:** Esperar 1-2 segundos después de configurar para que preview cargue

### "Texto se ve borroso"
**Solución:** Asegurar zoom al 100% y capturar en resolución nativa

### "Archivo muy pesado"
**Solución:** Pasar por tinypng.com para comprimir sin pérdida

---

**¡Con estas 5 screenshots completarás los Assets Visuales!** 🎉

**Siguiente:** Subir todo a GitHub y actualizar appsscript.json con URLs correctas.
