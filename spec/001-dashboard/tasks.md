# Tareas de implementación: Influencer Performance Dashboard

El dashboard se implementa en `index.html`; `server.py` se reutiliza sin cambios.

## 1. Estructura común y estilo

- [x] Crear `index.html` en la raíz con `<!doctype html>`, idioma español, codificación UTF-8 y viewport responsive.
- [x] Añadir el CDN oficial de Tailwind CSS v4: `https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4`.
- [x] Crear la estructura semántica base con `header`, `nav`, `main` y las tres secciones principales.
- [x] Definir un único `h1` y la jerarquía de encabezados para las secciones y subsecciones.
- [x] Crear navegación lateral oscura para escritorio y una presentación compacta para móvil.
- [x] Aplicar las paletas Ocean Analytics de modo claro y oscuro con utilities Tailwind y variantes `dark:`.
- [x] Hacer que el tema oscuro responda a la preferencia del sistema, sin añadir JavaScript de aplicación.
- [x] Establecer utilities coherentes para tipografía, espaciado, bordes y tarjetas.
- [x] Añadir indicadores positivos verdes, negativos rojos y advertencias ámbar con una señal adicional al color.

## 2. Bloque superior: KPIs

- [x] Crear una sección de KPIs con tarjetas y layout mobile-first.
- [x] Mostrar ventas generadas: 42.500 € y variación de +12,5 % respecto al mes anterior.
- [x] Mostrar comisión de Sarah: 6.375 €, identificando el cálculo del 15 % sobre 42.500 €.
- [x] Mostrar impacto de audiencia: 4,82 % y variación de −0,4 %.
- [x] Mostrar engagement medio: 7,2 % y variación de +2,1 %.

## 3. Bloque intermedio: Drivers

- [x] Crear subsecciones visualmente diferenciadas para plataformas, productos y actividad.
- [x] Añadir los ingresos y porcentajes reportados por plataforma: Instagram, TikTok y YouTube.
- [x] Verificar que los ingresos por plataforma sumen 42.500 € y los porcentajes, 100 %.
- [x] Añadir para cada producto categoría, precio, ingresos y tasa de conversión reportada.
- [x] Mostrar la comisión derivada al 15 % para cada producto: 2.280 €, 2.775 € y 1.320 €.
- [x] Verificar que los ingresos de productos sumen 42.500 € y las comisiones, 6.375 €.
- [x] Añadir actividad de Instagram: crecimiento, clics y compartidos.
- [x] Añadir actividad de TikTok: crecimiento, visualizaciones y tasa de finalización.
- [x] Añadir actividad de YouTube: variación, tiempo medio de visualización y CTR.
- [x] Identificar los datos reportados y evitar inferir tasas o métricas sin denominadores disponibles.

## 4. Bloque inferior: Detalles operacionales

- [x] Crear una subsección de colaboraciones recientes con una tabla semántica y accesible.
- [x] Añadir caption, encabezados de columna y asociaciones accesibles para los datos tabulares.
- [x] Incorporar las tres campañas con marca, estado, seguidores, ingresos, pago a Sarah y ROI reportados.
- [x] Indicar que los totales de campaña (38.500 € de ingresos y 5.775 € de pagos) son parciales y no reconcilian el consolidado.
- [x] Etiquetar los ROI de campaña como valores reportados, sin recalcularlos ni presentarlos como verificados.
- [x] Adaptar la presentación de la tabla a móvil sin desbordar la página y conservando la relación entre valores y encabezados.

## 5. Validación

- [x] Revisar que las métricas no calculables se omitan o se identifiquen como no disponibles.
- [x] Verificar landmarks, encabezados, tablas y legibilidad con ambos temas.
- [x] Comprobar contraste WCAG AA de textos e indicadores en modo claro y oscuro.
- [x] Revisar la interfaz en móvil (~375 px), tablet (768 px) y escritorio (1280 px o más).
- [x] Confirmar que no exista scroll horizontal de página y que la navegación se adapte a cada tamaño.
- [x] Ejecutar `python3 server.py` desde la raíz y comprobar `http://localhost:3000`.
- [x] Confirmar que solo se usen HTML5 y Tailwind CSS v4, sin otros frameworks, JavaScript de aplicación ni CSS personalizado.
- [x] Confirmar que `server.py` no haya sido modificado.

## 6. Mejoras de navegación y visualización

- [x] Situar la navegación antes del encabezado y reforzar su jerarquía con z-index, borde y sombra.
- [x] Añadir un gráfico accesible de ingresos por plataforma con valores y porcentajes reportados.
- [x] Añadir un gráfico accesible para comparar ingresos por producto con una escala explícita.
- [x] Validar los gráficos en tema claro y oscuro y revisar su adaptación responsive.
