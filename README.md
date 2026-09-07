# Hub Erick Nikson v1

Landing estática, mobile-first y sin backend para desplegar directamente en Vercel.

## Estructura

- `index.html` — contenido y metadata.
- `styles.css` — sistema visual, responsive, hover y cursor glow.
- `script.js` — seguimiento ligero del puntero en desktop.
- `assets/icons/` — íconos de marca de redes sociales.
- `assets/brand/monogram-en.svg` — **pendiente:** colocar aquí el monograma EN aprobado.
- `vercel.json` — configuración mínima y headers básicos.

## Monograma EN

El archivo maestro no venía adjunto a este chat. Para no recrearlo incorrectamente, la v1 intenta cargar `assets/brand/monogram-en.svg` y oculta ese elemento si el asset no existe.

Cuando tengas el SVG/PNG aprobado, colócalo como:

`assets/brand/monogram-en.svg`

Si el formato original es PNG, cambia las dos referencias en `index.html` o conviértelo desde la fuente maestra.

## Ejecutar localmente

No requiere instalación:

```bash
python3 -m http.server 4173
```

Luego abre `http://localhost:4173`.

## Desplegar en Vercel

### Opción A — Vercel Drop (la más directa para esta v1)
1. Abre Vercel Drop.
2. Arrastra la carpeta del proyecto o el ZIP `hub-erick-nikson-v1.zip`.
3. Elige equipo y nombre del proyecto.
4. Deploy.

Como el proyecto tiene `index.html` en la raíz y no usa framework, Vercel lo publica como sitio estático sin build.

### Opción B — GitHub
1. Sube esta carpeta a un repositorio.
2. En Vercel, crea un proyecto e importa el repositorio.
3. Mantén la raíz del proyecto en `./`.
4. No configures un build si Vercel detecta el proyecto como estático.
5. Deploy.

### Opción C — Vercel CLI
Desde esta carpeta:

```bash
vercel
```

Para producción:

```bash
vercel --prod
```

## Pendientes antes del dominio final

- Añadir el monograma EN aprobado.
- Crear favicon y social preview a partir del mismo asset.
- Tras definir dominio, añadir `canonical` y `og:url` en `index.html`.
