#  Urban Grocers - API & Backend QA

Este repositorio documenta las pruebas de backend realizadas para la aplicación "Urban Grocers", enfocándose en la lógica de negocios del servicio de mensajería y costos de entrega.

##  Objetivo del Proyecto
Validar la fiabilidad de la API encargada de calcular los costos y tiempos de entrega, asegurando que el sistema maneje correctamente las solicitudes según el inventario y destino.

##  Alcance de las Pruebas (Backend)

### 1. Validación de Lógica de Negocio
Se diseñaron y ejecutaron más de 40 casos de prueba para verificar algoritmos críticos:
* **Cálculo de Costos:** Verificación del campo `deliveryPrice` basado en variables dinámicas.
* **Tiempos de Entrega:** Validación de `deliveryTime` asegurando precisión en las estimaciones.
* **Variables de Entrada:** Pruebas de límites y equivalencia en los campos `productsWeight` y `productsCount` para evitar errores de cálculo.

### 2. Pruebas de API con Postman
* **Códigos de Estado:** Verificación de respuestas HTTP correctas:
    * `200 OK` para solicitudes válidas (incluso cuando `isItPossibleToDeliver: false`).
    * `400 Bad Request` para entradas inválidas o estructuras JSON incorrectas.
* **Escenarios:** Cobertura de casos positivos, negativos y "edge cases" (ej. IDs de productos inexistentes o listas duplicadas).

##  Herramientas Utilizadas
* **Postman:** Ejecución de colecciones de prueba y validación de JSON.
* **Swagger:** Análisis de documentación de API para diseño de casos.
* **Jira:** Reporte de bugs y seguimiento del ciclo de vida del defecto.
