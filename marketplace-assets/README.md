# 🎨 Assets para Google Workspace Marketplace

Esta carpeta contiene todos los assets visuales necesarios para publicar el complemento en Google Workspace Marketplace.

## 📋 Checklist de Assets Requeridos

### ✅ Logos e Iconos

- [ ] **logo-128.png** (128x128px)
  - Logo principal del complemento
  - Fondo transparente
  - Colores: `#1a73e8` y `#667eea`

- [ ] **logo-32.png** (32x32px)
  - Versión pequeña del logo
  - Debe ser reconocible a tamaño reducido

- [ ] **icon-128.png** (128x128px)
  - Icono que aparece en el menú de extensiones
  - Puede ser igual al logo-128

### ✅ Screenshots (1280x800px)

- [ ] **screenshot-1.png** - Panel Lateral Principal
  - Mostrar el panel lateral con la lista de herramientas
  - Destacar interfaz limpia y organizada

- [ ] **screenshot-2.png** - Calculadora de Columnas
  - Mostrar operación entre dos columnas
  - Incluir preview de resultados
  - Datos de ejemplo: ventas, cantidades

- [ ] **screenshot-3.png** - Laboratorio de Texto
  - Pipeline con 3-4 operaciones
  - Mostrar transformación antes/después

- [ ] **screenshot-4.png** - Super Buscador Visual
  - Búsqueda de duplicados o valores únicos
  - Mostrar resultados resaltados en la hoja

- [ ] **screenshot-5.png** - Suma Condicional
  - Condiciones configuradas
  - Resultado calculado visible

### ✅ Banners Promocionales

- [ ] **promo-440x280.png** (440x280px)
  - Banner pequeño para listado
  - Texto: "Calculadora Sin Fórmulas - 15+ Herramientas"
  - Íconos de herramientas principales

- [ ] **promo-1400x560.png** (1400x560px)
  - Banner grande para página de detalle
  - Diseño más elaborado
  - Incluir screenshots pequeños o mockups

---

## 🎨 Guía de Diseño

### Paleta de Colores

```css
/* Primarios */
--google-blue: #1a73e8;
--purple-gradient-start: #667eea;
--purple-gradient-end: #764ba2;

/* Secundarios */
--light-gray: #f8f9fa;
--text-primary: #202124;
--text-secondary: #5f6368;
```

### Tipografía

- **Principal**: Google Sans (o Roboto como alternativa)
- **Código/Monospace**: Roboto Mono

### Estilo Visual

- ✅ Minimalista y limpio
- ✅ Colores consistentes con interfaz del complemento
- ✅ Screenshots con datos realistas (no lorem ipsum)
- ✅ Sin marcas de agua ni branding excesivo
- ❌ NO usar capturas de pantalla borrosas
- ❌ NO incluir información personal en screenshots

---

## 📸 Cómo Crear Screenshots de Calidad

### Herramientas Recomendadas

1. **Para Captura:**
   - Windows: Snipping Tool, ShareX
   - Mac: Cmd+Shift+4
   - Chrome Extension: Awesome Screenshot

2. **Para Edición:**
   - Canva (plantillas listas)
   - Figma (diseño profesional)
   - Photoshop/GIMP (avanzado)

### Proceso Paso a Paso

1. **Preparar Google Sheets:**
   ```
   - Crear hoja con datos de ejemplo limpios
   - Usar nombres de columnas descriptivos
   - Evitar datos sensibles
   ```

2. **Configurar Herramienta:**
   ```
   - Abrir el complemento
   - Configurar operación visualmente atractiva
   - Asegurarse que el preview muestre resultados
   ```

3. **Capturar:**
   ```
   - Pantalla completa en 1280x800
   - O captura parcial y resize a 1280x800
   - Mantener relación de aspecto 16:10
   ```

4. **Anotar (opcional):**
   ```
   - Agregar flechas para destacar funcionalidades
   - Círculos alrededor de elementos importantes
   - Texto explicativo breve
   ```

### Ejemplos de Datos para Screenshots

#### Para Calculadora de Columnas:
```
| Producto    | Precio | Cantidad | Total |
|-------------|--------|----------|-------|
| Laptop      | 1200   | 5        | ?     |
| Mouse       | 25     | 20       | ?     |
| Teclado     | 75     | 10       | ?     |
```

#### Para Laboratorio de Texto:
```
| Nombre Original      | Transformado |
|---------------------|--------------|
| JUAN PÉREZ          | Juan Pérez   |
|   maría garcía   | María García |
| pedro_rodriguez     | Pedro Rodriguez |
```

#### Para Super Buscador:
```
| ID Cliente | Nombre      | Email              |
|-----------|-------------|--------------------|
| 001       | Ana López   | ana@email.com      |
| 002       | Ana López   | ana@email.com      | ← Duplicado
| 003       | Carlos Ruiz | carlos@email.com   |
```

---

## 🖼️ Plantillas Sugeridas

### Logo (128x128px)

```
┌─────────────────┐
│                 │
│    🧮          │
│   ────         │
│   CALC         │
│                 │
└─────────────────┘
```

**Elementos:**
- Icono calculadora estilizado
- Colores degradado azul-púrpura
- Sin texto (o solo iniciales)

### Banner Promocional (440x280px)

```
┌───────────────────────────────────────┐
│ 🧮 Calculadora Sin Fórmulas           │
│                                       │
│ ✨ 15+ Herramientas                   │
│ 📊 Sin Código | Instantáneo           │
│ 🎯 Para Google Sheets                 │
│                                       │
│         [Imagen de interfaz]          │
└───────────────────────────────────────┘
```

---

## ✅ Validación de Assets

Antes de subir, verificar:

- [ ] Todas las imágenes en formato PNG
- [ ] Dimensiones exactas según especificaciones
- [ ] Peso de archivo < 2MB cada una
- [ ] Sin pixelación o artefactos de compresión
- [ ] Colores consistentes con la marca
- [ ] Texto legible (si aplica)
- [ ] No hay información sensible visible

### Herramienta de Validación Online

Usar: https://www.websiteplanet.com/webtools/imagecompressor/
- Comprimir sin perder calidad
- Verificar dimensiones
- Optimizar para web

---

## 📦 Estructura Final

```
marketplace-assets/
├── README.md (este archivo)
├── logo-128.png ✅
├── logo-32.png ✅
├── icon-128.png ✅
├── screenshot-1.png ✅
├── screenshot-2.png ✅
├── screenshot-3.png ✅
├── screenshot-4.png ✅
├── screenshot-5.png ✅
├── promo-440x280.png ✅
├── promo-1400x560.png ✅
└── templates/ (opcional)
    ├── logo-template.psd
    ├── banner-template.psd
    └── screenshot-template.fig
```

---

## 🎯 Próximos Pasos

1. **Crear los assets** siguiendo esta guía
2. **Validar** usando el checklist de arriba
3. **Almacenar** en esta carpeta
4. **Subir** a Google Workspace Marketplace console
5. **Publicar** URLs en `appsscript.json` si es necesario

---

## 📞 Recursos Adicionales

- [Guía de Marca Google](https://about.google/brand-resource-center/)
- [Material Design Icons](https://fonts.google.com/icons)
- [Unsplash](https://unsplash.com/) - Imágenes stock gratuitas
- [Remove.bg](https://www.remove.bg/) - Remover fondos

---

**Última actualización:** Enero 2024
**Versión del complemento:** 1.0.0
