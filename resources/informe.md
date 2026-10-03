F# INFORME DE REQUISITOS: PLANIFICADOR DE MENÚS Y LISTA DE MERCADO

## CÉLULA 5 - PROYECTO SAZÓN

---

### PORTADA

**PROYECTO SAZÓN: INFORME DE REQUISITOS**  
**MÓDULO: PLANIFICADOR DE MENÚS Y LISTA DE MERCADO (CÉLULA 5)**  

**Autor:**  
Jean Steven / Scrum Master & Lead Developer

**Institución Educativa:**  
CESDE  

**Programa:**  
Análisis y Desarrollo de Software / Ingeniería de Software  

**Fecha:**  
Octubre 06 de 2026  

---

### TABLA DE CONTENIDO

1. Introducción
2. Objetivos
   2.1. Objetivo General
   2.2. Objetivos Específicos
3. Planteamiento del Problema
   3.1. Necesidad
   3.2. Manejo Actual
   3.3. Solución Propuesta
4. Alcance del Proyecto (Célula 5)
   4.1. Inclusiones (Entregables)
   4.2. Exclusiones
   4.3. Despliegue y Relación Arquitectónica (Frontend - Backend)
5. Stack Tecnológico
6. Diagramación y Modelado
   6.1. Casos de Uso
   6.2. Modelo Relacional de Datos (5 Tablas)
   6.3. Script SQL (DDL Deducido)
7. Aspectos Legales, Propiedad Intelectual y Cumplimiento Contractual
   7.1. Marco Legal del Contrato de Aprendizaje y Exposición Corporativa
   7.2. Análisis de Infracciones Marcarías (Uso No Autorizado de Grupo Nutresa S.A.)
   7.3. Responsabilidades y Sanciones Consecuentes
8. Conclusiones y Reflexión de Trabajo en Equipo
   8.1. Conclusiones del Desarrollo Técnico
   8.2. Reflexión de Gestión (Scrum Master ante Células de Trabajo Inactivas)
9. Glosario
10. Bibliografía

#### LISTADO DE TABLAS
* Tabla 1: Matriz de Trazabilidad de Requisitos de la Célula 5.
* Tabla 2: Diccionario de Datos - Entidades de Persistencia del Planificador.

#### LISTADO DE ILUSTRACIONES
* Ilustración 1: Diagrama de Casos de Uso del Planificador Semanal (Célula 5).
* Ilustración 2: Modelo Entidad-Relación (MER) de las 5 Tablas del Módulo.
* Ilustración 3: Arquitectura de Despliegue Decoupled Frontend-Backend.

---

## 1. INTRODUCCIÓN

El desarrollo de sistemas de información aplicados a la optimización de procesos cotidianos representa uno de los pilares de la ingeniería de software contemporánea. El presente "Informe de Requisitos" detalla de forma exhaustiva los componentes arquitectónicos, funcionales, legales y relacionales que estructuran el módulo de Planificador de Menús y Lista de Mercado, denominado técnicamente como la Célula 5 dentro del macroproyecto ecosistémico "Sazón". 

Este documento se ha formulado bajo los lineamientos metodológicos de la Guía de Fundamentos para la Dirección de Proyectos (PMBOK) y las directrices de especificación de requisitos formal. El objetivo es delimitar la frontera del software de la célula, garantizando la consistencia del modelo de datos frente a la arquitectura REST compartida, aislando los riesgos operacionales y configurando un entorno de software robusto, escalable y éticamente responsable.

---

## 2. OBJETIVOS

### 2.1. Objetivo General
Diseñar, especificar y modelar el sistema de información de requisitos y persistencia de datos para el módulo de "Planificador de Menús y Lista de Mercado", garantizando la sincronización full-stack descentralizada mediante React y Spring Boot, bajo un estricto marco de cumplimiento de propiedad intelectual y metodologías ágiles.

