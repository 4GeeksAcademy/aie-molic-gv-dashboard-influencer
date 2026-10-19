# Influencer Performance Dashboard

## Propósito

Definir un dashboard de rendimiento para Sarah, influencer de Sarah's Studio, que consolide datos ficticios de Instagram, TikTok y YouTube en una vista clara para supervisar ventas, comisiones, productos, plataformas y colaboraciones.

## Usuarios y necesidades

- Sarah necesita consultar sus ventas generadas y la comisión que le corresponde.
- Sarah necesita comparar el rendimiento reportado por producto y plataforma.
- Sarah necesita revisar colaboraciones activas o pausadas y actividad reciente de sus canales.
- La información debe poder interpretarse en móvil, tablet y escritorio sin perder la jerarquía de los tres bloques principales.

## Requisitos funcionales

### Bloque superior: KPIs

El dashboard debe mostrar al menos tres KPIs en tarjetas visualmente coherentes. Debe incluir los siguientes valores ficticios:

| Indicador | Valor | Variación o contexto |
|---|---:|---|
| Ventas generadas (Total Revenue) | 42.500 € | +12,5 % respecto al mes anterior |
| Comisión de Sarah | 6.375 € | 15 % de 42.500 € |
| Impacto de audiencia (Audience Impact) | 4,82 % | −0,4 % |
| Engagement medio (Avg. Engagement) | 7,2 % | +2,1 % |

La comisión se calcula como `ventas generadas × 15 %`. Los 42.500 € representan ventas, no ganancias netas de Sarah.

### Bloque intermedio: drivers

El bloque debe presentar al menos tres drivers claramente diferenciados. Debe incluir los siguientes datos:

#### Rendimiento por plataforma

| Plataforma | Ingresos reportados | Porcentaje reportado |
|---|---:|---:|
| Instagram | 22.100 € | 52 % |
| TikTok | 14.450 € | 34 % |
| YouTube | 5.950 € | 14 % |
| **Total** | **42.500 €** | **100 %** |

#### Productos promocionados

| Producto | Categoría | Precio | Ingresos reportados | Tasa de conversión reportada | Comisión al 15 % sobre ingresos |
|---|---|---:|---:|---:|---:|
| Producto A | Skincare | 50 € | 15.200 € | 5,2 % | 2.280 € |
| Producto B | Apparel | 120 € | 18.500 € | 4,1 % | 2.775 € |
| Producto C | Accessory | 80 € | 8.800 € | 3,8 % | 1.320 € |
| **Total** |  |  | **42.500 €** |  | **6.375 €** |

Los precios unitarios y la comisión del 15 % deben quedar identificados como condiciones del negocio. Las comisiones por producto son derivadas de los ingresos reportados y la tasa acordada.

#### Actividad por plataforma

- **Instagram:** crecimiento +18 %, 45.200 clics y 1.200 compartidos.
- **TikTok:** crecimiento +32 %, 890.000 visualizaciones y 42 % de tasa de finalización.
- **YouTube:** variación −2 %, tiempo medio de visualización de 4 minutos y 12 segundos, y CTR de 2,8 %.

### Bloque inferior: detalles operacionales

El dashboard debe incluir una tabla o listado semántico de colaboraciones recientes con marca, campaña, estado, seguidores, ingresos reportados, pago a Sarah y ROI reportado.

| Marca | Campaña | Estado | Seguidores | Ingresos reportados | Pago a Sarah reportado | ROI reportado |
|---|---|---|---:|---:|---:|---:|
| Luxe Skincare | Summer Campaign | Activa | 245.000 | 12.400 € | 1.860 € | 6,2x |
| Urban Apparel | Fall Collection | Activa | 82.000 | 4.200 € | 630 € | 4,8x |
| Tech Gadgets | Review Video | Pausada | 1.200.000 | 21.900 € | 3.285 € | 5,4x |

Los datos de campaña corresponden a colaboraciones recientes, no necesariamente al total consolidado de ventas. Sus ingresos suman 38.500 € y los pagos reportados suman 5.775 €, por lo que no deben presentarse como si reconciliaran el total de 42.500 € y 6.375 €.

## Requisitos de presentación y semántica

- El documento debe usar HTML5 semántico con `header`, `nav`, `main`, `section` y, cuando corresponda, `article`, `table` y `footer`.
- Debe tener un único encabezado principal (`h1`) y una jerarquía lógica de encabezados para los tres bloques y sus drivers.
- Las tablas deben tener encabezados identificables y accesibles; los datos de campañas y productos deben conservar su asociación con cada columna en todos los tamaños.
- El diseño debe seguir la referencia visual del ejercicio: dashboard legible, jerarquía clara, agrupación consistente de KPIs, drivers y datos operacionales.
- La moneda de presentación es EUR (€). Los porcentajes y variaciones deben conservar el signo y formato proporcionados.
- Los datos son ficticios y el dashboard debe indicarlo de forma visible y concisa.

## Requisitos técnicos y responsive

- Utilizar exclusivamente HTML5 y Tailwind CSS v4, cargado en `<head>` desde `https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4`.
- No utilizar React, Vue, Bootstrap, otros frameworks, JavaScript ni CSS personalizado.
- Aplicar estilos y layout mediante clases utility de Tailwind, con enfoque mobile-first y breakpoints `sm:`, `md:` y `lg:`.
- En móvil, tablet y escritorio, los bloques deben mantener orden, legibilidad y jerarquía. Las tarjetas y columnas deben adaptarse al ancho disponible.
- No debe producirse scroll horizontal en la página. Las tablas deben adaptarse a pantallas pequeñas sin desbordar el viewport.
- Los gráficos son opcionales; si se incluyen, solo se permite Chart CSS construido sin CSS personalizado adicional.

