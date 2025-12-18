# GUÍA DE ESTILO VISUAL - TRUE CRIME FACTORY
## Sistema de Diseño para Web y Contenidos Digitales

**Versión:** 1.0
**Fecha:** Diciembre 2025
**Basado en:** Estética visual de "Crims" (TV3) y estilo cinematográfico de Carles Porta

---

## FILOSOFÍA VISUAL

El estilo visual de True Crime Factory se fundamenta en la tradición del **noir cinematográfico** combinado con un tratamiento documental contemporáneo. La estética debe transmitir:

- **Elegancia oscura** — Sofisticación visual sin sensacionalismo
- **Tensión controlada** — Atmósfera inquietante pero respetuosa
- **Credibilidad periodística** — Rigor visual que refuerza la autoridad narrativa
- **Inmersión emocional** — El espectador vive la experiencia en primera persona

---

## PALETA DE COLORES

### Colores Principales

| Nombre | Hex | RGB | Uso |
|--------|-----|-----|-----|
| **Negro Profundo** | `#0A0A0A` | 10, 10, 10 | Fondo principal, base |
| **Negro Carbón** | `#1A1A1A` | 26, 26, 26 | Fondos secundarios, cards |
| **Gris Sombra** | `#2D2D2D` | 45, 45, 45 | Elementos UI, bordes |
| **Gris Niebla** | `#4A4A4A` | 74, 74, 74 | Texto secundario |
| **Blanco Hueso** | `#F5F5F0` | 245, 245, 240 | Texto principal |
| **Blanco Puro** | `#FFFFFF` | 255, 255, 255 | Acentos, highlights |

### Colores de Acento

| Nombre | Hex | RGB | Uso |
|--------|-----|-----|
| **Rojo Sangre** | `#8B0000` | 139, 0, 0 | Alertas, elementos dramáticos |
| **Rojo Óxido** | `#722F37` | 114, 47, 55 | Hover states, CTAs secundarios |
| **Ámbar Evidencia** | `#B8860B` | 184, 134, 11 | Highlights, elementos archivo |
| **Azul Forense** | `#1E3A5F` | 30, 58, 95 | Links, elementos informativos |

### CSS Variables

```css
:root {
  /* Fondos */
  --tcf-bg-primary: #0A0A0A;
  --tcf-bg-secondary: #1A1A1A;
  --tcf-bg-elevated: #2D2D2D;

  /* Textos */
  --tcf-text-primary: #F5F5F0;
  --tcf-text-secondary: #4A4A4A;
  --tcf-text-muted: #6B6B6B;

  /* Acentos */
  --tcf-accent-red: #8B0000;
  --tcf-accent-red-hover: #722F37;
  --tcf-accent-gold: #B8860B;
  --tcf-accent-blue: #1E3A5F;

  /* Bordes */
  --tcf-border-subtle: rgba(255, 255, 255, 0.08);
  --tcf-border-visible: rgba(255, 255, 255, 0.15);

  /* Sombras */
  --tcf-shadow-sm: 0 2px 4px rgba(0, 0, 0, 0.5);
  --tcf-shadow-md: 0 4px 12px rgba(0, 0, 0, 0.6);
  --tcf-shadow-lg: 0 8px 24px rgba(0, 0, 0, 0.7);
}
```

---

## TIPOGRAFÍA

### Familias Tipográficas

| Rol | Fuente Principal | Fallback | Características |
|-----|------------------|----------|-----------------|
| **Títulos** | Oswald | Impact, sans-serif | Condensada, impacto visual |
| **Subtítulos** | Playfair Display | Georgia, serif | Elegancia editorial |
| **Cuerpo** | Source Sans Pro | Arial, sans-serif | Legibilidad óptima |
| **Monospace** | Source Code Pro | Courier, monospace | Datos, evidencias |

### Escala Tipográfica

