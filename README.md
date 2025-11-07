# Capullos_ExamenA: ☕ Cafetería ITAM - Sistema de Pedidos con IA

Este repositorio contiene el diseño y documentación de un sistema de pedidos para la Cafetería del ITAM, desarrollado para la materia de Ingeniería de Software. 
- El objetivo principal es modelar un sistema funcional que permita a los estudiantes realizar pedidos, a los cajeros administrarlos y a los managers gestionar inventarios, incorporando recomendaciones personalizadas a través de Inteligencia Artificial.

El proyecto se desarrolló siguiendo principios de *arquitectura combinada basada en eventos y microservicios, priorizando **escalabilidad y extensibilidad*.

---

## 📂 Archivos del Repositorio

| Archivo / Carpeta | Descripción |
|------------------|-------------|
| casoDeUso.md | Contiene el diagrama y la descripción detallada de los *Casos de Uso*, actores, includes y extends. |
| arquitectura.pdf | Explica la *arquitectura del sistema*, combinando microservicios y manejo de eventos. |
| excelCostos.md | Incluye la *planificación temporal*, costos aproximados y desglose de funcionalidades implementables en 3 meses. |
| chatbot.md | Documento donde se describe el chatbot o recomendaciones IA utilizadas en el sistema. |

---

## Objetivos 

El sistema permite:
- Estudiantes: visualizar el menú, recibir recomendaciones de IA, ordenar y pagar. Esto se hace principalmente mediante un *chatbot* (arquitectura de eventos).
- Cajeros: consultar pedidos y marcar entregas.
- Managers: modificar inventario y visualizar predicciones de demanda basadas en IA.

El sistema se conecta (arquitectura de microservicios) con:
- *API Interna de la Cafetería* (menú, tickets, inventario)
- *Sistema Administrativo del ITAM* (login y cargo a colegiatura)

---

## 🦋 Miembros

- Rafaerl Harry Gomar
- Luis Fernando Rodríguez Retama
- Axel Castro Lara
- Valentina Maqueda Andrade
- Mauricia Peña López Ostolaza

---