### 2.2. Objetivos Específicos
* Modelar la estructura relacional de persistencia deduciendo exactamente cinco (5) tablas normalizadas en tercera forma normal (3NF) que soporten los procesos de planificación semanal y consolidación dinámica de insumos.
* Delimitar el alcance formal (Inclusiones y Exclusiones) de la entrega técnica, especificando los mecanismos de despliegue desacoplados y la interconexión con el backend a través de Spring Security y tokens JWT.
* Evaluar el impacto legal y las contingencias disciplinarias derivadas del uso no autorizado de activos intangibles corporativos (marcas, enseñas comerciales y paletas tipográficas) en entornos educativos bajo contratos de aprendizaje.
* Documentar la reflexión de gestión de proyectos bajo el rol de Scrum Master unipersonal, evidenciando las estrategias de mitigación implementadas para salvaguardar el ciclo de vida del software ante la inactividad de la célula asignada.

---

## 3. PLANTEAMIENTO DEL PROBLEMA

### 3.1. Necesidad
La gestión del suministro alimentario doméstico padece de ineficiencias críticas debido a la falta de trazabilidad e integración entre la selección de recetas y la adquisición física de ingredientes. Los usuarios se enfrentan a la dispersión de información ("recetas sueltas"), lo que induce a la compra redundante de insumos, desperdicio de alimentos perecederos y una planificación nutricional deficiente que no considera el inventario actual de la despensa.

### 3.2. Manejo Actual
El proceso convencional se ejecuta de forma analógica o fragmentada: apuntes manuales, capturas de pantalla de preparaciones aisladas y estimaciones heurísticas en el supermercado. No existe un motor algorítmico accesible que consolide las listas de compras de múltiples preparaciones ni que compute restas lógicas automáticas basándose en lo existente en la alacena.

### 3.3. Solución Propuesta
Implementar un sistema full-stack modular enfocado en la transición fluida "de la receta suelta al plan de la semana". El usuario interactúa con un calendario interactivo que consume recetas publicadas por el sistema, traduciendo de forma inmediata la asignación temporal en una orden unificada de compra. El software realiza la suma de ingredientes homogéneos, aplica la sustracción de existencias registradas en la despensa virtual y expone una lista interactiva categorizada con estados de compra en tiempo real.

---

## 4. ALCANCE DEL PROYECTO (CÉLULA 5)

### 4.1. Inclusiones (El Entregable Final)
El entregable final comprende el software completo y funcional enmarcado rigurosamente en el dominio de la Célula 5:
* **Frontend SPA (React):** Interfaz responsive construida sobre Bootstrap 5.3 que incorpora un calendario semanal interactivo con funciones de arrastrar y soltar (Drag and Drop) para ubicar recetas por día y momento del día (Desayuno, Almuerzo, Cena). Vista modular de la lista de mercado autogenerada, agrupada taxonómicamente por categorías de alimentos (Cárnicos, Granos, Lácteos, etc.) con selectores interactivos (checkboxes) para actualizar el estado de adquisición.
* **Backend API REST (Spring Boot):** Componente de lógica empresarial que expone endpoints protegidos para la creación, lectura, actualización y eliminación (CRUD) de planes semanales. Motor de consolidación que intercepta los IDs de recetas del plan, consulta sus ingredientes al módulo maestro, computa la sumatoria de cantidades por unidad de medida estándar, ejecuta la resta lógica cruzando datos con el módulo de Despensa Virtual y genera el payload JSON de la lista definitiva.
* **Capa de Datos:** Estructura física implementada de cinco (5) tablas relacionales en el motor corporativo, integradas jerárquicamente con el módulo común transaccional de Usuarios (Módulo 00).

### 4.2. Exclusiones
Queda explícitamente fuera del scope de la Célula 5:
* El desarrollo del módulo de Usuarios, autenticación basada en claims, emisión y firma de tokens criptográficos JWT (Responsabilidad docente / Módulo 00).
* El repositorio maestro del Catálogo de Productos y Marcas de Alimentos (Célula 1).
* El desarrollo de algoritmos de recomendaciones nutricionales o cálculo de semáforos calóricos (Célula 4).
* El hosting centralizado de la base de datos de producción global y la pasarela de pago para adquisición externa de productos.

