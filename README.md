# El Taller de Ani - sitio listo para GitHub

Sitio estático original, responsive y adaptado a **El Taller de Ani**. Incluye inicio, membresías, catálogo demostrativo, filtros, carrito persistente, acceso/registro de demostración, newsletter y páginas legales.

## Publicar en GitHub Pages
1. Creá un repositorio nuevo en GitHub.
2. Subí el contenido de esta carpeta, no el ZIP.
3. En **Settings > Pages**, elegí **Deploy from a branch**.
4. Seleccioná `main` y `/ (root)`, y guardá.

## Qué funciona sin servidor
- Diseño responsive.
- Menú móvil.
- Filtros de cursos.
- Carrito y cantidades guardados en `localStorage`.
- Formularios con validación básica.
- Navegación y páginas legales.

## Qué requiere integración real
GitHub Pages solo sirve archivos estáticos. Para producción necesitás:
- **Login real:** Supabase Auth, Firebase Authentication o un backend propio.
- **Pagos y suscripciones:** Mercado Pago Subscriptions/Preapproval mediante backend. Nunca pongas el Access Token en JavaScript público.
- **Base de datos:** Supabase/PostgreSQL o Firebase.
- **Emails:** Brevo, Mailchimp o una API desde backend.
- **Contenido privado:** validar sesión y membresía activa en el servidor, no solo ocultar elementos con CSS/JavaScript.

## Mercado Pago, estructura recomendada
1. Crear una aplicación en Mercado Pago Developers.
2. Guardar el `ACCESS_TOKEN` como variable secreta en el hosting del backend.
3. Crear preferencias de pago o planes de suscripción desde el servidor.
4. Recibir webhooks y validar el estado del pago.
5. Actualizar la membresía del usuario en la base de datos.
6. Redirigir desde `checkoutBtn` a la URL devuelta por el backend.

## Personalización
- Colores: `assets/css/styles.css`, bloque `:root`.
- Cursos y precios: `assets/js/app.js`, arreglo `products`.
- Membresías: `assets/js/app.js`, arreglo `plans`.
- Soporte configurado: `anitaller80@gmail.com`.

## Aviso
Las tarjetas y textos de cursos son ejemplos claramente identificados. Deben reemplazarse con contenido real antes de publicar. El sitio no copia recursos gráficos, textos ni código de terceros.
