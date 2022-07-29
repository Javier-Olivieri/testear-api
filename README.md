# Trabajo Final Coderhouse Comisión 20645

Aplicación eCommerce Backend que implementa un servidor de aplicación basado en la plataforma Node.js 
y el módulo express.

## Base routes

## Producto: /api/productos

#### GET: '/' 
Lista todos los productos disponibles.
#### GET: '/:id' 
Muestra un producto por su id (disponible para usuarios y administradores).
#### POST: '/' 
Para incorporar productos al listado (disponible para administradores).
#### PUT: '/:id' 
Actualiza un producto por su id (disponible para administradores).
#### DELETE: '/:id' 
Borra un producto por su id (disponible para administradores).

## Carrito: /api/carrito

#### POST: '/' 
Crea un carrito y devuelve su id.
#### DELETE: '/:id' 
Vacía un carrito y lo elimina.
#### GET: '/:id/productos' 
Me permite listar todos los productos guardados en el carrito.
#### POST: '/:id/productos/:id_prod' 
Para incorporar productos al carrito por su id de carrito y de producto.
#### DELETE: '/:id/productos/:id_prod' 
Eliminar un producto del carrito por su id de carrito y de producto.

## Usuario /api/usuario

#### POST: '/registro'
Registra un nuevo usuario guardando su informacion en BD. Se envía un email al admin con los datos del nuevo cliente.
#### POST: '/login' 
Realiza autenticación de un usuario ya registrado.
#### GET: '/loginsuccess'
Ruta a la que se redirecciona cuando el login fue exitoso.
#### GET: '/loginerror'
Ruta a la que se redirecciona cuando el login falla.
#### GET: '/logout'
Finaliza la sesión del usuario.
#### GET: '/sessionstatus'
Checkea si el usuario está autenticado.

## Checkout /api/checkout

#### POST: '/:id_cart'
Este endpoint a traves del id de carrito pasado por param y de información del cliente pasado por body se encarga de enviar un mail con la información de la compra, un sms y un whatsapp.