```css
/* Sistema modular - ratio 1.250 (Major Third) */
:root {
  --tcf-text-xs: 0.64rem;    /* 10.24px */
  --tcf-text-sm: 0.8rem;     /* 12.8px */
  --tcf-text-base: 1rem;     /* 16px */
  --tcf-text-lg: 1.25rem;    /* 20px */
  --tcf-text-xl: 1.563rem;   /* 25px */
  --tcf-text-2xl: 1.953rem;  /* 31.25px */
  --tcf-text-3xl: 2.441rem;  /* 39px */
  --tcf-text-4xl: 3.052rem;  /* 48.8px */
  --tcf-text-5xl: 3.815rem;  /* 61px */
}
```

### Estilos de Texto

```css
/* Título principal - Impacto */
.tcf-title-hero {
  font-family: 'Oswald', Impact, sans-serif;
  font-size: var(--tcf-text-5xl);
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  line-height: 1.1;
  color: var(--tcf-text-primary);
}

/* Título de sección */
.tcf-title-section {
  font-family: 'Playfair Display', Georgia, serif;
  font-size: var(--tcf-text-3xl);
  font-weight: 600;
  letter-spacing: 0.02em;
  line-height: 1.2;
  color: var(--tcf-text-primary);
}

/* Subtítulo / Lead */
.tcf-subtitle {
  font-family: 'Source Sans Pro', Arial, sans-serif;
  font-size: var(--tcf-text-lg);
  font-weight: 300;
  line-height: 1.6;
  color: var(--tcf-text-secondary);
}

/* Cuerpo de texto */
.tcf-body {
  font-family: 'Source Sans Pro', Arial, sans-serif;
  font-size: var(--tcf-text-base);
  font-weight: 400;
  line-height: 1.75;
  color: var(--tcf-text-primary);
}

/* Etiquetas y metadatos */
.tcf-label {
  font-family: 'Oswald', sans-serif;
  font-size: var(--tcf-text-xs);
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 0.15em;
  color: var(--tcf-accent-gold);
}

/* Citas / Testimonios */
.tcf-quote {
  font-family: 'Playfair Display', Georgia, serif;
  font-size: var(--tcf-text-xl);
  font-style: italic;
  line-height: 1.5;
  color: var(--tcf-text-primary);
  border-left: 3px solid var(--tcf-accent-red);
  padding-left: 1.5rem;
}

/* Datos / Evidencia */
.tcf-evidence {
  font-family: 'Source Code Pro', Courier, monospace;
  font-size: var(--tcf-text-sm);
  background: var(--tcf-bg-elevated);
  padding: 0.25em 0.5em;
  border-radius: 2px;
}
```

---

## EFECTOS VISUALES

### Gradientes

```css
/* Gradiente oscuro - fade a negro */
.tcf-gradient-dark {
  background: linear-gradient(
    180deg,
    transparent 0%,
    rgba(10, 10, 10, 0.8) 60%,
    var(--tcf-bg-primary) 100%
  );
}

/* Gradiente dramático - rojo a negro */
.tcf-gradient-dramatic {
  background: linear-gradient(
    135deg,
    rgba(139, 0, 0, 0.15) 0%,
    transparent 50%,
    rgba(10, 10, 10, 1) 100%
  );
}

/* Vignette effect */
.tcf-vignette {
  box-shadow: inset 0 0 150px rgba(0, 0, 0, 0.9);
}
```

### Filtros de Imagen

```css
/* Estilo documental - desaturado con contraste */
.tcf-filter-documentary {
  filter:
    grayscale(40%)
    contrast(1.1)
    brightness(0.95);
}

/* Estilo archivo - envejecido */
.tcf-filter-archive {
  filter:
    sepia(30%)
    grayscale(20%)
    contrast(1.05);
}

/* Estilo evidencia - alto contraste */
.tcf-filter-evidence {
  filter:
    grayscale(100%)
    contrast(1.3)
    brightness(1.1);
}

/* Hover reveal - de desaturado a color */
.tcf-filter-reveal {
  filter: grayscale(100%);
  transition: filter 0.5s ease;
}
.tcf-filter-reveal:hover {
  filter: grayscale(0%);
}
```

