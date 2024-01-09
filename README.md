# Aplicación de Renting de Vehículos

Esta aplicación permite gestionar los vehículos de una empresa de renting, almacenando información como marca, modelo y precio de alquiler en una base de datos. Además, proporciona funcionalidades para buscar vehículos según diferentes criterios.

## Configuración del Proyecto

### Requisitos

- JDK 11 o superior
- Maven
- Node.js (para la parte del cliente)

### Configuración del Backend

1. Clona este repositorio:
   ```bash
   git clone https://github.com/TuUsuario/renting-api.git
   ```

2. Abre el proyecto del backend en tu IDE de preferencia.

3. Ejecuta la aplicación Spring Boot.

### Configuración del Cliente

1. Abre la carpeta `client` en tu editor de código.

2. Instala las dependencias:
   ```bash
   npm install
   ```

3. Inicia la aplicación de cliente:
   ```bash
   npm start
   ```

4. Accede a la aplicación de cliente en `http://localhost:3000`.

## Endpoints del Backend

### Guardar Vehículos (POST)

- Guarda un nuevo vehículo en la base de datos.

   **Endpoint:**
   ```
   POST /api/vehiculo
   ```

   **Ejemplo de Payload:**
   ```json
   {
     "marca": "Toyota",
     "modelo": "Corolla",
     "precioAlquiler": 50.0
   }
   ```

### Buscar por Marca (GET)

- Busca vehículos por la marca especificada.

   **Endpoint:**
   ```
   GET /api/vehiculo/by-marca/{marca}
   ```

### Buscar por Modelo (GET)

- Busca vehículos por el modelo especificado.

   **Endpoint:**
   ```
   GET /api/vehiculo/by-modelo/{modelo}
   ```

### Buscar por Marca y Modelo (GET)

- Busca vehículos por la marca y modelo especificados.

   **Endpoint:**
   ```
   GET /api/vehiculo/{marca}/{modelo}
   ```

### Buscar Precios Inferiores (GET)

- Busca precios de alquiler de vehículos inferiores al precio especificado.

   **Endpoint:**
   ```
   GET /api/vehiculo/less-than/{precio}
   ```

### Calcular Importe Total (GET)

- Calcula el importe total de alquiler en función de los días.

   **Endpoint:**
   ```
   GET /api/vehiculo/importe-total/{precio}/{dias}
   ```

   **Ejemplo de Uso:**
   ```
   GET /api/vehiculo/importe-total/50.0/7
   ```

Este proyecto proporciona una solución integral para la gestión de vehículos de una empresa de renting, con un backend robusto y una interfaz de usuario interactiva en el cliente. ¡Explora las funcionalidades y gestiona los vehículos de manera eficiente!
