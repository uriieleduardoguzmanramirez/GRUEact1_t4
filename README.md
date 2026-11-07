# Actividad 1. Introducción a Spring Boot

**Materia:** Programación Web  
**Docente:** Adelina Martínez  
**Alumno:** Uriel Eduardo Guzmán Ramírez  
**Carrera:** Ingeniería en Sistemas Computacionales  
**Tema:** Configuración de Spring Boot y primeros controladores  
**Repositorio:** GRUEact1_t4

---

## 1. Introducción

En esta práctica se desarrolló una aplicación web básica utilizando Java y Spring Boot, con el propósito de conocer cómo se configura un proyecto y cómo funciona un servidor que recibe peticiones HTTP.

Se crearon controladores que permiten consultar información mediante diferentes rutas o endpoints, mostrando respuestas en texto y formato JSON.

También se realizaron pruebas de funcionamiento en la computadora local y se ejecutó la aplicación en un servidor VPS utilizando un puerto específico.

## 2. Objetivo

Configurar un entorno de desarrollo con Java y Spring Boot, crear controladores que respondan peticiones GET y ejecutar la aplicación tanto de manera local como en un servidor VPS.

## 3. Tecnologías utilizadas

- **Java 21:** lenguaje de programación utilizado.
- **Spring Boot:** framework para desarrollar la aplicación web.
- **Spring Web:** dependencia utilizada para crear los endpoints.
- **Maven:** herramienta para administrar las dependencias y compilar el proyecto.
- **Visual Studio Code:** editor utilizado para desarrollar el código.
- **Ubuntu (VPS):** servidor donde se ejecutó la aplicación.
- **Git y GitHub:** herramientas utilizadas para administrar y almacenar el proyecto.

## 4. Desarrollo de la práctica

Primero se creó el proyecto desde Spring Initializr, seleccionando Java, Maven y la dependencia Spring Web.

Después se abrió en Visual Studio Code y se desarrollaron dos controladores:

**ProyectoController.java**

Contiene dos endpoints. Uno muestra el nombre del proyecto y el otro devuelve información sobre su estado.

**MateriasController.java**

Contiene un endpoint que devuelve una lista de materias en formato JSON.

Para implementar los controladores se utilizó la anotación `@RestController` y para definir las rutas se utilizó `@GetMapping`.

## 5. Endpoints desarrollados

| Método | Endpoint | Descripción |
|---|---|---|
| GET | `/proyecto` | Muestra el nombre del proyecto. |
| GET | `/estado` | Devuelve información sobre el proyecto en formato JSON. |
| GET | `/materias` | Devuelve una lista de materias. |

### Ejemplo 1. Nombre del proyecto

**URL:** `http://localhost:8080/proyecto`

**Respuesta:**

```text
Proyecto Spring Boot - Uriel Eduardo
```

### Ejemplo 2. Estado del proyecto

**URL:** `http://localhost:8080/estado`

**Respuesta:**

```json
{
  "proyecto": "GRUEact1_t4",
  "estado": "Funcionando",
  "materia": "Programacion Web"
}
```

### Ejemplo 3. Lista de materias

**URL:** `http://localhost:8080/materias`

**Respuesta:**

```json
[
  "Programacion Web",
  "Administracion de Redes",
  "Automatas II",
  "Sistemas Programables"
]
```

## 6. Ejecución del proyecto

Para ejecutar el proyecto localmente, se abre la terminal en la carpeta principal y se utiliza:

```bash
./mvnw spring-boot:run
```

En Windows:

```powershell
.\mvnw.cmd spring-boot:run
```

Una vez iniciado el servidor, se pueden consultar los endpoints desde el navegador o Postman utilizando `localhost:8080`.

### Compilación

Para generar el archivo `.jar`, se utiliza:

```bash
./mvnw clean package
```

El archivo compilado se genera dentro de la carpeta `target`.


**Dirección del proyecto:**

http://52.159.103.236:8081/proyecto


## 7. Conclusión

Esta práctica permitió comprender el funcionamiento básico de Spring Boot, desde la creación y configuración de un proyecto hasta el desarrollo de controladores y endpoints.

También se aprendió a utilizar Maven para compilar la aplicación y a ejecutarla en un VPS, comprendiendo la diferencia entre realizar pruebas en un entorno local y publicar un servicio en un servidor.

Con estos conocimientos se establecen las bases para desarrollar posteriormente aplicaciones web más completas utilizando Java y Spring Boot.

---