### Animaciones

```css
/* Fade in desde la oscuridad */
@keyframes tcf-fade-in {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Pulso sutil - para elementos de alerta */
@keyframes tcf-pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.7; }
}

/* Línea de revelación */
@keyframes tcf-reveal-line {
  from { width: 0; }
  to { width: 100%; }
}

/* Typewriter effect para textos dramáticos */
@keyframes tcf-typewriter {
  from { width: 0; }
  to { width: 100%; }
}

.tcf-animate-in {
  animation: tcf-fade-in 0.6s ease-out forwards;
}

.tcf-animate-pulse {
  animation: tcf-pulse 2s ease-in-out infinite;
}
```

---

## COMPONENTES UI

### Cards de Episodio

```html
<article class="tcf-card-episode">
  <div class="tcf-card-image">
    <img src="thumbnail.jpg" alt="" class="tcf-filter-documentary">
    <div class="tcf-card-overlay"></div>
    <span class="tcf-card-duration">45:32</span>
  </div>
  <div class="tcf-card-content">
    <span class="tcf-label">Caso #12</span>
    <h3 class="tcf-card-title">El falso shaolín</h3>
    <p class="tcf-card-excerpt">Una llamada al 112 destapó a un asesino en serie...</p>
    <div class="tcf-card-meta">
      <time>2 jun 2013</time>
      <span>Bilbao</span>
    </div>
  </div>
</article>
```

```css
.tcf-card-episode {
  background: var(--tcf-bg-secondary);
  border: 1px solid var(--tcf-border-subtle);
  border-radius: 4px;
  overflow: hidden;
  transition: all 0.3s ease;
}

.tcf-card-episode:hover {
  border-color: var(--tcf-accent-red);
  box-shadow: var(--tcf-shadow-lg);
  transform: translateY(-4px);
}

.tcf-card-image {
  position: relative;
  aspect-ratio: 16/9;
  overflow: hidden;
}

.tcf-card-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(
    to top,
    rgba(10, 10, 10, 0.9) 0%,
    transparent 50%
  );
}

.tcf-card-duration {
  position: absolute;
  bottom: 0.5rem;
  right: 0.5rem;
  background: rgba(0, 0, 0, 0.8);
  padding: 0.25rem 0.5rem;
  font-family: 'Source Code Pro', monospace;
  font-size: var(--tcf-text-xs);
  color: var(--tcf-text-primary);
}

.tcf-card-content {
  padding: 1.25rem;
}

.tcf-card-title {
  font-family: 'Oswald', sans-serif;
  font-size: var(--tcf-text-xl);
  text-transform: uppercase;
  margin: 0.5rem 0;
  color: var(--tcf-text-primary);
}

.tcf-card-excerpt {
  font-size: var(--tcf-text-sm);
  color: var(--tcf-text-secondary);
  line-height: 1.5;
}

.tcf-card-meta {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
  font-size: var(--tcf-text-xs);
  color: var(--tcf-text-muted);
  text-transform: uppercase;
  letter-spacing: 0.1em;
}
```

### Intertítulos (Estilo Crims)

```html
<div class="tcf-intertitle">
  <span class="tcf-intertitle-number">03</span>
  <p class="tcf-intertitle-text">Los policías intuyen que no están solos</p>
</div>
```

```css
.tcf-intertitle {
  display: flex;
  align-items: center;
  gap: 1.5rem;
  padding: 2rem;
  background: var(--tcf-bg-primary);
  border-top: 1px solid var(--tcf-border-visible);
  border-bottom: 1px solid var(--tcf-border-visible);
}

.tcf-intertitle-number {
  font-family: 'Oswald', sans-serif;
  font-size: var(--tcf-text-4xl);
  font-weight: 700;
  color: var(--tcf-accent-red);
  line-height: 1;
}

.tcf-intertitle-text {
  font-family: 'Playfair Display', serif;
  font-size: var(--tcf-text-2xl);
  font-style: italic;
  color: var(--tcf-text-primary);
  margin: 0;
}
```

