# 🚀 Spring Boot Demo

> Setup inicial de un proyecto backend con **Spring Boot 4**, Jetty y Actuator listo para escalar.

---

## 📋 Descripción

Base de un proyecto backend con **Spring Boot 4** configurado con servidor embebido **Jetty**, **Spring Actuator** para monitoreo y **DevTools** para hot-reload. Pensado como punto de partida sólido para una arquitectura de microservicios.

---

## 🛠️ Tecnologías

| Tecnología | Versión |
|---|---|
| Java | 25 |
| Spring Boot | 4.0.3 |
| Servidor embebido | Jetty |
| Build tool | Maven |

### Dependencias principales

- `spring-boot-starter-webmvc` — MVC web framework
- `spring-boot-starter-jetty` — Servidor embebido Jetty (reemplaza Tomcat)
- `spring-boot-starter-actuator` — Endpoints de monitoreo y salud
- `spring-boot-devtools` — Hot-reload en desarrollo

---

## 📁 Estructura del proyecto

```
spring-boot-demo/
├── src/
│   ├── main/
│   │   ├── java/com/microservice/springbootdemo/
│   │   │   ├── SpringBootDemoApplication.java   # Entry point
│   │   │   └── controller/
│   │   │       └── HomeController.java          # Endpoint raíz
│   │   └── resources/
│   │       └── application.properties           # Configuración
│   └── test/
│       └── java/com/microservice/springbootdemo/
│           └── SpringBootDemoApplicationTests.java
├── pom.xml
└── mvnw
```

---

## ⚡ Endpoints

| Método | URL | Descripción |
|---|---|---|
| `GET` | `/` | Retorna `Hello World!` |
| `GET` | `/actuator/health` | Estado de salud de la app |
| `GET` | `/actuator` | Lista de endpoints del actuator |

---

## 🚀 Cómo ejecutar

### Prerrequisitos

- Java 25+
- Maven 3.9+ (o usar el wrapper incluido `./mvnw`)

### Levantar la aplicación

```bash
# Clonar el repositorio
git clone https://github.com/miguelbtcode/spring-boot-demo.git
cd spring-boot-demo

# Ejecutar con Maven Wrapper
./mvnw spring-boot:run
```

La aplicación estará disponible en: **http://localhost:8081**

### Compilar el JAR

```bash
./mvnw clean package
java -jar target/spring-boot-demo-0.0.1-SNAPSHOT.jar
```

### Ejecutar tests

```bash
./mvnw test
```

---

## ⚙️ Configuración

El archivo `src/main/resources/application.properties` contiene:

```properties
spring.application.name=spring-boot-demo
server.port=8081
```

Para cambiar el puerto, modifica `server.port` o usa una variable de entorno:

```bash
SERVER_PORT=9090 ./mvnw spring-boot:run
```

---

## 📄 Licencia

MIT License — libre de usar, modificar y distribuir.
# microservices-spring-boot
