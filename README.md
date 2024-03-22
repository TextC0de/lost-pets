# Resumen Detallado de la Aplicación de Lost Pets

La aplicación de Lost Pets es una herramienta digital innovadora diseñada con el propósito principal de facilitar la búsqueda y recuperación de mascotas perdidas. A través de una interfaz amigable y funcionalidades avanzadas, esta aplicación busca crear una comunidad solidaria entre los dueños de mascotas, proporcionando recursos tecnológicos para aumentar las posibilidades de reunir a las mascotas perdidas con sus familias.

## Tabla de Contenidos

- [Lost Pets](#lost-pets)
  - [Introducción](#introducción)
  - [Características Principales](#características-principales)
- [Tecnologías y Herramientas](#tecnologías-y-herramientas)
  - [Aplicación Móvil](#aplicación-móvil)
  - [Backend](#backend)
  - [Otros Componentes](#otros-componentes)
- [Plan de Desarrollo](#plan-de-desarrollo)
  - [Fase 1: Diseño y Prototipado](#fase-1-diseño-y-prototipado)
    - [1. Reporte de Mascotas Perdidas/Encontradas](#1-reporte-de-mascotas-perdidasencontradas)
    - [2. Visualización en Mapa](#2-visualización-en-mapa)
    - [3. Detalles y Fotografías de las Mascotas](#3-detalles-y-fotografías-de-las-mascotas)
    - [4. Autenticación de Usuarios](#4-autenticación-de-usuarios)
    - [5. Almacenamiento Seguro](#5-almacenamiento-seguro)
    - [6. Búsqueda y Filtros](#6-búsqueda-y-filtros)
    - [7. Comentarios](#7-comentarios)
    - [8. Notificaciones](#8-notificaciones)
    - [9. Compartir medios de contacto que están ocultos](#9-compartir-medios-de-contacto-que-están-ocultos)
  - [Fase 3: Lanzamiento y Recolección de Feedback](#fase-3-lanzamiento-y-recolección-de-feedback)
- [Características Adicionales para Desarrollos Futuros](#características-adicionales-para-desarrollos-futuros)

## Características Principales

- **Reporte de Mascotas Perdidas**: Los usuarios tienen la capacidad de reportar sus mascotas perdidas, incluyendo detalles críticos como la fecha y el lugar donde se perdieron, características físicas, y cualquier otra información que pueda facilitar su identificación y recuperación.

- **Visualización en Mapa**: Mediante la integración con Google Maps, la aplicación permite visualizar en un mapa interactivo las ubicaciones donde se han reportado mascotas perdidas, ofreciendo una herramienta potente para la búsqueda en áreas específicas.

- **Detalles y Fotografías de las Mascotas**: Para cada mascota perdida reportada, se pueden ver detalles detallados y fotografías, lo que permite a los usuarios identificar fácilmente a las mascotas y proporcionar ayuda efectiva.

## Tecnologías y Herramientas

### Aplicación Móvil

- **React Native con Expo**: Utilizado para el desarrollo de la aplicación móvil, permitiendo una experiencia de usuario fluida y responsive en diferentes dispositivos y plataformas.
- **Typescript**: Adoptado para añadir tipado estático al código, mejorando la legibilidad y mantenibilidad del código.
- **Nativewind**: Una librería que integra Tailwind CSS con React Native, facilitando el diseño de interfaces de usuario modernas y responsivas.
- **Google Maps para Geolocalización**: Integración clave para el mapeo de las ubicaciones de las mascotas perdidas, ofreciendo una herramienta de búsqueda geográfica precisa.

### Backend

- **Drizzle-orm**: Un ORM diseñado para simplificar las interacciones con bases de datos, mejorando la eficiencia del desarrollo backend.
- **Pothos y GraphQL Yoga**: Herramientas que juntas facilitan la creación de un API GraphQL eficiente, permitiendo consultas y mutaciones precisas de datos.
- **Neon (Base de Datos Serverless PostgreSQL)**: Proporciona un almacenamiento de datos escalable y de alta disponibilidad, ideal para aplicaciones modernas.
- **Redis para Caché**: Mejora la velocidad de respuesta de la aplicación almacenando temporalmente copias de los datos más solicitados.
- **Bull para Colas de Trabajo**: Gestiona tareas en segundo plano, como el procesamiento de imágenes o notificaciones, de manera eficiente y escalable.

### Otros Componentes

- **Clerk/Auth0 para Autenticación**: Se están evaluando estas plataformas para implementar un sistema de autenticación seguro y flexible, garantizando la protección de los datos de los usuarios.
- **S3 para Almacenamiento de Imágenes**: Se utiliza el servicio de almacenamiento de Amazon S3 para guardar las fotografías de las mascotas de manera segura y accesible.

## Plan de Desarrollo MVP

### Fase 1: Diseño y Prototipado

#### 1. Reporte de Mascotas Perdidas/Encontradas

- **Formulario de Reporte**: Interfaz intuitiva para ingresar la información de la mascota perdida, incluyendo nombre, especie, raza, color, características físicas distintivas, última ubicación vista, fecha de desaparición, y contacto del propietario.
- **Carga de Fotografías**: Capacidad para subir múltiples fotos de la mascota para facilitar su identificación.
- **Publicación y Gestión de Reportes**: Permitir a los usuarios gestionar sus propios reportes, actualizar información, o marcar a una mascota como encontrada.

#### 2. Visualización en Mapa

- **Mapa Interactivo**: Integración con Google Maps para mostrar las ubicaciones de las mascotas reportadas como perdidas. Cada reporte se puede visualizar como un pin en el mapa, con la posibilidad de filtrar por fecha y tipo de mascota.
- **Detalle al Seleccionar un Reporte**: Al seleccionar un reporte en el mapa, se mostrará un resumen del reporte con la opción de ver más detalles.

#### 3. Detalles y Fotografías de las Mascotas

- **Página de Detalle de la Mascota**: Para cada reporte, una página detallada que muestra toda la información de la mascota, incluyendo una galería de fotos, descripción, y datos de contacto del propietario para facilitar la comunicación.

#### 4. Autenticación de Usuarios

- **Registro e Inicio de Sesión**: Implementación de un sistema básico de autenticación que permita a los usuarios registrarse, iniciar sesión, y gestionar sus reportes de forma segura. La decisión entre Clerk y Auth0 dependerá de la evaluación de costos, facilidad de integración y funcionalidades ofrecidas.

#### 5. Almacenamiento Seguro

- **Almacenamiento de Fotos en S3**: Implementación de un sistema para cargar y almacenar de forma segura las fotos de las mascotas en el servicio de Amazon S3, asegurando la disponibilidad y el rendimiento.

#### 6. Búsqueda y Filtros

- **Búsqueda por Ubicación y Características**: Implementación de un sistema de búsqueda que permita a los usuarios filtrar los reportes por ubicación, especie, raza, color, y otras características físicas de la mascota.

#### 7. Comentarios

- **Comentarios en los Reportes**: Posibilidad para los usuarios de dejar comentarios en los reportes de mascotas perdidas, ofreciendo apoyo y consejos a los propietarios.

#### 8. Notificaciones

- **Notificaciones de Nuevos Reportes**: Implementación de un sistema de notificaciones que alerte a los usuarios cuando se publique un nuevo reporte en su área de interés.

#### 9. Compartir medios de contacto que están ocultos

- **Medios de Contacto Ocultos**: Para proteger la privacidad de los usuarios, los medios de contacto (teléfono, email) se mostrarán de forma oculta y solo estarán disponibles seg´un la interacción entre los usuarios.

#### Tecnologías y Herramientas

Para el MVP, el enfoque estará en utilizar tecnologías probadas y eficientes que permitan una rápida iteración y lanzamiento. La elección de React Native con Expo facilita el desarrollo de una aplicación móvil cross-platform, mientras que TypeScript añade un nivel adicional de seguridad y mantenibilidad al proyecto.

El backend se desarrollará con un enfoque en la escalabilidad y la eficiencia, utilizando Drizzle-orm para simplificar el acceso a datos y GraphQL para una interfaz API flexible y potente. La elección de Neon como base de datos serverless PostgreSQL ofrece una solución escalable y de alta disponibilidad desde el inicio.

#### Estrategia de Lanzamiento y Feedback

El lanzamiento del MVP se acompañará de una estrategia de comunicación enfocada en alcanzar a los dueños de mascotas a través de redes sociales y colaboraciones con organizaciones de animales. La recopilación activa de feedback será crucial durante esta fase para identificar rápidamente áreas de mejora y validar la propuesta de valor de la aplicación.

### Fase 2: Lanzamiento y Recolección de Feedback

- **Despliegue de la Aplicación**: Publicación de la aplicación en las tiendas de aplicaciones móviles, asegurando que cumple con todas las directrices y requisitos de publicación.

- **Marketing y Difusión**: Implementación de estrategias de marketing para promover la aplicación dentro de la comunidad de dueños de mascotas, incluyendo redes sociales, colaboraciones con refugios de animales, y eventos locales.

- **Recolección y Análisis de Feedback**: Establecimiento de canales de comunicación con los usuarios para recoger sus opiniones y sugerencias, y análisis de este feedback para identificar áreas de mejora.

### Características Adicionales para Desarrollos Futuros

1. **Notificaciones Push**: Para informar a los usuarios sobre mascotas perdidas en su área o actualizaciones sobre sus reportes.
2. **Sistema de Recompensas**: Incentivar la participación de la comunidad a través de recompensas por acciones que ayuden a reunir mascotas perdidas con sus dueños.
3. **Integración con Redes Sociales**: Permitir la difusión de los reportes de mascotas perdidas en plataformas de redes sociales para aumentar el alcance.
4. **Funcionalidades de Realidad Aumentada**: Explorar el uso de realidad aumentada para visualizar en el entorno real la última ubicación conocida de una mascota perdida.
5. **Sistema de Verificación de Usuarios**: Implementar mecanismos de verificación para aumentar la confianza en los reportes y perfiles.
