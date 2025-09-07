# AuthService - Order Management System

Microservicio de **autenticación y autorización** basado en Spring Boot y JWT.  
Forma parte del sistema **Order Management System**.

---

## Tecnologías
- Java 17
- Spring Boot 3
- Spring Security + JWT
- Spring Data JPA
- MySQL
- OpenFeign (para comunicación con otros microservicios)

---

##  Funcionalidad
- Registro de usuarios (`/api/auth/register`)
- Inicio de sesión (`/api/auth/login`)
- Generación y validación de **tokens JWT**
- Seguridad centralizada para proteger los demás microservicios

---

##  Estructura de Paquetes
com.ordermanagement.authservice
┣ 📂controller → Endpoints REST (AuthController)
┣ 📂service → Lógica de negocio (AuthService)
┣ 📂repository → Acceso a base de datos (UserRepository)
┣ 📂model → Entidades JPA (User)
┣ 📂dto → Objetos de transferencia (LoginRequestDTO, RegisterRequestDTO, AuthResponseDTO)
┣ 📂security → Seguridad con JWT (JwtUtil, JwtAuthenticationFilter, SecurityConfig, CustomUserDetailsService)
