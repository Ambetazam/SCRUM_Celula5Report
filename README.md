🍳 Sazón - Digital Recipe & Weekly Meal Planner
Academic Project Disclaimer / Descargo de Responsabilidad Académico: This is a strictly non-commercial, educational project. All brand names, palettes, and product references are used for academic and simulation purposes only. The project maintains absolute legal and structural neutrality.
Este es un proyecto estrictamente académico y no comercial. El uso de marcas, paletas y referencias es puramente con fines educativos y de simulación. El proyecto mantiene una neutralidad legal y estructural absoluta.
🌎 Language Quick Links / Atajos de Idioma
• English Version
• Versión en Español
🇬🇧 English Documentation
📝 Project Overview
Sazón is a full-stack digital recipe platform designed to optimize home cooking and minimize food waste. Users register the ingredients available in their pantries, and the platform dynamically suggests real, executable recipes, complete with nutritional breakdowns, a weekly menu planner, and an automatically generated grocery list.
The ecosystem is built using a decoupled, multi-cell micro-monolith architecture, utilizing React for the Single Page Application (SPA) frontend, Spring Boot for the RESTful API backend, and a shared Relational Database running on a 35-table schema.
🧬 Cell 5 Scope: Menu Planner & Grocery List
This specific module (Cell 5) manages the transition from fragmented, isolated recipes into a cohesive, structured nutritional plan for the week.
💻 Frontend (React)
• Interactive Weekly Calendar: Features a responsive layout allowing users to map out meals across specific days (Monday–Sunday) and standard meal types.
• Categorized Grocery List: Dynamically groups missing ingredients by product lines, allowing interactive checking/unchecking of purchased items without altering the base plan.
☕ Backend (Spring Boot)
• Menu Consolidator Engine: Aggregates and parses ingredient quantities from multiple scheduled recipes.
• Pantry Delta Calculator: Computes the mathematical difference (Delta) between required ingredients and active inventory data shared by the Pantry Module.
• Secured API endpoints validated against the centralized JWT/Spring Security architecture.
💾 Relational Data Model (Cell 5)
The data layer for this module is completely normalized to Third Normal Form (3NF) to avoid transactional anomalies and ensure relational integrity.
Entity-Relationship Architecture
• planes_menu: Tracks the metadata of the user's weekly structural plan.
• detalles_menu: Weak entity resolving the many-to-many relationship between plans and scheduled recipes.
• listas_mercado: Stores the unique instances of generated grocery tracking sheets.
• items_mercado: Tracks the dynamic state (bought/missing), metrics, and quantities of target ingredients.
• categorias_ingrediente: Internal lookup dictionary to optimize the classification and scannability of grocery outputs.
🛠️ Technological Stack
• Frontend: React (SPA Architecture), JavaScript (ES6+), Bootstrap 5.3.3.
• Backend: Java, Spring Boot 3.x, Spring Security, JPA/Hibernate.
• Security: Stateless Stateless Session via JWT (JSON Web Tokens).
• Database: Relational Schema (SQL).
• Agile Management: Scrum framework (Unipersonal Resilient Delivery).
🇪🇸 Documentación en Español
📝 Descripción General del Proyecto
Sazón es un recetario digital full-stack diseñado para optimizar la cocina en el hogar y reducir el desperdicio de alimentos. La plataforma permite al usuario ingresar los insumos disponibles en su despensa para devolverle opciones de preparación reales, desgloses nutricionales, un organizador de menús semanales y una lista de compras automatizada.
El ecosistema está construido bajo una arquitectura desacoplada de desarrollo en paralelo (7 células), utilizando React para el frontend (vistas SPA), Spring Boot para el procesamiento de la lógica de negocio (API REST), y una Base de Datos Relacional compartida compuesta por 35 tablas de negocio.
🧬 Alcance de la Célula 5: Planificador de Menús y Lista de Mercado
Este módulo específico es el encargado de transformar recetas aisladas en un plan nutricional estructurado para el usuario.
💻 Frontend (React)
• Calendario Semanal Interactivo: Interfaz adaptativa que permite organizar las preparaciones por días de la semana y momentos del día.
• Lista de Mercado Dinámica: Agrupación automatizada de los ingredientes faltantes por categorías de pasillo, permitiendo tachar artículos comprados en tiempo real.
☕ Backend (Spring Boot)
• Motor de Consolidación de Menús: Agrega, unifica y procesa las métricas y porciones de ingredientes procedentes de las recetas programadas.
• Calculador Delta de Inventario: Resta matemáticamente los insumos existentes en el módulo de Despensa Virtual para generar únicamente los ítems faltantes.
• Endpoints REST protegidos mediante la integración centralizada de JWT y Spring Security.
💾 Modelo de Datos Relacional (Célula 5)
La persistencia de datos de este módulo se encuentra rigurosamente normalizada en Tercera Forma Normal (3NF) para evitar redundancias e incoherencias transaccionales.
Entidades Implementadas
• planes_menu: Registra los encabezados y la vigencia del cronograma de alimentación del usuario.
• detalles_menu: Entidad asociativa que conecta los días y momentos específicos con las recetas del sistema.
• listas_mercado: Almacena las instancias independientes de compras generadas a partir de un plan activo.
• items_mercado: Controla el estado transitorio (comprado/pendiente) e inventario requerido de cada ingrediente.
• categorias_ingrediente: Diccionario maestro que optimiza el ordenamiento visual de la lista de compras.
🛠️ Stack Tecnológico
• Frontend: React (Arquitectura SPA), JavaScript (ES6+), Bootstrap 5.3.3.
• Backend: Java, Spring Boot 3.x, Spring Security, JPA/Hibernate.
• Seguridad: Autenticación de sesión Stateless mediante JWT.
• Base de Datos: Motor Relacional compatible con estándar ANSI SQL.
• Gestión Ágil: Framework Scrum (Ejecución y Resiliencia Unipersonal).
🚀 How to Run / Cómo Ejecutar
Backend Setup
1. Navigate to the backend directory / Navega al directorio del backend: cd backend
2. Configure your database connections in / Configura la base de datos en: src/main/resources/application.properties
3. Execute the Spring Boot application / Ejecuta la aplicación: ./mvnw spring-boot:run
Frontend Setup
1. Navigate to the frontend directory / Navega al directorio del frontend: cd frontend
2. Install npm dependencies / Instala las dependencias: npm install
3. Launch the development server / Inicia el entorno de desarrollo: npm start
