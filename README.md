# App-de-cocteleria# Coctelería

**Escuela nocturna de coctelería.** Una plataforma para descubrir, aprender y preparar cócteles de nivel principiante a experto, con medidas exactas, técnica explicada y marcas para cada bolsillo.

🔗 **Sitio en vivo:** https://gabyfrancom.github.io/App-de-cocteleria/

> "No memorices cientos de cócteles: comprende las familias, proporciones, ingredientes y técnicas que los construyen."

---

## ✨ Funcionalidades

- **Carta** — 22 recetas clásicas, organizadas en 4 niveles de dificultad (Principiante a Experto), con ingredientes en ml y oz, pasos de preparación, copa, hielo, guarnición e historia.
- **Búsqueda global** — encuentra cócteles, ingredientes y marcas al mismo tiempo desde un solo buscador.
- **Favoritos** — guarda tus cócteles preferidos y fíltralos en cualquier momento.
- **Marcas** — guía de botellas por gama (esencial / media / premium) para cada destilado base, enlazada a los cócteles donde protagoniza.
- **Mi Barra** — marca los ingredientes que tienes en casa y la app te dice qué puedes preparar ya, y qué te falta por un solo ingrediente.
- **Técnica** — fichas de las técnicas de coctelería usadas en las recetas (shake, stir, build, muddle, dry shake, layer/float, rinse, ahumado): qué es, cuándo usarla, herramientas y errores frecuentes.
- **Multiplicador de cantidades** — recalcula automáticamente cualquier receta para ×2, ×3, ×5 o ×10 servicios.
- **Crear** — tu cuaderno de recetas propias, con foto, ingredientes, técnica y notas de cata, guardado localmente en el dispositivo.
- **PWA** — instalable en el móvil como una app nativa (manifest + iconos incluidos).

## 🛠️ Stack técnico

- [React 19](https://react.dev/) + [TypeScript](https://www.typescriptlang.org/)
- [Vite 7](https://vite.dev/) como build tool
- [Tailwind CSS 3](https://tailwindcss.com/) + [shadcn/ui](https://ui.shadcn.com/) (estilo "new york")
- Persistencia local: `localStorage` (barra, favoritos) e `IndexedDB` (creaciones propias con fotos)
- Sin backend: toda la app corre en el navegador

## 🚀 Desarrollo local

```bash
npm install
npm run dev       # servidor de desarrollo en http://localhost:3000
npm run build     # compila a /dist
npm run lint      # revisa el código con ESLint
```

## 📁 Estructura del proyecto

```
src/
  components/    # CocktailCard, DetailSheet, GlobalSearch
  views/         # Home (Carta), Brands (Marcas), Bar (Mi Barra), Techniques (Técnica), Create (Crear)
  data/          # cocktails.ts, ingredients.ts, brands.ts, techniques.ts — toda la data de la app
  lib/           # storage.ts (localStorage/IndexedDB), utils.ts
public/
  cocktails/     # fotografías de cada cóctel
  manifest.webmanifest, favicon.png, icon.png, apple-touch-icon.png
```

## 🌐 Despliegue

El sitio se publica con **GitHub Pages** desde la carpeta raíz de la rama `main`. Como se sirve desde una subruta (`/App-de-cocteleria/`), todas las rutas de imágenes e íconos son **relativas** (sin `/` inicial) tanto en el código como en `index.html` y `manifest.webmanifest` — importante tenerlo en cuenta si se cambia el nombre del repositorio.

Para desplegar una actualización:
1. `npm run build` (genera `/dist`)
2. Sube el contenido de `/dist` (no la carpeta en sí) a la raíz del repositorio.

## 🗺️ Roadmap

- [ ] Enciclopedia de ingredientes navegable (fichas propias)
- [ ] Modo Bartender / Servicio (interfaz simplificada para trabajar detrás de la barra)
- [ ] Bartenders históricos y línea de tiempo de la historia de la coctelería
- [ ] Academia progresiva + quiz interactivo
- [ ] Cristalería y herramientas como fichas propias
- [ ] Calculadora de coste por cóctel
- [ ] Backend / base de datos real para sincronizar entre dispositivos

## 📄 Licencia

Uso personal / educativo.