### Bloque de Testimonio

```html
<blockquote class="tcf-testimony">
  <div class="tcf-testimony-source">
    <span class="tcf-label">Declaración judicial</span>
    <time>24:10</time>
  </div>
  <p class="tcf-testimony-text">
    "Con mi pie izquierdo en un giro, noto como... piso algo parecido a una mano."
  </p>
  <cite class="tcf-testimony-cite">— Agente Ertzaintza, Juicio 2014</cite>
</blockquote>
```

```css
.tcf-testimony {
  position: relative;
  background: var(--tcf-bg-elevated);
  border-left: 4px solid var(--tcf-accent-red);
  padding: 1.5rem 2rem;
  margin: 2rem 0;
}

.tcf-testimony::before {
  content: '"';
  position: absolute;
  top: -0.5rem;
  left: 1rem;
  font-family: 'Playfair Display', serif;
  font-size: 4rem;
  color: var(--tcf-accent-red);
  opacity: 0.3;
}

.tcf-testimony-source {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

.tcf-testimony-source time {
  font-family: 'Source Code Pro', monospace;
  font-size: var(--tcf-text-sm);
  color: var(--tcf-text-muted);
}

.tcf-testimony-text {
  font-family: 'Playfair Display', serif;
  font-size: var(--tcf-text-xl);
  font-style: italic;
  line-height: 1.6;
  color: var(--tcf-text-primary);
  margin: 0;
}

.tcf-testimony-cite {
  display: block;
  margin-top: 1rem;
  font-family: 'Source Sans Pro', sans-serif;
  font-size: var(--tcf-text-sm);
  font-style: normal;
  color: var(--tcf-text-secondary);
}
```

### Timeline de Caso

```html
<div class="tcf-timeline">
  <div class="tcf-timeline-item">
    <div class="tcf-timeline-marker"></div>
    <div class="tcf-timeline-content">
      <time class="tcf-timeline-date">15:40</time>
      <p class="tcf-timeline-event">Llamada al 112</p>
    </div>
  </div>
  <div class="tcf-timeline-item tcf-timeline-item--active">
    <div class="tcf-timeline-marker"></div>
    <div class="tcf-timeline-content">
      <time class="tcf-timeline-date">15:43</time>
      <p class="tcf-timeline-event">Llegada de la primera patrulla</p>
    </div>
  </div>
  <!-- más items -->
</div>
```

```css
.tcf-timeline {
  position: relative;
  padding-left: 2rem;
}

.tcf-timeline::before {
  content: '';
  position: absolute;
  left: 0.5rem;
  top: 0;
  bottom: 0;
  width: 2px;
  background: var(--tcf-border-visible);
}

.tcf-timeline-item {
  position: relative;
  padding-bottom: 2rem;
}

.tcf-timeline-marker {
  position: absolute;
  left: -1.75rem;
  top: 0.25rem;
  width: 12px;
  height: 12px;
  background: var(--tcf-bg-secondary);
  border: 2px solid var(--tcf-text-secondary);
  border-radius: 50%;
}

.tcf-timeline-item--active .tcf-timeline-marker {
  background: var(--tcf-accent-red);
  border-color: var(--tcf-accent-red);
  box-shadow: 0 0 0 4px rgba(139, 0, 0, 0.3);
}

.tcf-timeline-date {
  display: block;
  font-family: 'Source Code Pro', monospace;
  font-size: var(--tcf-text-sm);
  color: var(--tcf-accent-gold);
  margin-bottom: 0.25rem;
}

.tcf-timeline-event {
  font-family: 'Source Sans Pro', sans-serif;
  font-size: var(--tcf-text-base);
  color: var(--tcf-text-primary);
  margin: 0;
}
```

