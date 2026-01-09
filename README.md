# Spring Boot Microservice Dependencies

Dependencias obligatorias para microservicios basados en Spring Boot.

## Descripción

Este proyecto es un POM padre que define las dependencias estándar y obligatorias para microservicios desarrollados con Spring Boot en la organización. Incluye starters esenciales, herramientas de monitoreo, documentación de APIs, manejo de errores, resiliencia y utilidades de desarrollo.

## Uso

Para utilizar estas dependencias en un nuevo microservicio, configure el POM de su proyecto de la siguiente manera:

```xml
<parent>
    <groupId>com.nacionservicios.emv</groupId>
    <artifactId>spring-boot-microservice-dependencies</artifactId>
    <version>1.0.0</version>
</parent>
```

Esto heredará automáticamente todas las dependencias definidas en este proyecto.

## Dependencias Incluidas

Este POM incluye las siguientes dependencias principales:

### Spring Boot Starters
- **spring-boot-starter-web**: Para desarrollo de aplicaciones web con Spring MVC
- **spring-boot-starter-validation**: Para validación de beans con Hibernate Validator
- **spring-boot-starter-actuator**: Para monitoreo y métricas de la aplicación

### Monitoreo y Tracing
- **micrometer-tracing-bridge-otel**: Puente para tracing con OpenTelemetry
- **opentelemetry-exporter-otlp**: Exportador OTLP para OpenTelemetry

### Documentación de APIs
- **spring-openapi-starter**: Starter personalizado para OpenAPI
- **springdoc-openapi-starter-webmvc-ui**: Generación automática de documentación OpenAPI con UI

### Manejo de Errores y Resiliencia
- **exception-handling-spring-boot-starter**: Starter personalizado para manejo de excepciones
- **resilience4j-spring-boot3**: Librería de resiliencia (circuit breaker, retry, rate limiter)

### Utilidades de Desarrollo
- **lombok**: Para reducción de código boilerplate (opcional)
- **mapstruct**: Para mapeo de objetos
- **spring-boot-devtools**: Herramientas de desarrollo (opcional)

### Testing
- **spring-boot-starter-test**: Dependencias para testing con Spring Boot

### Construcción de Imágenes Docker
- **jib-maven-plugin**: Plugin Google Jib para construcción optimizada de imágenes Docker sin Docker daemon

## Configuración

La mayoría de las dependencias están preconfiguradas con versiones compatibles. Para versiones específicas, consulte las propiedades definidas en el POM padre (`spring-boot-master-parent`).

## Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-07-01

### Added
- Spring Boot Web Starter para desarrollo de APIs REST
- Spring Boot Validation Starter para validación de datos
- Spring Boot Actuator para monitoreo y health checks
- Micrometer Tracing Bridge OpenTelemetry para observabilidad
- OpenTelemetry Exporter OTLP para exportación de traces
- Spring OpenAPI Starter personalizado para documentación
- SpringDoc OpenAPI Starter con UI para documentación interactiva
- Exception Handling Spring Boot Starter para manejo centralizado de errores
- Resilience4j Spring Boot 3 para patrones de resiliencia
- Lombok para reducción de código boilerplate
- MapStruct para mapeo de objetos DTO
- Spring Boot DevTools para desarrollo
- Spring Boot Test Starter para testing
- Google Jib Maven Plugin para construcción optimizada de imágenes Docker
