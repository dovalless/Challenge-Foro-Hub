# 🎓 ForoHub - API REST para Foros de Discusión

<div align="center">

**API REST Spring Boot - Sistema de Gestión de Tópicos en Foros**

[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Java](https://img.shields.io/badge/Java-11%2B-007396?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![Spring Security](https://img.shields.io/badge/Spring_Security-6.x-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)](https://spring.io/projects/spring-security)
[![MySQL](https://img.shields.io/badge/MySQL-8.x-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

[🚀 Características](#-características) • 
[🛠️ Stack Tecnológico](#️-stack-tecnológico) • 
[⚙️ Instalación](#️-instalación-y-ejecución) • 
[📚 API Endpoints](#️-api-endpoints) • 
[🔐 Seguridad](#️-autenticación-y-autorización) • 
[🧪 Validaciones](#️-validaciones) • 
[👨‍💻 Autor](#️-autor)

</div>

---

## 📋 Descripción del Proyecto
**ForoHub** es una API REST desarrollada con **Spring Framework** para gestionar un sistema completo de foros de discusión. La aplicación permite realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar) sobre tópicos, implementando validaciones de negocio, autenticación/autorización de usuarios y persistencia en bases de datos relacionales.

### 🎯 Objetivos del Proyecto
- Implementar una API RESTful siguiendo las mejores prácticas
- Gestionar tópicos de discusión con operaciones CRUD completas
- Asegurar la aplicación mediante Spring Security
- Validar reglas de negocio y datos de entrada
- Proporcionar una base sólida para sistemas de foros escalables

### 💼 Casos de Uso
- **Foros educativos:** Discusiones en cursos online
- **Comunidades técnicas:** Soporte y discusión entre desarrolladores  
- **Foros empresariales:** Comunicación interna departamental
- **Plataformas de debate:** Discusiones temáticas organizadas

---

## 🚀 Características

### 📝 Gestión Completa de Tópicos
| Operación | Descripción | Método HTTP |
|-----------|-------------|-------------|
| **Crear** | Publicar nuevo tópico con título y mensaje | `POST /api/topics` |
| **Listar** | Obtener todos los tópicos con paginación | `GET /api/topics` |
| **Consultar** | Obtener detalles de un tópico específico | `GET /api/topics/{id}` |
| **Actualizar** | Modificar título y contenido de un tópico | `PUT /api/topics/{id}` |
| **Eliminar** | Remover tópico del sistema (soft/hard delete) | `DELETE /api/topics/{id}` |

### 🛡️ Características de Seguridad
- ✅ Autenticación basada en JWT (JSON Web Tokens)
- ✅ Autorización por roles (USER, ADMIN, MODERATOR)
- ✅ Protección contra ataques CSRF
- ✅ Rate limiting para prevenir abusos
- ✅ Encriptación de contraseñas (BCrypt)

### 📊 Características Técnicas
- **Arquitectura:** RESTful API con controladores por separación de concerns
- **Persistencia:** Capa de datos con Spring Data JPA y Hibernate
- **Validación:** Bean Validation con mensajes personalizados
- **Documentación:** OpenAPI/Swagger para documentación automática
- **Testing:** Suite completa de tests unitarios e integración

---

## 🛠️ Stack Tecnológico

### 🔧 Backend
| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| **Java** | 11+ | Lenguaje principal de desarrollo |
| **Spring Boot** | 3.x | Framework principal de la aplicación |
| **Spring Data JPA** | 3.x | Abstracción para persistencia de datos |
| **Spring Security** | 6.x | Autenticación y autorización |
| **Hibernate** | 6.x | ORM para mapeo objeto-relacional |
| **Maven** | 3.8+ | Gestión de dependencias y build |

### 🗄️ Base de Datos
| Base de Datos | Entorno | Propósito |
|---------------|---------|-----------|
| **H2 Database** | Desarrollo/Pruebas | Base de datos en memoria para testing |
| **MySQL** | Producción | Base de datos relacional para producción |
| **Flyway/Liquibase** | Todos | Migraciones de base de datos |

### 🧪 Testing y Calidad
| Herramienta | Propósito |
|-------------|-----------|
| **JUnit 5** | Testing unitario y de integración |
| **Mockito** | Mocking de dependencias |
| **Spring Boot Test** | Testing de contexto Spring |
| **Jacoco** | Cobertura de código |
| **Postman/Insomnia** | Testing de endpoints API |

### 📦 Dependencias Principales
```xml
<dependencies>
    <!-- Spring Boot Starters -->
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-security</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-validation</artifactId>
    </dependency>
    
    <!-- Base de Datos -->
    <dependency>
        <groupId>com.h2database</groupId>
        <artifactId>h2</artifactId>
        <scope>runtime</scope>
    </dependency>
    <dependency>
        <groupId>com.mysql</groupId>
        <artifactId>mysql-connector-j</artifactId>
        <scope>runtime</scope>
    </dependency>
    
    <!-- Utilities -->
    <dependency>
        <groupId>io.jsonwebtoken</groupId>
        <artifactId>jjwt-api</artifactId>
        <version>0.11.5</version>
    </dependency>
</dependencies>
```

---

## ⚙️ Instalación y Ejecución

### ✅ Prerrequisitos
- **Java JDK 11 o superior** ([Descargar](https://www.oracle.com/java/technologies/downloads/))
- **Apache Maven 3.8+** ([Descargar](https://maven.apache.org/download.cgi))
- **MySQL 8.x** (para entorno de producción)
- **Git** ([Descargar](https://git-scm.com/downloads))

### 📥 Clonar el Repositorio
```bash
# Clonar el repositorio
git clone https://github.com/dovalless/ForoHub.git
cd ForoHub

# Verificar estructura del proyecto
ls -la
```

### 🔧 Configuración del Proyecto

#### 1. Configuración para Desarrollo (H2 Database)
```properties
# src/main/resources/application-dev.properties
spring.datasource.url=jdbc:h2:mem:forohubdb
spring.datasource.username=sa
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console
```

#### 2. Configuración para Producción (MySQL)
```properties
# src/main/resources/application-prod.properties
spring.datasource.url=jdbc:mysql://localhost:3306/forohub?useSSL=false&serverTimezone=UTC
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=validate
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
```

#### 3. Variables de Entorno Recomendadas
```bash
# .env file (opcional)
DB_HOST=localhost
DB_PORT=3306
DB_NAME=forohub
DB_USER=forohub_user
DB_PASS=StrongPassword123!
JWT_SECRET=YourSuperSecretKeyForJWT12345
```

### 🚀 Compilar y Ejecutar

#### Opción 1: Usando Maven Wrapper
```bash
# Compilar el proyecto
./mvnw clean compile

# Ejecutar tests
./mvnw test

# Ejecutar en modo desarrollo
./mvnw spring-boot:run -Dspring-boot.run.profiles=dev

# Construir JAR ejecutable
./mvnw clean package

# Ejecutar JAR
java -jar target/forohub-0.0.1-SNAPSHOT.jar
```

#### Opción 2: Usando Docker
```dockerfile
# Dockerfile
FROM openjdk:11-jre-slim
COPY target/forohub-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/app.jar"]
```

```bash
# Construir imagen Docker
docker build -t forohub-api .

# Ejecutar contenedor
docker run -p 8080:8080 -e "SPRING_PROFILES_ACTIVE=prod" forohub-api
```

#### Opción 3: Usando IDE (IntelliJ IDEA/Eclipse)
1. Importar como proyecto Maven
2. Configurar JDK 11+
3. Ejecutar la clase principal `ForoHubApplication.java`
4. Acceder a `http://localhost:8080`

### 🧪 Verificar Instalación
```bash
# Verificar que la aplicación está corriendo
curl http://localhost:8080/api/health

# Salida esperada
{"status":"UP","timestamp":"2024-01-15T10:30:00Z"}
```

---

## 📚 API Endpoints

### 🔐 Autenticación
| Método | Endpoint | Descripción | Autenticación Requerida |
|--------|----------|-------------|-------------------------|
| `POST` | `/api/auth/register` | Registrar nuevo usuario | No |
| `POST` | `/api/auth/login` | Iniciar sesión (obtener JWT) | No |
| `POST` | `/api/auth/refresh` | Refrescar token JWT | Sí |
| `POST` | `/api/auth/logout` | Cerrar sesión | Sí |

### 📝 Gestión de Tópicos
| Método | Endpoint | Descripción | Roles Permitidos |
|--------|----------|-------------|------------------|
| `POST` | `/api/topics` | Crear nuevo tópico | USER, ADMIN, MODERATOR |
| `GET` | `/api/topics` | Listar todos los tópicos (paginado) | USER, ADMIN, MODERATOR |
| `GET` | `/api/topics/{id}` | Obtener tópico por ID | USER, ADMIN, MODERATOR |
| `PUT` | `/api/topics/{id}` | Actualizar tópico existente | OWNER, ADMIN, MODERATOR |
| `DELETE` | `/api/topics/{id}` | Eliminar tópico (soft delete) | OWNER, ADMIN, MODERATOR |
| `GET` | `/api/topics/search` | Buscar tópicos por criterios | USER, ADMIN, MODERATOR |

### 👥 Gestión de Usuarios
| Método | Endpoint | Descripción | Roles Permitidos |
|--------|----------|-------------|------------------|
| `GET` | `/api/users/profile` | Obtener perfil del usuario actual | USER, ADMIN, MODERATOR |
| `PUT` | `/api/users/profile` | Actualizar perfil de usuario | USER, ADMIN, MODERATOR |
| `GET` | `/api/users/{id}` | Obtener usuario por ID (admin only) | ADMIN |
| `GET` | `/api/users` | Listar todos los usuarios | ADMIN |

### 📊 Ejemplos de Uso

#### 1. Crear Nuevo Tópico
```http
POST /api/topics
Authorization: Bearer {jwt_token}
Content-Type: application/json

{
    "titulo": "¿Cuál es el mejor framework para APIs REST?",
    "mensaje": "Estoy evaluando opciones para mi próximo proyecto...",
    "categoria": "TECNOLOGIA",
    "etiquetas": ["java", "spring", "api"]
}
```

**Respuesta Exitosa (201 Created):**
```json
{
    "id": 1,
    "titulo": "¿Cuál es el mejor framework para APIs REST?",
    "mensaje": "Estoy evaluando opciones para mi próximo proyecto...",
    "autor": {
        "id": 1,
        "nombre": "Juan Pérez",
        "email": "juan@example.com"
    },
    "categoria": "TECNOLOGIA",
    "etiquetas": ["java", "spring", "api"],
    "fechaCreacion": "2024-01-15T10:30:00Z",
    "fechaActualizacion": "2024-01-15T10:30:00Z",
    "estado": "ACTIVO"
}
```

#### 2. Obtener Tópico por ID
```http
GET /api/topics/1
Authorization: Bearer {jwt_token}
```

**Respuesta Exitosa (200 OK):**
```json
{
    "id": 1,
    "titulo": "¿Cuál es el mejor framework para APIs REST?",
    "mensaje": "Estoy evaluando opciones para mi próximo proyecto...",
    "autor": {
        "id": 1,
        "nombre": "Juan Pérez",
        "email": "juan@example.com"
    },
    "categoria": "TECNOLOGIA",
    "etiquetas": ["java", "spring", "api"],
    "respuestas": [
        {
            "id": 1,
            "mensaje": "Yo recomiendo Spring Boot por...",
            "autor": {
                "id": 2,
                "nombre": "María García",
                "email": "maria@example.com"
            },
            "fechaCreacion": "2024-01-15T11:30:00Z"
        }
    ],
    "fechaCreacion": "2024-01-15T10:30:00Z",
    "fechaActualizacion": "2024-01-15T10:30:00Z",
    "estado": "ACTIVO",
    "vistas": 150,
    "likes": 25
}
```

#### 3. Listar Tópicos con Paginación
```http
GET /api/topics?page=0&size=10&sort=fechaCreacion,desc&categoria=TECNOLOGIA
Authorization: Bearer {jwt_token}
```

**Respuesta Exitosa (200 OK):**
```json
{
    "content": [
        {
            "id": 1,
            "titulo": "¿Cuál es el mejor framework para APIs REST?",
            "autor": "Juan Pérez",
            "categoria": "TECNOLOGIA",
            "fechaCreacion": "2024-01-15T10:30:00Z",
            "respuestasCount": 15,
            "vistas": 150
        }
    ],
    "pageable": {
        "pageNumber": 0,
        "pageSize": 10,
        "sort": {
            "sorted": true,
            "unsorted": false,
            "empty": false
        }
    },
    "totalElements": 1,
    "totalPages": 1,
    "last": true,
    "size": 10,
    "number": 0,
    "sort": {
        "sorted": true,
        "unsorted": false,
        "empty": false
    },
    "numberOfElements": 1,
    "first": true,
    "empty": false
}
```

---

## 🔐 Autenticación y Autorización

### 🎯 Flujo de Autenticación JWT
```
1. Cliente envía credenciales → /api/auth/login
2. Servidor valida credenciales y genera JWT
3. Cliente incluye JWT en header Authorization: Bearer {token}
4. Servidor valida JWT en cada request protegido
5. Spring Security valida autorizaciones basadas en roles
```

### 🔑 Registro de Usuario
```http
POST /api/auth/register
Content-Type: application/json

{
    "nombre": "Darwin Ovalles",
    "email": "darwin@example.com",
    "password": "SecurePass123!",
    "confirmPassword": "SecurePass123!"
}
```

### 🔐 Login y Obtención de Token
```http
POST /api/auth/login
Content-Type: application/json

{
    "email": "darwin@example.com",
    "password": "SecurePass123!"
}
```

**Respuesta Exitosa:**
```json
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
    "type": "Bearer",
    "expiresIn": 3600,
    "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
    "usuario": {
        "id": 1,
        "nombre": "Darwin Ovalles",
        "email": "darwin@example.com",
        "roles": ["USER"]
    }
}
```

### 🛡️ Configuración de Seguridad
```java
@Configuration
@EnableWebSecurity
public class SecurityConfig {
    
    @Bean
    public SecurityFilterChain filterChain(HttpSecurity http) throws Exception {
        http
            .csrf(csrf -> csrf.disable())
            .sessionManagement(session -> session.sessionCreationPolicy(SessionCreationPolicy.STATELESS))
            .authorizeHttpRequests(auth -> auth
                .requestMatchers("/api/auth/**").permitAll()
                .requestMatchers("/api/topics/**").hasAnyRole("USER", "ADMIN", "MODERATOR")
                .requestMatchers("/api/admin/**").hasRole("ADMIN")
                .anyRequest().authenticated()
            )
            .addFilterBefore(jwtAuthenticationFilter, UsernamePasswordAuthenticationFilter.class);
        
        return http.build();
    }
}
```

### 👥 Roles y Permisos
| Rol | Permisos |
|-----|----------|
| **USER** | Crear/leer/actualizar sus propios tópicos |
| **MODERATOR** | Todos permisos USER + moderar tópicos de otros |
| **ADMIN** | Todos permisos + gestión de usuarios y sistema |

---

## 🧪 Validaciones

### ✅ Validaciones de Entrada
```java
public class TopicRequestDTO {
    
    @NotBlank(message = "El título es obligatorio")
    @Size(min = 5, max = 200, message = "El título debe tener entre 5 y 200 caracteres")
    private String titulo;
    
    @NotBlank(message = "El mensaje es obligatorio")
    @Size(min = 10, max = 5000, message = "El mensaje debe tener entre 10 y 5000 caracteres")
    private String mensaje;
    
    @NotNull(message = "La categoría es obligatoria")
    private Category categoria;
    
    @Size(max = 5, message = "Máximo 5 etiquetas permitidas")
    private List<String> etiquetas;
}
```

### 🚫 Manejo de Errores
```json
{
    "timestamp": "2024-01-15T10:30:00Z",
    "status": 400,
    "error": "Bad Request",
    "message": "Error de validación",
    "path": "/api/topics",
    "errors": [
        {
            "field": "titulo",
            "message": "El título es obligatorio"
        },
        {
            "field": "mensaje", 
            "message": "El mensaje debe tener entre 10 y 5000 caracteres"
        }
    ]
}
```

### 🛡️ Códigos de Estado HTTP
| Código | Significado | Casos de Uso |
|--------|-------------|--------------|
| `200 OK` | Operación exitosa | GET, PUT exitosos |
| `201 Created` | Recurso creado | POST exitoso |
| `400 Bad Request` | Error en la solicitud | Validaciones fallidas |
| `401 Unauthorized` | No autenticado | Token inválido o expirado |
| `403 Forbidden` | No autorizado | Permisos insuficientes |
| `404 Not Found` | Recurso no encontrado | ID inexistente |
| `409 Conflict` | Conflicto de datos | Email duplicado |
| `500 Internal Server Error` | Error del servidor | Excepciones no manejadas |

---

## 🗄️ Estructura de Base de Datos

### 📊 Diagrama de Entidades
```
┌─────────────┐      ┌─────────────┐      ┌─────────────┐
│   Usuario   │      │   Tópico    │      │  Respuesta  │
├─────────────┤      ├─────────────┤      ├─────────────┤
│ id          │◄─────│ autor_id    │      │ id          │
│ nombre      │      │ id          │◄─────│ topico_id   │
│ email       │      │ titulo      │      │ autor_id    │
│ password    │      │ mensaje     │      │ mensaje     │
│ roles       │      │ categoria   │      │ fecha       │
│ activo      │      │ etiquetas   │      │ likes       │
│ fecha_reg   │      │ fecha_crea  │      └─────────────┘
└─────────────┘      │ fecha_act   │
                     │ estado      │
                     │ vistas      │
                     │ likes       │
                     └─────────────┘
```

### 🗂️ Scripts de Base de Datos
```sql
-- Crear base de datos
CREATE DATABASE IF NOT EXISTS forohub CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

-- Tabla de usuarios
CREATE TABLE usuarios (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL,
    roles VARCHAR(50) DEFAULT 'USER',
    activo BOOLEAN DEFAULT TRUE,
    fecha_registro TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Tabla de tópicos
CREATE TABLE topicos (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    titulo VARCHAR(200) NOT NULL,
    mensaje TEXT NOT NULL,
    autor_id BIGINT NOT NULL,
    categoria VARCHAR(50) NOT NULL,
    etiquetas JSON,
    fecha_creacion TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    fecha_actualizacion TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    estado VARCHAR(20) DEFAULT 'ACTIVO',
    vistas INT DEFAULT 0,
    likes INT DEFAULT 0,
    FOREIGN KEY (autor_id) REFERENCES usuarios(id) ON DELETE CASCADE
);

-- Índices para mejor performance
CREATE INDEX idx_topicos_autor ON topicos(autor_id);
CREATE INDEX idx_topicos_categoria ON topicos(categoria);
CREATE INDEX idx_topicos_fecha ON topicos(fecha_creacion);
```

---

## 🧪 Testing

### 🔬 Tests Unitarios
```java
@ExtendWith(MockitoExtension.class)
class TopicServiceTest {
    
    @Mock
    private TopicRepository topicRepository;
    
    @InjectMocks
    private TopicService topicService;
    
    @Test
    void createTopic_ValidRequest_ReturnsTopicDTO() {
        // Given
        TopicRequestDTO request = new TopicRequestDTO(
            "Test Title", 
            "Test Message", 
            Category.TECHNOLOGY
        );
        User author = new User(1L, "Test User", "test@example.com");
        
        // When
        TopicDTO result = topicService.createTopic(request, author);
        
        // Then
        assertNotNull(result);
        assertEquals("Test Title", result.getTitle());
        verify(topicRepository).save(any(Topic.class));
    }
}
```

### 🧪 Tests de Integración
```java
@SpringBootTest
@AutoConfigureMockMvc
class TopicControllerIntegrationTest {
    
    @Autowired
    private MockMvc mockMvc;
    
    @Test
    @WithMockUser(username = "test@example.com", roles = {"USER"})
    void createTopic_ValidRequest_ReturnsCreated() throws Exception {
        // Given
        String requestBody = """
            {
                "titulo": "Integration Test Topic",
                "mensaje": "This is an integration test message",
                "categoria": "TECHNOLOGY"
            }
            """;
        
        // When & Then
        mockMvc.perform(post("/api/topics")
                .contentType(MediaType.APPLICATION_JSON)
                .content(requestBody))
                .andExpect(status().isCreated())
                .andExpect(jsonPath("$.titulo").value("Integration Test Topic"));
    }
}
```

### 📊 Cobertura de Tests
```bash
# Ejecutar tests con cobertura
./mvnw clean test jacoco:report

# Ver reporte de cobertura
open target/site/jacoco/index.html
```

---

## 🚀 Deployment

### ☁️ Opciones de Despliegue

#### 1. Docker Compose (Local/Desarrollo)
```yaml
# docker-compose.yml
version: '3.8'
services:
  mysql:
    image: mysql:8.0
    environment:
      MYSQL_ROOT_PASSWORD: rootpassword
      MYSQL_DATABASE: forohub
      MYSQL_USER: forohub_user
      MYSQL_PASSWORD: forohub_pass
    ports:
      - "3306:3306"
    volumes:
      - mysql_data:/var/lib/mysql
  
  app:
    build: .
    environment:
      SPRING_DATASOURCE_URL: jdbc:mysql://mysql:3306/forohub
      SPRING_DATASOURCE_USERNAME: forohub_user
      SPRING_DATASOURCE_PASSWORD: forohub_pass
      SPRING_PROFILES_ACTIVE: prod
    ports:
      - "8080:8080"
    depends_on:
      - mysql

volumes:
  mysql_data:
```

#### 2. AWS Elastic Beanstalk
```bash
# Crear aplicación
eb init -p java-11 forohub-api --region us-east-1

# Configurar entorno
eb create forohub-prod \
  --envvars SPRING_PROFILES_ACTIVE=prod \
  --database \
  --database.engine mysql \
  --database.username forohub_user \
  --database.password $(openssl rand -base64 12)

# Desplegar
eb deploy
```

#### 3. Google Cloud Run
```bash
# Construir imagen
gcloud builds submit --tag gcr.io/your-project/forohub-api

# Desplegar en Cloud Run
gcloud run deploy forohub-api \
  --image gcr.io/your-project/forohub-api \
  --platform managed \
  --region us-central1 \
  --allow-unauthenticated \
  --set-env-vars="SPRING_PROFILES_ACTIVE=prod"
```

### 📈 Monitoreo y Logs
```yaml
# application-monitoring.yml
management:
  endpoints:
    web:
      exposure:
        include: health,info,metrics,prometheus
  metrics:
    export:
      prometheus:
        enabled: true
  tracing:
    sampling:
      probability: 1.0

logging:
  level:
    com.forohub: DEBUG
  file:
    name: logs/forohub-api.log
  logback:
    rollingpolicy:
      max-file-size: 10MB
      max-history: 30
```

---

## 🤝 Contribuir

### 🎯 Guía de Contribución
1. **Fork el repositorio**
   ```bash
   git clone https://github.com/dovalless/ForoHub.git
   ```

2. **Crear rama de feature**
   ```bash
   git checkout -b feature/nueva-funcionalidad
   ```

3. **Realizar cambios y commits**
   ```bash
   git add .
   git commit -m "feat: agregar funcionalidad de búsqueda avanzada"
   ```

4. **Push y Pull Request**
   ```bash
   git push origin feature/nueva-funcionalidad
   ```

### 📝 Convenciones de Commits
| Tipo | Descripción | Ejemplo |
|------|-------------|---------|
| **feat** | Nueva funcionalidad | `feat: agregar autenticación JWT` |
| **fix** | Corrección de bug | `fix: resolver NPE en servicio de tópicos` |
| **docs** | Documentación | `docs: actualizar README con ejemplos` |
| **style** | Formato, estilo | `style: aplicar formato de código` |
| **refactor** | Refactorización | `refactor: extraer lógica a servicio separado` |
| **test** | Tests | `test: agregar tests para controlador de usuarios` |
| **chore** | Tareas de mantenimiento | `chore: actualizar dependencias de Spring` |

### 🧪 Ejecutar Tests Antes de Contribuir
```bash
# Ejecutar todos los tests
./mvnw clean test

# Ejecutar tests de integración
./mvnw test -Dtest="*IntegrationTest"

# Verificar calidad de código
./mvnw spotless:check pmd:check
```

---

## 👨‍💻 Autor

<div align="center">

**Darwin Manuel Ovalles Cesar**

<p align="center">
<a href="https://www.linkedin.com/in/darwin-manuel-ovalles-cesar-dev" target="_blank">
<img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="LinkedIn - Darwin Ovalles" height="40" width="50" />
</a>
<a href="https://github.com/dovalless" target="_blank">
<img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/github.svg" alt="GitHub - Darwin Ovalles" height="40" width="50" />
</a>
</p>

💼 **LinkedIn**: [darwin-manuel-ovalles-cesar-dev](https://www.linkedin.com/in/darwin-manuel-ovalles-cesar-dev/)  
🌐 **GitHub**: [@dovalless](https://github.com/dovalless)  
📧 **Contacto**: Disponible a través de LinkedIn  
🎓 **Certificaciones**: Java, Spring Framework, AWS, Docker  

*"ForoHub representa la aplicación de mejores prácticas en desarrollo de APIs REST con Spring Boot. Cada endpoint está diseñado pensando en escalabilidad, seguridad y mantenibilidad para servir como base para sistemas de foros de discusión robustos."*

**#Java #SpringBoot #RESTAPI #JWT #MySQL #Docker #CleanArchitecture**

</div>

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

```
MIT License
Copyright (c) 2024 Darwin Manuel Ovalles Cesar

Permiso concedido, libre de cargo, a cualquier persona que obtenga una copia
de este software y los archivos de documentación asociados (el "Software"), 
para tratar en el Software sin restricción, incluyendo sin limitación los derechos
de usar, copiar, modificar, fusionar, publicar, distribuir, sublicenciar y/o vender
copias del Software, y permitir a las personas a quienes se les proporcione el Software
hacer lo mismo, sujeto a las siguientes condiciones:

El aviso de copyright anterior y este aviso de permiso se incluirán en todas
las copias o partes sustanciales del Software.
```

---

## 🙏 Agradecimientos

- **Spring Framework Team** - Por crear un framework excepcional
- **Comunidad Java** - Por su continua innovación y apoyo
- **Alura Latam** - Por la inspiración para proyectos educativos
- **Contribuidores Open Source** - Por hacer posible el ecosistema

<div align="center">

### ⭐ Si ForoHub te resulta útil, considera darle una estrella en GitHub ⭐

### 🚀 ¡Próximo paso: Implementar WebSocket para chat en tiempo real! 🚀

**Desarrollado con 💙 y ☕ por Darwin Ovalles**

---
*Versión: 1.0.0 | Spring Boot 3.1.5 | Java 11 | Última actualización: Enero 2024*

</div>
```