---

## ICONOGRAFÍA Y SÍMBOLOS

### Sistema de Iconos

Usar iconos lineales (stroke) con las siguientes características:
- **Peso:** 1.5px stroke
- **Tamaño base:** 24x24px
- **Color por defecto:** `var(--tcf-text-secondary)`
- **Color activo:** `var(--tcf-text-primary)`

### Iconos Recomendados (Lucide/Feather)

| Concepto | Icono | Uso |
|----------|-------|-----|
| Caso | `file-text` | Identificar casos/episodios |
| Audio | `headphones` | Contenido podcast |
| Video | `play-circle` | Contenido video |
| Ubicación | `map-pin` | Localización del crimen |
| Fecha | `calendar` | Cronología |
| Persona | `user` | Víctimas, testigos |
| Alerta | `alert-triangle` | Contenido sensible |
| Búsqueda | `search` | Investigación |
| Documento | `file` | Evidencias, archivos |

---

## IMÁGENES Y FOTOGRAFÍA

### Tratamiento Visual

1. **Fotografías de archivo**
   - Aplicar `tcf-filter-archive`
   - Bordes sutiles con `border: 1px solid var(--tcf-border-subtle)`
   - Esquinas mínimamente redondeadas: `border-radius: 2px`

2. **Fotografías actuales**
   - Aplicar `tcf-filter-documentary`
   - Alto contraste, baja saturación

3. **Localizaciones**
   - Preferir tomas aéreas o angulares
   - Tratamiento desaturado
   - Uso de vignette para foco

4. **Retratos**
   - Fondo oscuro o difuminado
   - Iluminación lateral (estilo noir)
   - Mirada a cámara cuando sea posible

### Aspect Ratios

| Formato | Ratio | Uso |
|---------|-------|-----|
| Hero/Banner | 21:9 | Cabeceras de página |
| Thumbnail video | 16:9 | Cards de episodio |
| Cuadrado | 1:1 | Redes sociales, avatares |
| Vertical | 9:16 | Stories, shorts |
| Documental | 2.39:1 | Franjas cinematográficas |

---

## LAYOUT Y ESPACIADO

### Sistema de Grid

```css
:root {
  --tcf-grid-columns: 12;
  --tcf-grid-gutter: 1.5rem;
  --tcf-container-max: 1200px;
  --tcf-container-padding: 1rem;
}

.tcf-container {
  max-width: var(--tcf-container-max);
  margin: 0 auto;
  padding: 0 var(--tcf-container-padding);
}

@media (min-width: 768px) {
  :root {
    --tcf-container-padding: 2rem;
  }
}
```

### Escala de Espaciado

```css
:root {
  --tcf-space-1: 0.25rem;   /* 4px */
  --tcf-space-2: 0.5rem;    /* 8px */
  --tcf-space-3: 0.75rem;   /* 12px */
  --tcf-space-4: 1rem;      /* 16px */
  --tcf-space-5: 1.5rem;    /* 24px */
  --tcf-space-6: 2rem;      /* 32px */
  --tcf-space-8: 3rem;      /* 48px */
  --tcf-space-10: 4rem;     /* 64px */
  --tcf-space-12: 6rem;     /* 96px */
  --tcf-space-16: 8rem;     /* 128px */
}
```

---

