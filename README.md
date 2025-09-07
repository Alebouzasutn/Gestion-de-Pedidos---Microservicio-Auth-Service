# AuthService - Order Management System

Microservicio de **autenticación y autorización** basado en Spring Boot y JWT.  
Forma parte del sistema **Order Management System**.

**Función principal: autenticar y registrar usuarios, emitir tokens.**

- Entradas: datos de registro (username, email, password) o login (username, password) desde el frontend.

- Salidas: JWT válido o error de autenticación.

Cómo afecta a los otros microservicios:

Todos los requests a orderservice y productservice requieren que el frontend envíe un JWT generado por authservice.

Otros microservicios no conocen la contraseña ni gestionan usuarios, solo confían en el JWT.

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
