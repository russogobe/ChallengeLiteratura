# ChallengeLiteratura

## Descripción
**ChallengeLiteratura** es una aplicación que permite gestionar un catálogo de libros, interactuar con datos de autores y libros, y obtener estadísticas útiles sobre la literatura. La aplicación permite realizar búsquedas, ver los libros más descargados, filtrar por idioma, y más. Todo esto se conecta con una API externa que facilita la obtención de datos de libros y autores.

## Características principales

- **Buscar libros por título**: Permite encontrar libros por su título, mostrando información relevante como autor, idioma y descargas.
- **Listar todos los libros**: Muestra un listado completo de todos los libros en la base de datos.
- **Top 10 libros más descargados**: Obtiene y muestra los 10 libros más descargados.
- **Buscar título por nombre de autor**: Permite buscar libros asociados a un autor específico.
- **Estadísticas de libros por idioma**: Muestra la cantidad de libros disponibles para cada idioma.
- **Listar autores vivos en un año específico**: Filtra autores que estuvieron vivos en un año determinado.

## Tecnologías utilizadas

- **Spring Boot**: Framework utilizado para construir la API y la lógica de negocio.
- **Java 17**: Lenguaje de programación utilizado para desarrollar la aplicación.
- **JPA (Java Persistence API)**: Para gestionar la base de datos con consultas eficientes.
- **RestTemplate**: Para obtener datos externos desde la API de libros "Gutendex".
- **PostgreSQL**: Base de datos relacional donde se almacenan los libros y autores.

## Estructura del Proyecto

- **`Principal.java`**: Contiene la interfaz de usuario, que permite interactuar con las funcionalidades principales de la aplicación a través de un menú de texto.
- **`LibroService.java`**: Servicio que gestiona la lógica de negocio relacionada con los libros, incluyendo la consulta a la API externa.
- **`LibroRepository.java`**: Interfaz que extiende `JpaRepository`, facilitando las consultas y operaciones CRUD en la base de datos.
- **`AutorRepository.java`**: Interfaz que extiende `JpaRepository`, gestionando las operaciones CRUD para autores.
- **`Libro.java`** y **`Autor.java`**: Modelos de datos que representan los libros y autores en la base de datos.

## Instalación

1. **Clona el repositorio:**
   ```bash
   git clone https://github.com/tuusuario/Challenge-Literatura.git
   ```

2. **Compila el proyecto**:
   Si estás utilizando Maven:
   ```bash
   mvn clean install
   ```

3. **Configura la base de datos**:
   Asegúrate de tener PostgreSQL corriendo y configura las credenciales en el archivo `application.properties`:
   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/nombre_base_de_datos
   spring.datasource.username=usuario
   spring.datasource.password=contraseña
   spring.jpa.hibernate.ddl-auto=update
   ```

4. **Ejecuta la aplicación**:
   ```bash
   mvn spring-boot:run
   ```

5. **Accede a la aplicación** a través del terminal, donde podrás interactuar con el menú.

## Contribuciones

¡Contribuciones son bienvenidas! Si tienes alguna sugerencia, reporte de error o mejora, siéntete libre de abrir un **issue** o enviar un **pull request**.

## Licencia

Este proyecto está bajo la **MIT License**.

---

¡Gracias por explorar **ChallengeLiteratura**! Disfruta gestionando libros y autores de manera sencilla y eficiente. 🚀📚
