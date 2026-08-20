<div align="center">
  <h1> Sistema de Gestión Integral Administrativa (SGIA)</h1>
  <p><i>Proyecto de Prácticas Profesionales. Una solución de escritorio robusta, modular y segura para la administración moderna de recursos humanos, activos y bienestar social.</i></p>
  
  [![Python Version](https://img.shields.io/badge/Python-3.13%2B-blue.svg)](https://www.python.org/)
  [![GUI](https://img.shields.io/badge/GUI-Tkinter-lightgrey.svg)]()
  [![Database](https://img.shields.io/badge/Database-SQLite3-003B57.svg)]()
  [![License](https://img.shields.io/badge/License-MIT-green.svg)]()
</div>

---

## Descripción General

El **SGIA** es un proyecto desarrollado como parte de las prácticas profesionales. Se trata de una plataforma de escritorio desarrollada íntegramente en Python. Diseñada bajo un enfoque de arquitectura modular, la aplicación centraliza y automatiza los procesos críticos de la organización, ofreciendo una experiencia de usuario (UX) fluida y moderna. 

El sistema garantiza la integridad y confidencialidad de la información mediante bases de datos aisladas, encriptación de credenciales y un sistema de auditoría continua (logs).

![System Preview](https://github.com/Lmendoza09/Sistema-de-Gestion-Integral-SGIA-/blob/main/Sistema%20SGIA.jpeg)

## Características Destacadas

### Seguridad y Orquestación (`Main.py`)
- **Autenticación Cifrada:** Gestión de credenciales utilizando algoritmos de *hashing* seguro.
- **Control de Acceso Basado en Roles (RBAC):** Restricción y habilitación de funcionalidades según el perfil de seguridad del usuario.
- **Trazabilidad Continua:** Implementación de `RotatingFileHandler` para el registro inmutable de eventos y transacciones en el sistema.
- **UI/UX Moderna:** Interfaces diseñadas con componentes personalizados (*Custom Widgets*) de Tkinter/ttk, soportando estados *hover*, animaciones y una paleta de colores corporativa estandarizada.

### Gestión del Capital Humano (`GestionHumana.py`)
- **Expediente Digital Único:** Centralización de datos demográficos, médicos, de contacto y operativos de los funcionarios.
- **Control de Estructura Organizativa:** Mapeo de cargos, dependencias departamentales y antigüedad del personal.
- **Gestión Documental:** Vinculación de soportes físicos (como PDFs de identificación) directamente a los perfiles digitales.
- **Mapeo Familiar:** Registro del núcleo familiar para procesos de beneficios, seguros y contacto de emergencia.

### Control de Activos y Bienes (`Bienes.py`)
- **Gestión de Inventario:** Ciclo de vida completo del inventario institucional y tecnológico.
- **Trazabilidad de Asignaciones:** Seguimiento de responsables, estados operativos y ubicaciones físicas de cada activo.

### Bienestar Social y Salud Ocupacional (`BienestarSocial.py`)
- **Gestión de Ausentismo y Reposos:** Monitoreo detallado de incidencias médicas, tiempos de recuperación y diagnósticos.
- **Estadísticas de Salud:** Organización de la data médica para facilitar la exportación y el análisis de salud ocupacional.

## Stack Tecnológico

| Componente | Tecnología | Propósito |
|------------|------------|-----------|
| **Core & Lógica** | `Python 3.13` | Lenguaje principal de desarrollo y orquestación. |
| **Frontend** | `Tkinter` & `ttk` | Interfaz gráfica nativa optimizada con estilos visuales modernos. |
| **Persistencia** | `SQLite3` | Base de datos relacional local, estructurada en micro-bases de datos. |
| **Reportes PDF** | `ReportLab` | Generación dinámica de reportes, actas y comprobantes en formato PDF. |
| **Reportes Excel**| `OpenPyXL` | Extracción de datos y construcción de reportes tabulares (`.xlsx`). |
| **Imágenes** | `Pillow (PIL)` | Manipulación y renderizado de fotografías de perfil y recursos gráficos. |

## Arquitectura de Almacenamiento

Para garantizar la seguridad, portabilidad y limpieza del entorno, el sistema emplea una estrategia de **aislamiento de datos locales**:
- **Almacenamiento Oculto:** Generación automática de un entorno de datos protegido (ej. `.sistema_bienes` en Temp/AppData) con atributos del sistema operativo para prevenir manipulaciones accidentales por parte del usuario final.
- **Bases de Datos Desacopladas:** Cada módulo opera sobre su propia base de datos (`gestion_humana.db`, `sistema_bienes.db`, `sistema_reposos.db`). Esto previene bloqueos transaccionales, reduce riesgos de corrupción y facilita los respaldos modulares.

## Link del Video

💾  [Demostración del Sistema] (https://youtu.be/_X_LrD-WAhI)

