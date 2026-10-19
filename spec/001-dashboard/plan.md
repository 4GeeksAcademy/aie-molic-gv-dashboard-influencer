# Plan de implementación: Influencer Performance Dashboard

## Objetivo

Implementar un dashboard estático para Sarah's Studio en un único `index.html`, usando HTML5 semántico y Tailwind CSS v4 desde el CDN oficial. La interfaz consolidará las métricas ficticias de Instagram, TikTok y YouTube en los tres bloques definidos por la especificación.

## Alcance por bloques

### 1. Estructura común e indicadores principales

- Crear `index.html` en la raíz del repositorio con metadatos, viewport y el CDN oficial `https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4`.
- Definir la jerarquía semántica con `header`, `nav`, `main`, `section`, encabezados y landmarks accesibles.
- Diseñar una navegación lateral oscura en escritorio y una variante compacta para móvil.
- Aplicar la identidad Ocean Analytics con los temas claro y oscuro mediante utilities de Tailwind y variantes `dark:`, siguiendo la preferencia del sistema.
- Presentar tarjetas KPI para ventas generadas (42.500 €), comisión de Sarah (6.375 €, equivalente al 15 %), impacto de audiencia (4,82 %) y engagement medio (7,2 %).
- Distinguir estados positivos, negativos y advertencias mediante color y una señal adicional, como texto o iconografía.

### 2. Drivers

- Mostrar como áreas diferenciadas el rendimiento por plataforma, los productos promocionados y la actividad por plataforma.
- En plataformas, presentar los ingresos y porcentajes reportados de Instagram, TikTok y YouTube.
- En productos, mostrar categoría, precio, ingresos, tasa de conversión reportada y comisión derivada al 15 %.
- En actividad, presentar las cifras disponibles de clics, compartidos, visualizaciones, finalización, tiempo de visualización, CTR y variaciones de cada plataforma.
- Identificar claramente qué cifras son reportadas y cuáles se derivan del modelo de comisión.

### 3. Detalles operacionales

- Mostrar las tres colaboraciones recientes en una tabla accesible con marca, campaña, estado, seguidores, ingresos, pago a Sarah y ROI reportados.
- Adaptar la tabla para móvil conservando la asociación entre cada dato y su encabezado, sin provocar scroll horizontal de página.
- Indicar que las colaboraciones suman 38.500 € en ingresos y 5.775 € en pagos, por lo que sus cifras no reconcilian el consolidado de 42.500 € y 6.375 €.
- Mostrar el ROI de campaña únicamente como dato reportado, sin recalcularlo ni presentarlo como verificado.

## Consideraciones técnicas y visuales

- Usar exclusivamente HTML5 y Tailwind CSS v4; no añadir frameworks, CSS personalizado ni JavaScript propio de la aplicación.
- Reutilizar `server.py` sin modificarlo para servir `index.html`.
- Seguir un diseño mobile-first con breakpoints `sm:`, `md:` y `lg:`; mantener legibilidad y jerarquía en móvil, tablet y escritorio.
- Aplicar de forma consistente los colores y superficies de ambos temas especificados para Ocean Analytics. La navegación lateral debe permanecer oscura en escritorio en ambos temas.
- Mantener escalas consistentes de tipografía, espaciado, bordes y tarjetas, y verificar contraste WCAG AA en ambos temas.
- Omitir o identificar como no disponibles las métricas que no puedan derivarse de los datos proporcionados; no inventar denominadores, alcance ni costes.
- Interpretar “sin JavaScript” como ausencia de JavaScript de aplicación. El CDN oficial de Tailwind Browser v4 es un script y requiere conectividad externa.
- No añadir un selector manual de tema: el modo oscuro seguirá la preferencia de color del sistema mediante Tailwind.

## Archivos relevantes

- `index.html`: nuevo punto de entrada, con estructura semántica, contenido ficticio y utilities Tailwind.
- `server.py`: servidor existente que se reutilizará sin cambios.
- `spec/001-dashboard/spec.md`: requisitos y criterios de aceptación que rigen la implementación.

## Verificación

1. Ejecutar `python3 server.py` desde la raíz y comprobar el dashboard en `http://localhost:3000`.
2. Revisar visualmente los temas claro y oscuro en móvil (~375 px), tablet (768 px) y escritorio (1280 px o más); confirmar que no hay desbordamiento horizontal y que la navegación se adapta.
3. Revisar landmarks, jerarquía de encabezados, tablas accesibles, legibilidad y contraste WCAG AA para texto e indicadores en ambos temas.
4. Comprobar los datos: el 15 % de 42.500 € es 6.375 €; las comisiones derivadas por producto suman 6.375 €; los totales de las campañas se mantienen como datos parciales reportados.
5. Confirmar el uso exclusivo de HTML5 y del CDN oficial de Tailwind v4, sin frameworks, JavaScript propio ni CSS personalizado, y verificar que `server.py` no fue modificado.
