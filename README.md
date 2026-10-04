# 🍳 Sazón — Digital Recipe & Weekly Meal Planner

> **Academic Project Disclaimer / Descargo de Responsabilidad Académico**
>
> **English:** This is a strictly non-commercial, educational project. All brand names, palettes, and product references are used for academic and simulation purposes only. The project maintains absolute legal and structural neutrality.
>
> **Español:** Este es un proyecto estrictamente académico y no comercial. El uso de marcas, paletas y referencias es puramente con fines educativos y de simulación. El proyecto mantiene una neutralidad legal y estructural absoluta.

---

## 🌎 Language Quick Links / Atajos de Idioma

*  🇬🇧 [English Version](#-english-documentation)
*  🇪🇸 [Versión en Español](#-documentación-en-español)

---

## 📄 Project Documentation

The complete requirements documentation for **Sazón — Célula 5: Planificador de Menús y Lista de Mercado** is available in PDF format.

### 🌐 Online Presentation

The project documentation can be presented through the static site:

👉 **[Open the Project Presentation](./index.html)**

### 📑 Requirements Report

The complete academic report is available here:

👉 **[Download / Open the Requirements Report](./INFORME_REQUISITOS_CELUlA_5.pdf)**

The static presentation uses the official PDF document contained in this repository as its primary source.






# 🇬🇧 English Documentation

## 📝 Project Overview

	**Sazón** is a full-stack digital recipe platform designed to optimize home cooking and minimize food waste.

	Users register the ingredients available in their pantries, and the platform dynamically suggests real, executable recipes, complete with:

	- Nutritional breakdowns
	- Weekly menu planning
	- Automatically generated grocery lists

	The ecosystem is built using a **decoupled, multi-cell micro-monolith architecture**, utilizing:

	- **React** for the Single Page Application (SPA) frontend
	- **Spring Boot** for the RESTful API backend
	- A shared **Relational Database** running on a **35-table schema**

---

## 🧬 Cell 5 Scope: Menu Planner & Grocery List

	This specific module (**Cell 5**) manages the transition from fragmented, isolated recipes into a cohesive, structured nutritional plan for the week.

### 💻 Frontend — React

#### Interactive Weekly Calendar

	Features a responsive layout allowing users to map out meals across specific days:

	- Monday–Sunday
	- Standard meal types

#### Categorized Grocery List

	Dynamically groups missing ingredients by product lines, allowing interactive checking/unchecking of purchased items without altering the base plan.

---

### ☕ Backend — Spring Boot

#### Menu Consolidator Engine

	Aggregates and parses ingredient quantities from multiple scheduled recipes.

#### Pantry Delta Calculator

	Computes the mathematical difference (**Delta**) between:

	- Required ingredients
	- Active inventory data shared by the Pantry Module

	This allows the system to determine which ingredients are actually missing.

#### Secured API Endpoints

	REST endpoints are validated against the centralized:

	- JWT authentication architecture
	- Spring Security configuration

---

## 💾 Relational Data Model — Cell 5

	The data layer for this module is completely normalized to **Third Normal Form (3NF)** to avoid transactional anomalies and ensure relational integrity.

### Entity-Relationship Architecture

	| Entity | Description |
	|---|---|
	| `planes_menu` | Tracks the metadata of the user's weekly structural plan. |
	| `detalles_menu` | Weak entity resolving the many-to-many relationship between plans and scheduled recipes. |
	| `listas_mercado` | Stores the unique instances of generated grocery tracking sheets. |
	| `items_mercado` | Tracks the dynamic state (bought/missing), metrics, and quantities of target ingredients. |
	| `categorias_ingrediente` | Internal lookup dictionary used to optimize the classification and scannability of grocery outputs. |

---

## 🛠️ Technological Stack

	| Layer | Technology |
	|---|---|
	| Frontend | React (SPA Architecture), JavaScript (ES6+), Bootstrap 5.3.3 |
	| Backend | Java, Spring Boot 3.x, Spring Security, JPA/Hibernate |
	| Security | Stateless Session via JWT (JSON Web Tokens) |
	| Database | Relational Schema (SQL) |
	| Agile Management | Scrum Framework (Unipersonal Resilient Delivery) |

---

# 🇪🇸 Documentación en Español


## 📝 Descripción General del Proyecto

	**Sazón** es un recetario digital full-stack diseñado para optimizar la cocina en el hogar y reducir el desperdicio de alimentos.

	La plataforma permite al usuario ingresar los insumos disponibles en su despensa para devolverle:

	- Opciones de preparación reales
	- Desgloses nutricionales
	- Un organizador de menús semanales
	- Una lista de compras automatizada

	El ecosistema está construido bajo una **arquitectura desacoplada de desarrollo en paralelo (7 células)**, utilizando:

	- **React** para el frontend y las vistas SPA
	- **Spring Boot** para el procesamiento de la lógica de negocio mediante una API REST
	- Una **Base de Datos Relacional compartida** compuesta por **35 tablas de negocio**

---

## 🧬 Alcance de la Célula 5: Planificador de Menús y Lista de Mercado

	Este módulo específico es el encargado de transformar recetas aisladas en un plan nutricional estructurado para el usuario.




### 💻 Frontend — React

#### Calendario Semanal Interactivo

	Interfaz adaptativa que permite organizar las preparaciones por:

	- Días de la semana
	- Momentos del día

#### Lista de Mercado Dinámica

	Agrupación automatizada de los ingredientes faltantes por categorías de pasillo, permitiendo tachar artículos comprados en tiempo real.

---

### ☕ Backend — Spring Boot

#### Motor de Consolidación de Menús

	Agrega, unifica y procesa las métricas y porciones de ingredientes procedentes de las recetas programadas.

#### Calculador Delta de Inventario

	Resta matemáticamente los insumos existentes en el módulo de **Despensa Virtual** para generar únicamente los ítems faltantes.

#### Endpoints REST Protegidos

	Los endpoints REST están protegidos mediante la integración centralizada de:

	- JWT
	- Spring Security

---

## 💾 Modelo de Datos Relacional — Célula 5

	La persistencia de datos de este módulo se encuentra rigurosamente normalizada en **Tercera Forma Normal (3NF)** para evitar redundancias e incoherencias transaccionales.

### Entidades Implementadas

	| Entidad | Descripción |
	|---|---|
	| `planes_menu` | Registra los encabezados y la vigencia del cronograma de alimentación del usuario. |
	| `detalles_menu` | Entidad asociativa que conecta los días y momentos específicos con las recetas del sistema. |
	| `listas_mercado` | Almacena las instancias independientes de compras generadas a partir de un plan activo. |
	| `items_mercado` | Controla el estado transitorio (comprado/pendiente) e inventario requerido de cada ingrediente. |
	| `categorias_ingrediente` | Diccionario maestro que optimiza el ordenamiento visual de la lista de compras. |

---

## 🛠️ Stack Tecnológico

	| Capa | Tecnología |
	|---|---|
	| **Frontend** | React (Arquitectura SPA), JavaScript (ES6+), Bootstrap 5.3.3 |
	| **Backend** | Java, Spring Boot 3.x, Spring Security, JPA/Hibernate |
	| **Seguridad** | Autenticación de sesión Stateless mediante JWT |
	| **Base de Datos** | Motor Relacional compatible con estándar ANSI SQL |
	| **Gestión Ágil** | Framework Scrum (Ejecución y Resiliencia Unipersonal) |

---

# 🚀 How to Run / Cómo Ejecutar


## ☕ Backend Setup



### 1. Navigate to the backend directory / Navega al directorio del backend

	bash
	cd backend

### 2. Configure your database connection / Configura la conexión de base de datos

	Edit the following file:

	src/main/resources/application.properties

	Configure the required database properties according to your local environment.

### 3. Execute the Spring Boot application / Ejecuta la aplicación
	
	./mvnw spring-boot:run

##    Frontend Setup

### 4. Navigate to the frontend directory / Navega al directorio del frontend

	cd frontend

### 5. Install npm dependencies / Instala las dependencias

	npm install

### 6. Launch the development server / Inicia el entorno de desarrollo

	npm start



## 📁 Basic Project Structure
	sazon/
	├── backend/
	│   ├── src/
	│   │   └── main/
	│   │       ├── java/
	│   │       └── resources/
	│   │           └── application.properties
	│   └── mvnw
	│
	├── frontend/
	│   ├── src/
	│   ├── public/
	│   ├── package.json
	│   └── ...
	│
	└── README.md


## 📌 Academic Project

This project is developed exclusively for educational, academic, and simulation purposes.

Este proyecto ha sido desarrollado exclusivamente con fines educativos, académicos y de simulación.

## Contributors:

https://github.com/Ambetazam/
https://github.com/andresvel-dot/
