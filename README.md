# Renting - API

La **RentingVehiculosApp API** es un servicio que permite gestionar los vehículos de una empresa de renting. Permite realizar operaciones de guardar, buscar y calcular importes de alquiler.

## Configuración del Proyecto

1. Clona este repositorio:

   ```bash
   git clone https://github.com/TuUsuario/renting-api.git
   ```

2. Abre el proyecto en tu entorno de desarrollo preferido.

3. Ejecuta la aplicación Spring Boot.

La API estará disponible en `http://localhost:8080`.

## Endpoints

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

## Notas Adicionales

- Asegúrate de tener una base de datos configurada correctamente. La aplicación utiliza la base de datos `tecnocom` y la tabla `clientes`. Ajusta la configuración según sea necesario.

- Este proyecto está configurado para ser utilizado como una API independiente en el backend de una aplicación más grande. Asegúrate de integrarlo correctamente en tu proyecto global.

¡Explora los endpoints y gestiona eficientemente los vehículos en tu empresa de renting con la RentingVehiculosApp API!