### 4.3. Despliegues y Relación Frontend-Backend
El sistema operará bajo una arquitectura desacoplada (Decoupled Architecture). El Frontend se desplegará de forma estática en plataformas orientadas a la optimización de bordes (Edge Networks) como Vercel o Netlify. El Backend en Spring Boot se empaquetará como un contenedor Dockerizado independiente y se desplegará en un entorno virtualizado en la nube o servidor local de pruebas. 

La comunicación se realizará exclusivamente de forma asíncrona mediante peticiones HTTPS transportando payloads HTTP JSON. Cada transacción originada en el cliente de React hacia los endpoints `/api/planificador/**` deberá adjuntar obligatoriamente el header `Authorization: Bearer <JWT_TOKEN>` para ser interceptado y validado por el filtro Spring Security de la aplicación.

---

## 5. STACK TECNOLÓGICO

El ecosistema tecnológico seleccionado responde a los criterios de robustez empresarial, soporte comunitario y tipado estricto en persistencia:
* **Frontend:** React.js, JavaScript (ECMAScript 6+), HTML5, CSS3 nativo soportado con variables dinámicas de diseño, Bootstrap 5.3 para maquetación modular y responsive, y Axios para consumo de servicios REST.
* **Backend:** Java Enterprise Edition (JDK 17+), Framework Spring Boot, Spring Security (Autenticación trans-módulo), Spring Data JPA para el mapeo objeto-relacional (ORM).
* **Persistencia:** Sistema de Gestión de Bases de Datos Relacionales (RDBMS) compatible con SQL estándar (PostgreSQL / MySQL).
* **Herramientas de Diseño y Gestión:** Canva Model y diagramadores UML para conceptualización arquitectónica; Git como sistema de control de versiones distribuido bajo el flujo GitFlow.

---

## 6. DIAGRAMACIÓN Y MODELADO

### 6.1. Casos de Uso
El comportamiento dinámico del sistema se rige por los siguientes casos de uso principales liderados por el actor "Cocinero" (Usuario Autenticado):
1. **CU-01: Crear Plan Semanal:** Permite inicializar un bloque temporal de planificación asociado al usuario.
2. **CU-02: Asignar Receta a Menú:** Operación Drag and Drop que vincula un ID de receta a un día específico (1-7) y tipo de comida.
3. **CU-03: Consolidar Lista de Mercado:** Ejecución del proceso por lotes en el servidor que lee el plan, une ingredientes, resta existencias de la despensa y genera los ítems de compra.
4. **CU-04: Actualizar Estado de Compra:** Modificación del flag booleano de adquisición sobre un ítem específico de la lista sin alterar los parámetros base del menú estructurado.

### 6.2. Modelo Relacional de Datos (Deducción Estricta de 5 Tablas)
Para soportar el modelo operativo de la Célula 5 sin incurrir en redundancias y respetando las convenciones obligatorias (nombres en minúsculas, plural, sin tildes, llaves primarias explícitas, tablas puente con guion bajo), se deducen las siguientes cinco (5) tablas de negocio:

1. **planes_menu:** Estructura la entidad principal de planificación temporalizada.
2. **detalles_menu:** Tabla que desglosa las celdas del calendario, asociando recetas específicas a días y momentos.
3. **listas_mercado:** Entidad con vida propia que consolida el encabezado de la orden de compras derivada de un plan.
4. **items_mercado:** Detalle granular de cada ingrediente o producto que se debe adquirir, su cantidad y estado.
5. **categorias_ingrediente:** Maestro taxonómico local para agrupar los ítems de la lista en la interfaz visual por pasillos de supermercado (Cárnicos, Lácteos, Vegetales, etc.).

