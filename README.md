# Fullstack Angular & NestJS Projects

![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)

---

## Sobre mí

Hola, soy **Jean Torres**, desarrollador **Fullstack** especializado en el stack **Angular + NestJS**, con desarrollo móvil en **Flutter**.  
Apasionado por crear aplicaciones web robustas, escalables y con las mejores prácticas del desarrollo moderno.

Este repositorio reúne algunos de mis proyectos personales, desarrollados con arquitectura limpia y desplegados para demostración en vivo.

**Objetivo:** Mostrar mis habilidades técnicas, estructura de proyectos y capacidad para construir aplicaciones reales end-to-end.

---

## Proyectos

### PetShop Online (LisaPet)

**Descripción:**  
Aplicación web completa para la gestión y venta de productos para mascotas, con catálogo dinámico, carrito de compras y sistema de autenticación seguro.

#### Tienda:

- Autenticación segura con JWT
- Catálogo de productos con variantes y galerías de imágenes
- Búsqueda y filtrado por categoría, marca y tipo de mascota
- Paginación e infinite scroll
- Carrito de compras con persistencia
- Lista de deseos (Wishlist)
- Checkout con pagos en línea (Culqi y Yape) confirmados por webhooks y métodos de pago guardados
- Envío a domicilio o recojo en agencia
- Direcciones de envío con ubigeo de Perú (departamento, provincia y distrito)
- Mis pedidos con historial de estados
- Soporte al cliente mediante tickets
- Libro de reclamaciones
- Preferencias de notificación
- Diseño responsive con TailwindCSS

#### Panel administrativo:

- Dashboard con métricas
- Gestión de productos, variantes y galerías
- Gestión de inventario
- Categorías, marcas y tipos de mascota
- Gestión de pedidos
- Punto de venta
- Roles y permisos, con menú y rutas filtrados según el rol
- Reportes financieros, de stock y de clientes
- Exportación de reportes (PDF, Excel, CSV)
- Gestión de clientes y usuarios internos
- Gestión de banners
- Configuración de despachos
- Configuraciones generales, integraciones y backups

### Aspectos técnicos

- API REST documentada con Swagger
- Autorización por roles y permisos en backend (guards) y frontend
- Integridad referencial completa en MySQL y procedimientos almacenados para los registros de usuarios
- Webhooks de pago con bloqueo transaccional para evitar pedidos duplicados
- Seguridad: Helmet, límite de peticiones y sesiones JWT multi-dispositivo
- Caché con Redis, imágenes en Cloudinary y correo transaccional (Resend)
- Backups automatizados con cron jobs y restauración de base de datos
- Skeletons de carga en todo el panel

### Próximamente

- Configuración de promociones y cupones
- Sistema de reseñas y feedback

### Tecnologías

Angular 21 · TailwindCSS · NestJS · MySQL (TypeORM) · Redis · JWT Authentication · TypeScript · Culqi y Yape · Cloudinary · Swagger/OpenAPI · Netlify y Railway (despliegue)

