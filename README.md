# PujaYa — demo de subastas

PujaYa adaptado al catálogo académico “El objeto cotidiano como manifiesto (1945–1970)”. MVP visual en React + Vite + Tailwind, con estilos propios y cliente Supabase preparado.

## Ejecutar
1. Instalar Node.js LTS.
2. Descomprimir el proyecto y abrir la carpeta en VS Code.
3. En la terminal ejecutar `npm install`.
4. Ejecutar `npm run dev` y abrir la URL local que muestra Vite.

## Demo actual
- Home, catálogo de 15 lotes, filtros por sala, detalle curatorial, historial local, creación de publicaciones, carga de imagen, favoritos, login simulado y modo oscuro.
- Las subastas y pujas de esta primera entrega se guardan en localStorage del navegador.
- Las pujas respetan incremento mínimo, impiden ofertar al vendedor y aplican extensión de 2 minutos si la oferta llega en los últimos 2 minutos.
- El catálogo contiene los 15 lotes del PDF, distribuidos en Cocina (01–05), Sala de estar (06–11) y Taller, oficina y calle (12–15). Las fichas incorporan diseñador, fabricante/escuela, año, origen, materiales, relevancia histórica y conexiones entre objetos. Las imágenes de esta versión son referencias visuales del diseño original y conviene reemplazarlas por fotografías documentales de cada pieza antes de una presentación final.

## Conectar Supabase
1. Crear un proyecto en Supabase.
2. Copiar `.env.example` como `.env` y completar URL y anon key.
3. Ejecutar `supabase/schema.sql` desde el SQL Editor.
4. Configurar Storage con un bucket `auction-images` y políticas de acceso.
5. Implementar la puja como RPC transaccional antes de habilitar escrituras reales.

**Estado de esta entrega:** la interfaz y la demo local están implementadas; `src/supabase.js` deja preparado el cliente, pero autenticación real, persistencia remota, Storage y Realtime todavía requieren conexión y lógica backend. El esquema SQL es una base inicial, no una implementación segura completa del motor de pujas.

## Usuarios demo
La interfaz permite ingresar con cualquier email y contraseña (solo simulado). Podés usar por ejemplo:
- micaela@demo.com
- tomas@demo.com
- lucia@demo.com

No hay contraseñas reales ni pagos reales.