### 6.3. Script SQL (DDL Estricto)
```sql
-- 1. Tabla de Categorias de Ingredientes (Agrupación taxonómica)
CREATE TABLE categorias_ingrediente (
    id_categoria INT AUTO_INCREMENT,
    nombre VARCHAR(100) NOT NULL,
    CONSTRAINT pk_categorias_ingrediente PRIMARY KEY (id_categoria)
);

-- 2. Tabla Principal de Planes de Menú
CREATE TABLE planes_menu (
    id_plan INT AUTO_INCREMENT,
    id_usuario INT NOT NULL, -- Apunta al módulo común transaccional 00
    fecha_inicio DATE NOT NULL,
    fecha_fin DATE NOT NULL,
    estado VARCHAR(30) DEFAULT 'activo',
    CONSTRAINT pk_planes_menu PRIMARY KEY (id_plan)
);

-- 3. Tabla Detalle de Menú (Asociación Calendario Semanal)
CREATE TABLE detalles_menu (
    id_detalle INT AUTO_INCREMENT,
    id_plan INT NOT NULL,
    id_receta INT NOT NULL, -- Apunta al módulo de la Célula 2 (Recetario)
    dia_semana INT NOT NULL, -- Valores de 1 a 7 (Lunes a Domingo)
    tipo_comida VARCHAR(30) NOT NULL, -- 'desayuno', 'almuerzo', 'cena', 'snack'
    CONSTRAINT pk_detalles_menu PRIMARY KEY (id_detalle),
    CONSTRAINT fk_detalles_planes FOREIGN KEY (id_plan) REFERENCES planes_menu(id_plan) ON DELETE CASCADE
);

-- 4. Tabla de Cabecera de Lista de Mercado
CREATE TABLE listas_mercado (
    id_lista INT AUTO_INCREMENT,
    id_plan INT NOT NULL,
    fecha_generacion TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    actualizada_en TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    CONSTRAINT pk_listas_mercado PRIMARY KEY (id_lista),
    CONSTRAINT fk_listas_planes FOREIGN KEY (id_plan) REFERENCES planes_menu(id_plan) ON DELETE CASCADE
);

-- 5. Tabla de Ítems Granulares de la Lista de Mercado
CREATE TABLE items_mercado (
    id_item INT AUTO_INCREMENT,
    id_lista INT NOT NULL,
    id_categoria INT NOT NULL,
    nombre_ingrediente VARCHAR(150) NOT NULL,
    cantidad_requerida DECIMAL(10,2) NOT NULL,
    unidad_medida VARCHAR(20) NOT NULL, -- 'g', 'ml', 'und', 'libra'
    comprado BOOLEAN DEFAULT FALSE, -- Flag interactivo React sin dañar el plan
    CONSTRAINT pk_items_mercado PRIMARY KEY (id_item),
    CONSTRAINT fk_items_listas FOREIGN KEY (id_lista) REFERENCES listas_mercado(id_lista) ON DELETE CASCADE,
    CONSTRAINT fk_items_categorias FOREIGN KEY (id_categoria) REFERENCES categorias_ingrediente(id_categoria)
);
```

---

## 7. ASPECTOS LEGALES, PROPIEDAD INTELECTUAL Y CUMPLIMIENTO CONTRACTUAL

### 7.1. Marco Legal del Contrato de Aprendizaje y Exposición Corporativa
El desarrollo de proyectos académicos en entornos de formación técnica o tecnológica bajo la modalidad de **Contrato de Aprendizaje** (por ejemplo, regulado en Colombia bajo la Ley 789 de 2002) se rige por un principio de estricta subordinación académica y contractual. Bajo este marco jurídico, los aprendices se asimilan a la esfera corporativa de las empresas patrocinadoras para su etapa práctica, estando sujetos a acuerdos explícitos de confidencialidad, uso ético de recursos y políticas de seguridad de la información.