## Identidad visual y temas

El dashboard debe seguir la identidad **Ocean Analytics**, con una estética moderna, minimalista y profesional basada en azules y turquesas. Los colores se aplicarán mediante clases utility de Tailwind, incluidas sus utilidades de color arbitrario cuando sean necesarias; no se permite definir CSS personalizado.

| Uso | Modo claro | Modo oscuro |
|---|---|---|
| Fondo principal | `#F5F8FC` | `#0B1424` |
| Tarjetas | `#FFFFFF` | `#162339` |
| Texto principal | `#152238` | `#F1F5F9` |
| Texto secundario | `#64748B` | `#94A3B8` |
| Acento | `#2563EB` | `#60A5FA` |
| Superficies suaves | `#CFFAFE` | `#164E63` |

- Se deben ofrecer estilos completos para ambos temas usando las variantes `dark:` de Tailwind CSS v4 y sin JavaScript. El modo oscuro debe seguir la preferencia de color del sistema; no se requiere un control interactivo de cambio de tema.
- En escritorio, la navegación lateral debe permanecer oscura en ambos temas y distinguirse con claridad del contenido principal. En móvil, la navegación debe adaptarse al espacio disponible sin provocar desbordamiento.
- Los estados positivos deben usar verde, los negativos rojo y las advertencias ámbar, con contraste suficiente sobre las superficies de ambos temas. El significado no debe depender exclusivamente del color.
- Espaciados, tipografía, bordes y tarjetas deben mantener una escala y estilo consistentes en toda la interfaz.
- El texto, los controles, los indicadores y los límites necesarios para distinguir componentes deben tener contraste adecuado en ambos temas. Como mínimo, el texto normal debe alcanzar contraste WCAG AA de 4,5:1 y el texto grande y elementos gráficos esenciales, 3:1.

## Tratamiento de métricas no calculables y discrepancias

- Se debe mostrar la tasa de conversión de productos tal como se proporcionó, pero no recalcularla: no se han facilitado los conteos de conversiones ni el denominador correspondiente.
- No se puede calcular el ROI de plataforma de forma independiente porque no se proporcionaron costes por plataforma. Los ROI de campañas se pueden mostrar únicamente como valores reportados, sin presentarlos como verificados o recalculados.
- El impacto de audiencia (4,82 %) y el engagement medio (7,2 %) se muestran como valores reportados; no se debe inferir su fórmula o desglose por plataforma o producto.
- No se proporcionan métricas suficientes para calcular engagement por plataforma o producto, conversiones totales, conversiones sobre alcance, coste por conversión ni alcance por plataforma. Deben omitirse o identificarse claramente como no disponibles, sin inventar cifras.
- Se proporcionó también un valor de 36.125 € como “My Earnings” después de una retención del 15 %. No coincide con la comisión de Sarah definida para este dashboard: el 15 % de 42.500 € es 6.375 €. Por tanto, 36.125 € no debe presentarse como comisión o ganancia de Sarah.
- La retención adicional del 15 % atribuida a la plataforma no tiene un significado suficientemente definido y no debe aplicarse al cálculo de la comisión de Sarah.

## Criterios de aceptación

1. La página identifica el dashboard, la marca Sarah's Studio, a Sarah y las tres plataformas consolidadas.
2. Hay tres bloques claramente distinguibles: KPIs, drivers y detalles operacionales.
3. El bloque superior contiene al menos tres KPIs; muestra 42.500 € de ventas y 6.375 € de comisión de Sarah, con el 15 % indicado.
4. El bloque de drivers contiene al menos tres factores diferenciados e incluye los datos de plataformas, productos y actividad definidos en esta especificación.
5. Los ingresos de las plataformas y productos suman 42.500 €; las comisiones de productos suman 6.375 €.
6. El bloque operacional muestra las tres colaboraciones, sus estados y los valores proporcionados; deja claro que los totales de campañas no reconcilian el total consolidado.
7. Los valores reportados se distinguen de los calculados, y las métricas no calculables o ambiguas no se presentan como resultados verificados.
8. El HTML conserva landmarks semánticos, encabezados jerárquicos y tablas accesibles.
9. La interfaz se adapta a móvil, tablet y escritorio mediante utilidades responsive de Tailwind; el contenido no genera scroll horizontal en la página.
10. Se utiliza el CDN oficial de Tailwind CSS v4 y no se incorporan frameworks, JavaScript ni CSS personalizado.
11. La interfaz aplica la identidad Ocean Analytics y los seis colores especificados para cada uno de los modos claro y oscuro.
12. Ambos temas se implementan con utilidades de Tailwind CSS v4, sin JavaScript ni CSS personalizado; el tema oscuro responde a la preferencia del sistema.
13. En escritorio la navegación lateral se mantiene oscura en ambos temas, y en móvil se adapta sin desbordamiento.
14. Los indicadores positivos, negativos y de advertencia se diferencian con verde, rojo y ámbar, respectivamente, además de una señal no basada solo en color.
15. Tipografía, espaciados, bordes y tarjetas son consistentes; el contraste cumple como mínimo WCAG AA para texto y elementos visuales esenciales en ambos temas.