**Demo:** [Ver aplicación en vivo](https://lisapet.netlify.app/home)

**Video demostrativo:** [Ver video en YouTube](https://youtu.be/30-dXIeToNs)

#### Credenciales de demostración (para probar ambas interfaces)

| Rol       | Correo electrónico                  | Contraseña  |
|-----------|--------------------------------------|-------------|
| Admin     | `demo_admin@lisapets.com`       | `Lisapets2026`|
| Cliente   | `demo_cliente@lisapets.com`     | `Lisapets2026`|

#### Pagos con tarjeta (modo de prueba — sandbox)

El checkout usa el entorno de pruebas de Culqi. **No se procesa ningún cobro real bajo ninguna circunstancia** — no ingreses una tarjeta real, será rechazada por no coincidir con ningún caso de prueba reconocido. Usa una de estas:

| Escenario            | Número               | CVV | Vencimiento |
|-----------------------|-----------------------|-----|-------------|
| Compra exitosa         | 4111 1111 1111 1111 | 123 | 09/30       |
| Fondos insuficientes   | 4000 0400 0000 0008 | 295 | 03/30       |

---

### EcoRecoge: Aplicación de Servicio de Recolección de Residuos Sólidos

**Descripción:**  
Plataforma completa (app móvil, panel web y API) para el servicio de recolección de residuos sólidos: los vecinos consultan horarios, siguen al camión en tiempo real y reportan incidencias; los recolectores ven su ruta del día; y la municipalidad administra todo desde un panel web.

Versión 1.0 en 2024; versión 1.1 en 2026, con backend nuevo, migración a PostgreSQL, modo recolector y refuerzo de seguridad.

#### App móvil (Flutter) — publicada en Google Play:

- Horarios y rutas con filtros, paginación e infinite scroll
- "Mi parada": avance del camión hacia la parada del vecino en tiempo real
- Modo recolector: ruta del día, paradas atendidas, vehículo asignado y avisos de ruta
- Reportes de incidencias con foto y ubicación
- Notificaciones push (Firebase Cloud Messaging)
- Caché sin conexión y eliminación de cuenta desde la app
- Clean Architecture con Provider · 83 pruebas automatizadas

#### Panel web (Angular 21):

- Dashboard con KPIs y exportación a CSV
- Mapas con Leaflet: paradas, reportes y seguimiento de la ruta en vivo
- Gestión de usuarios, personal, horarios, rutas, vehículos y asignaciones semanales
- Roles y permisos configurables
- Notificaciones web push
- Seguridad en el navegador (CSP y cabeceras HTTP) · 61 pruebas unitarias

#### API (NestJS 12 + PostgreSQL):

- PostgreSQL en Supabase con funciones PL/pgSQL (migrado desde MySQL)
- Sesiones con Redis y rotación de refresh tokens en cookie HttpOnly
- Control de acceso por roles (RBAC) y límite de peticiones contra fuerza bruta
- Notificaciones push (FCM y Web Push), correo (Resend), SMS (Twilio) e imágenes en Cloudinary
- 313 pruebas de integración

**Tecnologías:**
Flutter · Dart · Angular 21 · TypeScript · Leaflet · NestJS 12 · PostgreSQL (Supabase) · Redis · Firebase · Vercel y Railway (despliegue)

**Demo web:** [Ver aplicación web en vivo](https://ecorecoge.vercel.app)

**Demo móvil:** [ Ver aplicación en Google Play](https://play.google.com/store/apps/details?id=com.ecohuancan.ecorecoge)

#### Credenciales de demostración (para probar ambas interfaces)

| Rol       | Correo electrónico                  | Contraseña  |
|-----------|--------------------------------------|-------------|
| Admin     | `demo_admin@gmail.com`       | `EcoRecoge2026`|
| Cliente   | `demo_cliente@gmail.com`     | `EcoRecoge2026`|
---

### ⚡ Aplicación Pokémon SSR

**Descripción:**  
Aplicación desarrollada con Server-Side Rendering (SSR) para optimizar el rendimiento y SEO. Implementa patrones avanzados de Angular y consumo eficiente de APIs externas.

**Características:**
- Server-Side Rendering (SSR)
- Listado completo de Pokémon
- Paginación optimizada
- Carga rápida y SEO-friendly

**Tecnologías:**
- Angular SSR
- NestJS
- MySQL
- TypeScript
- REST API
- Notificaciones

**Demo:** [Ver aplicación en vivo](https://pokemon-ssr-angular-jtr.netlify.app/pokemons?page=1)  
**Repositorio:** [Ver código fuente](https://github.com/JeanTR20/pokemon_SSR)

---

### Gif App

**Descripción:**  
Aplicación interactiva para búsqueda y visualización de GIFs animados, desarrollada para reforzar conceptos de consumo de APIs externas y manejo de estado en Angular.

**Características:**
- Búsqueda de GIFs en tiempo real
- Trending GIFs
- Historial de búsquedas
- Diseño responsive
- Carga lazy de imágenes
- Interfaz moderna con TailwindCSS

**Tecnologías:**
- Angular
- TypeScript
- TailwindCSS
- Giphy API
- Reactive Forms

**Demo:** [Ver aplicación en vivo](https://gif-app-jean-torres.netlify.app/#/dashboard/trending)  
**Repositorio:** [Ver código fuente](https://github.com/JeanTR20/gifs_app)

---

## Habilidades Técnicas

### Frontend
- **Framework:** Angular 21
- **Lenguajes:** TypeScript, JavaScript, HTML5, CSS3
- **Estilos:** TailwindCSS, SCSS
- **Conceptos:** Reactive Programming, RxJS, Signals
- **SSR:** Angular Universal
- **Mapas:** Leaflet
- **Responsive Design**

### Mobile
- **Framework:** Flutter (Dart)
- **Estado y arquitectura:** Provider, Clean Architecture
- **Servicios:** Firebase Cloud Messaging, publicación en Google Play

### Backend
- **Framework:** NestJS
- **APIs:** REST API, Swagger/OpenAPI, webhooks
- **Autenticación:** JWT, refresh tokens, Guards, Interceptors, RBAC
- **Seguridad:** Helmet, límite de peticiones, cookies HttpOnly
- **Arquitectura:** Modular, Clean Architecture

### Base de Datos
- **SQL:** PostgreSQL (PL/pgSQL), MySQL
- **Caché y sesiones:** Redis
- **ORM:** TypeORM
- **Diseño:** Modelado de datos, Relaciones, funciones y procedimientos almacenados

### Testing
- Jest, Karma/Jasmine, Flutter test, pruebas de integración de API

### DevOps & Herramientas
- **Control de versiones:** Git, GitHub
- **Despliegue continuo:** Vercel, Netlify, Railway (deploy automático al hacer push)
- **Servicios:** Supabase, Cloudinary, Firebase
- **Otros:** npm, Postman, VS Code


---

## Notas

- Los proyectos están desplegados con fines **demostrativos y educativos**.
- Algunas funcionalidades pueden estar limitadas en el entorno de prueba.
- El backend y las credenciales sensibles no se exponen públicamente por seguridad.
- Todos los proyectos siguen las mejores prácticas de desarrollo y clean code.

---

## Contacto

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/JeanTR20)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](http://www.linkedin.com/in/jeantr)

**Email:** Disponible en mi perfil de LinkedIn

---

## Agradecimientos

Gracias por visitar mi portafolio.

---

<p align="center">
  <i>Desarrollado por Jean Torres</i>
</p>

<p align="center">
  <sub>© 2025 Jean Torres. Todos los derechos reservados.</sub>
</p>
