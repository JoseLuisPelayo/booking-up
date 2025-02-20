# Sistema de Reservas con Laravel

¡Bienvenido al repositorio del Sistema de Reservas desarrollado con Laravel! Este proyecto es una aplicación web que permite a los usuarios realizar reservas en diferentes negocios, gestionar sus créditos, y visualizar sus reservas y slots disponibles.

## Lo que Aprenderás

Este proyecto cubre los siguientes aspectos clave:

- **Modelado de Datos**: Diseño y modelado de la base de datos para el sistema de reservas, incluyendo entidades como negocios, horarios, usuarios y reservas.
  
- **Negocios y Horarios**: Implementación de la lógica para gestionar negocios, definir horarios de apertura/cierre, y especificar los días de disponibilidad.

- **Generación de Slots de Reserva**: Desarrollo de un comando personalizado para generar slots de reserva basados en las franjas horarias definidas para cada negocio.

- **Créditos de Usuario**: Implementación de un sistema de créditos que permite a los usuarios realizar reservas solo si tienen suficientes créditos disponibles.

- **Funcionalidad de Reserva y Cancelación**: Lógica para que los usuarios puedan realizar y cancelar reservas.

- **Visualización de Reservas**: Interfaz para que los usuarios puedan ver sus reservas activas.

- **Visualización de Slots Disponibles**: Sistema para que los usuarios puedan visualizar los slots disponibles filtrando por año, mes, día y negocio.

## Requisitos Previos

Antes de comenzar, asegúrate de tener instalado lo siguiente:

- PHP >= 8.0
- Composer
- MySQL
- Laravel CLI
- Node.js y NPM (para compilar assets)

## Instalación

Sigue estos pasos para configurar el proyecto en tu máquina local:

1. **Clona el repositorio**:
   ```
   git clone https://github.com/tu-usuario/sistema-reservas-laravel.git
   cd sistema-reservas-laravel
   ```
2. Instala las dependencias de Composer: 

`composer install` 
 3. Instala las dependencias de NPM: 
 `npm install` 
 4. Copia el archivo .env.example a .env: 
`cp .env.example .env` 
 4. Genera una clave de aplicación: 
`php artisan key:generate` 
 5. Configura la base de datos: 
 Crea una base de datos MySQL para el proyecto. 
 Actualiza el archivo .env con las credenciales de tu base de datos: 
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nombre_de_tu_base_de_datos
DB_USERNAME=tu_usuario
DB_PASSWORD=tu_contraseña
```
6. Ejecuta las migraciones y seeders: 
`php artisan migrate --seed` 
7. Compila los assets:
`npm run dev` 
8. Inicia el servidor de desarrollo: 
`php artisan serve` 
9. Accede a la aplicación: 
Abre tu navegador y visita http://localhost:8000.

 - Uso 
	- Generación de Slots de Reserva 
		Para generar los slots de reserva, ejecuta el siguiente comando:

		`php artisan generate:reservation-slots` 
		Este comando generará los slots de reserva basados en los horarios definidos para cada negocio. 

	- Realizar una Reserva 
	Inicia sesión como usuario.  

	Navega hasta la página de un negocio. 

	Selecciona un slot disponible y realiza la reserva. 

	- Cancelar una Reserva 
		Ve a la sección "Mis Reservas". 
		Selecciona la reserva que deseas cancelar y haz clic en "Cancelar". 

	- Visualización de Slots Disponibles
		Puedes filtrar los slots disponibles por año, mes, día y negocio en la página de búsqueda de slots.

- Contribución
	- Si deseas contribuir a este proyecto, sigue estos pasos:

	- Haz un fork del repositorio.

	- Crea una nueva rama (git checkout -b feature/nueva-funcionalidad).

	- Realiza tus cambios y haz commit (git commit -am 'Añade nueva funcionalidad').

	- Haz push a la rama (git push origin feature/nueva-funcionalidad).

	- Abre un Pull Request.