Orientar de forma explícita un proyecto formativo de software para simular o suplantar una plataforma oficial de un conglomerado como **Grupo Nutresa S.A.** (o cualquiera de sus negocios: Zenú, Noel, Doria, Colcafé, etc.) sin contar con una autorización formal de la Dirección Jurídica de dicha compañía representa una extralimitación de las competencias académicas. El desconocimiento unilateral de los términos y condiciones de los contratos de aprendizaje o de los lineamientos formativos por parte del personal docente no exime de responsabilidad legal a los ejecutores del código.

### 7.2. Análisis de Infracciones Marcarías (Uso No Autorizado de Activos de Grupo Nutresa S.A.)
La apropiación indebida de los siguientes elementos en la aplicación desarrollada (como se evidencia en el código fuente extraído):
1. **Identidad Visual Corporativa:** Inclusión exacta de variables hexadecimales correspondientes a los verdes institucionales declarados en el portal oficial de Grupo Nutresa (`#114622`, `#215B33`, `#3D8E33`, `#7FBA00`).
2. **Propiedad Industrial Titularizada:** Exposición directa en metadatos y vistas de marcas registradas propiedad de Nutresa (Zenú, Noel, Doria, Ranchera, Ducales, Chocolisto, Jet).
3. **Suplantación de Entorno:** Generación de un entorno web que describe textualmente la plataforma como *"el recetario digital de Grupo Nutresa"*, crea un riesgo inminente de **Infracción marcaria** y **Competencia desleal por confusión** (regulado bajo normativas de propiedad industrial de la Comunidad Andina - Decisión 486, y leyes nacionales de marcas). Aunque el proyecto tenga la etiqueta de "ejercicio académico", su publicación en redes abiertas o plataformas de hosting público (como Vercel o GitHub) elimina la excepción de uso privado, exponiendo el software a la percepción pública como un producto oficial o autorizado.

### 7.3. Responsabilidades y Sanciones Consecuentes
El despliegue de esta interfaz y su vinculación explícita con marcas reales acarrea graves consecuencias jurídicas distribuidas en tres niveles de responsabilidad:

* **Para la Persona Natural (Diseñador/Programador que extrajo y aplicó la marca):**
  * **Sanciones Civiles y Económicas:** Demandas por indemnización de perjuicios causados a la reputación y el valor de marca del Grupo Nutresa, derivadas del uso de activos con fines de explotación o exhibición pública no autorizada.
  * **Acciones Penales:** Acciones penales asociadas al delito de usurpación de derechos de propiedad industrial y derechos de obtención de variedades vegetales (según el código penal aplicable), el cual sanciona a quien utilice fraudulentamente una marca registrada legítimamente.
* **Para la Institución Educativa:**
  * **Responsabilidad Institucional:** Demandas por omisión en el deber de supervisión académica y tutoría de proyectos. Las entidades de control educativo pueden imponer multas administrativas y la pérdida de registros calificados de los programas formativos por permitir que sus docentes promuevan prácticas violatorias de la propiedad intelectual.
* **Para los Aprendices / Desarrolladores dentro del Proyecto Académico:**
  * **Cancelación del Contrato de Aprendizaje:** El uso no autorizado de marcas de la empresa patrocinadora o de terceros dentro de un proyecto académico coordinado bajo la supervisión de la empresa/institución constituye una **falta grave** a las obligaciones contractuales de lealtad y confidencialidad. Esto faculta la terminación inmediata del contrato con justa causa, interrumpiendo el patrocinio económico y generando un veto permanente en el historial laboral corporativo.
  * **Sanciones Disciplinarias Académicas:** Procesos disciplinarios de expulsión definitiva de la institución educativa por plagio, infracción de derechos de autor y violación del código de ética del estudiante, inhabilitando la obtención del título técnico o profesional.

**Medida Correctiva Adoptada por esta Scrum Mastería:** Con el fin de blindar legalmente el proyecto, salvaguardar la integridad disciplinaria del desarrollador y respetar el principio de buena fe, **el módulo de la Célula 5 se declara completa e irreversiblemente neutral**. El software se redefine bajo la marca abstracta y genérica **"Sazón Independiente"**. Se elimina toda referencia literal a productos o marcas de Grupo Nutresa S.A., sustituyendo las paletas de colores y catálogos por denominaciones genéricas universales (ej. "Spaghetti Genérico", "Embutido de Res"). El código fuente no contendrá ningún elemento que induzca a la suplantación corporativa.

