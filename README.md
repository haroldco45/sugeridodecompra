# 🚀 Analizador de Pedidos Sugeridos - Vibras Positivas

Esta es una **Progressive Web App (PWA)** desarrollada para optimizar la reposición de inventarios en **Distrileco**. La herramienta procesa datos de ventas históricas y existencias actuales para calcular automáticamente cuánto pedir a cada proveedor.

## 📊 Lógica de Columnas (Mapeo Estricto)

La aplicación utiliza exclusivamente las siguientes columnas de la hoja de cálculo para su análisis:

* **O:** Nombre del Proveedor (Agrupador principal).
* **D:** Nombre del Producto / Descripción.
* **A:** Referencia Interna del producto.
* **L:** Promedio de ventas (últimos 60 días).
* **J:** Inventario Actual en Bodega.
* **H:** Sugerido original del sistema.
* **C:** Unidad de Medida (Caja, Bulto, UND).
* **V:** Fecha de la última compra realizada.
* **M:** Días transcurridos desde la última compra hasta hoy.

## 🧠 Algoritmo de Sugerido "Vibras"

El sistema calcula la necesidad de pedido basándose en la rotación mensual extraída del promedio de 60 días:

1.  **Consumo Mensual:** Se calcula como `L / 2`.
2.  **Sugerido App:** Si el **Inventario Actual (J)** es menor al consumo mensual, la App sugiere la diferencia exacta para cubrir los próximos 30 días de operación.
3.  **Alerta de Quiebre:** Los productos con stock crítico (menor al 25% del promedio) se resaltan visualmente.

## 📱 Características Técnicas

* **Offline First:** Funciona sin internet una vez cargada la página.
* **Privacidad:** Los datos del Excel se procesan en el navegador del usuario, no se suben a ningún servidor externo.
* **Geolocalización:** Cada pedido enviado por WhatsApp incluye las coordenadas exactas de la ubicación desde donde se genera.
* **Filtro Inteligente:** Permite buscar por proveedor para gestionar pedidos completos por marca.

---

## ⚖️ Propiedad Intelectual y Créditos

> **IMPORTANTE:** Toda la aplicación, código fuente y lógica de negocio son propiedad de **Vibras Positivas**.

* **Desarrollador:** Vibras Positivas
* **Derechos de Autor:** © 2026 Todos los derechos reservados.
* **Contacto de Soporte:** 3117700431
* **Ubicación:** Caucasia, Antioquia, Colombia.
