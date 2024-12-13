
# FleetManager

## Descripción

FleetManager es una aplicación para la gestión de flotas de vehículos, incluyendo la administración de escuelas de manejo, profesores y vehículos.

## Tecnologías Utilizadas

- Java
- Spring Boot
- Hibernate
- REST API

## Endpoints

### DrivingSchoolsController

1. **Get Driving Schools**
   - **Endpoint**: `GET /v1/driving_schools/`
   - **Descripción**: Obtiene una lista de todas las escuelas de manejo.
   - **Respuesta**: `Result<List<DrivingSchool>>`

2. **Add Driving School**
   - **Endpoint**: `POST /v1/driving_schools/`
   - **Descripción**: Agrega una nueva escuela de manejo.
   - **Cuerpo de la solicitud**: `AddDrivingSchoolDTO`
   - **Respuesta**: `Result<DrivingSchool>`

3. **Open Driving School Section**
   - **Endpoint**: `POST /v1/driving_schools/{id}/sections`
   - **Descripción**: Abre una nueva sección en una escuela de manejo específica.
   - **Parámetro de ruta**: `id` (identificador de la escuela de manejo)
   - **Cuerpo de la solicitud**: `OpenSectionDTO`
   - **Respuesta**: `Result<Section>`

### TeachersController

1. **Get All Teachers**
   - **Endpoint**: `GET /v1/teachers/`
   - **Descripción**: Obtiene una lista de todos los profesores.
   - **Respuesta**: `Result<List<Teacher>>`

2. **Hire Teacher**
   - **Endpoint**: `POST /v1/teachers/`
   - **Descripción**: Contrata a un nuevo profesor.
   - **Cuerpo de la solicitud**: `HireTeacherDTO`
   - **Respuesta**: `Result<Teacher>`

3. **Fire Teacher**
   - **Endpoint**: `POST /v1/teachers/fire`
   - **Descripción**: Despide a un profesor.
   - **Cuerpo de la solicitud**: `FireTeacherDTO`
   - **Respuesta**: `Result<Void>`

### VehiclesController

1. **Find All Vehicles**
   - **Endpoint**: `GET /v1/vehicles/`
   - **Descripción**: Obtiene una lista de todos los vehículos.
   - **Respuesta**: `Result<List<Vehicle>>`

2. **Associate Vehicle**
   - **Endpoint**: `POST /v1/vehicles/associate/`
   - **Descripción**: Asocia un vehículo a un profesor o entidad.
   - **Cuerpo de la solicitud**: `AssociateVehicleDTO`
   - **Respuesta**: `Result<Void>`

3. **Buy Vehicle**
   - **Endpoint**: `POST /v1/vehicles/`
   - **Descripción**: Compra un nuevo vehículo.
   - **Cuerpo de la solicitud**: `BuyVehicleDTO`
   - **Respuesta**: `Result<Vehicle>`

## Instalación

1. Clona el repositorio:
   ```sh
   git clone https://github.com/josericardopenase/fleet_management_ddd.git
   ```
2. Navega al directorio del proyecto:
   ```sh
   cd fleet_management_ddd
   ```
3. Compila el proyecto:
   ```sh
   ./mvnw clean install
   ```

## Uso

1. Inicia la aplicación:
   ```sh
   ./mvnw spring-boot:run
   ```

2. Accede a la API a través de `http://localhost:8080`.

## Contribución

Las contribuciones son bienvenidas. Por favor, sigue los siguientes pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza tus cambios y haz commit (`git commit -am 'Agrega nueva funcionalidad'`).
4. Sube los cambios a tu rama (`git push origin feature/nueva-funcionalidad`).
5. Abre un Pull Request.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