## EJEMPLO: PÁGINA DE EPISODIO

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>El Falso Shaolín | True Crime Factory</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@400;500;700&family=Playfair+Display:ital,wght@0,400;0,600;1,400&family=Source+Code+Pro:wght@400;500&family=Source+Sans+Pro:wght@300;400;600&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="tcf-styles.css">
</head>
<body class="tcf-body-dark">

  <!-- Hero -->
  <header class="tcf-hero">
    <div class="tcf-hero-bg">
      <img src="hero-shaolin.jpg" alt="" class="tcf-filter-documentary">
      <div class="tcf-gradient-dark"></div>
      <div class="tcf-vignette"></div>
    </div>
    <div class="tcf-container tcf-hero-content">
      <span class="tcf-label">Caso #12 · Bilbao</span>
      <h1 class="tcf-title-hero">El Falso Shaolín</h1>
      <p class="tcf-subtitle">
        Una llamada de socorro al 112 destapó a un asesino en serie
        en pleno centro de Bilbao.
      </p>
      <div class="tcf-hero-meta">
        <time>2 de junio de 2013</time>
        <span>·</span>
        <span>45:32</span>
      </div>
    </div>
  </header>

  <!-- Contenido -->
  <main class="tcf-main">
    <div class="tcf-container">

      <!-- Intro -->
      <section class="tcf-section">
        <div class="tcf-intertitle">
          <span class="tcf-intertitle-number">01</span>
          <p class="tcf-intertitle-text">
            La llamada que lo cambió todo
          </p>
        </div>
        <div class="tcf-prose">
          <p>
            Eran las 15.40 de la tarde, a plena luz del día. Una mujer
            de mediana edad se asomó por casualidad a la ventana y vio
            algo que le llamó la atención...
          </p>
        </div>
      </section>

      <!-- Testimonio -->
      <blockquote class="tcf-testimony">
        <div class="tcf-testimony-source">
          <span class="tcf-label">Llamada 112</span>
          <time>15:40</time>
        </div>
        <p class="tcf-testimony-text">
          "¡La está metiendo adentro a golpes...!"
        </p>
        <cite class="tcf-testimony-cite">
          — Testigo anónima, llamada de emergencia
        </cite>
      </blockquote>

      <!-- Timeline -->
      <section class="tcf-section">
        <h2 class="tcf-title-section">Cronología</h2>
        <div class="tcf-timeline">
          <!-- items -->
        </div>
      </section>

    </div>
  </main>

  <!-- Footer -->
  <footer class="tcf-footer">
    <div class="tcf-container">
      <p class="tcf-footer-brand">True Crime Factory</p>
      <p class="tcf-footer-tagline">Llum a la foscor</p>
    </div>
  </footer>

</body>
</html>
```

---

## CHECKLIST DE IMPLEMENTACIÓN

### Antes de publicar cualquier página:

- [ ] Fondo oscuro (`#0A0A0A`) como base
- [ ] Tipografía Oswald para títulos en uppercase
- [ ] Playfair Display para citas y subtítulos elegantes
- [ ] Imágenes con filtro documental/archivo aplicado
- [ ] Acentos en rojo usado con moderación
- [ ] Contraste suficiente para accesibilidad (WCAG AA)
- [ ] Espaciado generoso entre secciones
- [ ] Intertítulos para separar bloques narrativos
- [ ] Testimonios destacados con border-left rojo
- [ ] Metadata (fechas, duraciones) en monospace

---

## PRINCIPIOS FUNDAMENTALES

1. **Oscuridad elegante** — El negro es protagonista, no ausencia
2. **Contraste dramático** — Luz y sombra con propósito narrativo
3. **Tipografía jerárquica** — Cada nivel tiene su personalidad
4. **Rojo con intención** — Solo para elementos de máximo impacto
5. **Desaturación controlada** — Color como excepción, no regla
6. **Respeto visual** — Sin morbo gráfico ni sensacionalismo
7. **Atmósfera inmersiva** — El visitante entra en la historia

---

**Documento elaborado por:** Zoopa Network Professional Team
**Referencia visual:** Crims (TV3), estética noir cinematográfica
**Estado:** Documento vivo - actualizar según evolución de marca

---

*"Crims presenta el lado más oscuro de la humanidad, y crea una atmósfera donde el espectador —acompañado por la voz en off de Carles Porta— vive la experiencia emocional en primera persona."*
— [Goroka](https://www.goroka.tv/project/crims/)