---

## 8. CONCLUSIONES Y REFLEXIÓN DE TRABAJO EN EQUIPO

### 8.1. Conclusiones del Desarrollo Técnico
La estructuración técnica del módulo de Requisitos demostró que la separación clara de responsabilidades (Separation of Powers) entre el estado del Frontend en React y el cómputo relacional de base de datos en Spring Boot es la única vía viable para garantizar un sistema escalable. El modelo relacional de 5 tablas diseñado provee el nivel de normalización exacto para mitigar anomalías de inserción y actualización. La introducción de la tabla de ítems con estados independientes (`comprado`) permite que la interacción del usuario en la tienda sea sumamente fluida sin comprometer la integridad histórica de los planes de menú generados en el backend.

### 8.2. Reflexión de Gestión (Scrum Master ante Células de Trabajo Inactivas)
*Nota del Autor/Scrum Master:* El ciclo de vida de este proyecto ha presentado una anomalía severa en su dimensión humana y organizativa. El equipo asignado está compuesto nominalmente por cinco (5) personas; sin embargo, debido a una ruptura total de los canales de comunicación interpersonales ("no se hablan entre ellos") y a un estado generalizado de apatía operativa ("nadie quiere hacer nada"), la totalidad de las actividades de preventa, ingeniería de requisitos, modelado relacional 3NF, codificación del backend en Spring Boot y maquetación en React han sido asumidas de forma **unipersonal** por el suscrito en calidad de Scrum Master y Coder de la célula.

Asumir la resiliencia del proyecto bajo este escenario de deserción funcional del equipo ha exigido la adopción pragmática de un rol de **"Scrum Master Extremo"**. Lejos de claudicar ante la disfunción de la célula, se ha tomado la decisión política y técnica de sacar adelante el software de forma independiente. Esta situación, si bien representa una sobrecarga de esfuerzo cognitivo, se transforma en una demostración empírica de capacidad técnica, disciplina de auto-gestión y liderazgo operacional. El proyecto Sazón - Célula 5 se entregará completo, funcional y con un estándar de calidad superior, demostrando que la determinación de un solo ingeniero de software es capaz de superar la inercia del abandono colectivo.

---

## 9. GLOSARIO

* **API REST (Representational State Transfer):** Interfaz de programación de aplicaciones que utiliza peticiones HTTP para transferir datos en formatos legibles, generalmente JSON.
* **JWT (JSON Web Token):** Estándar abierto basado en JSON para la creación de tokens de acceso que permiten la propagación segura de identidades y claims entre el cliente y el servidor.
* **Convención DDL (Data Definition Language):** Subconjunto del lenguaje SQL empleado para definir y modificar las estructuras de los objetos de la base de datos (tablas, índices, restricciones).
* **Normalización (3NF):** Proceso de optimización relacional que organiza las columnas y tablas de una base de datos para asegurar que las dependencias lógicas estén correctamente asignadas, eliminando la redundancia y protegiendo la integridad de los datos.
* **Scrum Master:** Facilitador de proyectos ágiles responsable de remover impedimentos, asegurar el cumplimiento de la metodología y guiar al equipo (o célula) hacia la consecución de los objetivos del Sprint.

---

## 10. BIBLIOGRAFÍA

* American Psychological Association. (2020). *Publication manual of the American Psychological Association* (7th ed.). https://doi.org/10.1037/0000165-000
* Date, C. J. (2003). *An Introduction to Database Systems* (8th ed.). Pearson Addison Wesley.
* Walls, C. (2022). *Spring in Action* (6th ed.). Manning Publications.
* Comunidad Andina de Naciones. (2000). *Decisión 486: Régimen Común sobre Propiedad Industrial*. Gaceta Oficial de la República.
