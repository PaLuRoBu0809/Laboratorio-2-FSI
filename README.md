## Informe de Laboratorio Nro 2: Reglas del Negocio con Spring Boot y Drools

Este repositorio contiene la implementación de un **Sistema de Administración de Reglas de Negocio (BRMS)** aplicado a una aerolínea comercial. El proyecto utiliza el motor de reglas **Drools** integrado con **Spring Boot** para desacoplar la lógica de negocio del código transaccional.

---

## Información
* **Asignatura:** Fundamentos de Sistemas de Información
* **Estudiante:** Pablo Luis Rodriguez Burgos
* **Docente:** Diego Botia
* **Fecha de entrega:** 14 de Abril de 2026

---

## Introducción
El objetivo principal de esta práctica es reemplazar la lógica de negocio rígida (*hardcoded*) por un paradigma de **programación declarativa**. Utilizando el lenguaje **DRL (Drools Rule Language)** y el algoritmo **Rete**, el sistema evalúa dinámicamente políticas operativas complejas (beneficios, ascensos, equipaje, compensaciones) sin necesidad de recompilar la aplicación ante cambios en las reglas.

---

## Tecnologías Utilizadas
* **Java 17**
* **Spring Boot 3.2.x**
* **Drools 8.44.0.Final**
* **Apache Maven** (Gestión de dependencias)
* **Postman** (Pruebas de API REST)
* **NetBeans** (IDE)

---

## Arquitectura de la Solución
El proyecto sigue el patrón **MVC** (orientado a microservicios) y se divide en los siguientes módulos:

| Capa | Descripción |
| :--- | :--- |
| **Model** | POJOs (`Passenger`, `Flight`, `Luggage`) que representan los *Facts* evaluados por el motor. |
| **Config** | Inicialización de `KieServices` y `KieContainer` como Singleton en el contexto de Spring. |
| **Service** | Or
