Cell 5 — User Histories

For Cell 5, the user histories should be written from the perspective of the user and describe a concrete interaction or need that the system must satisfy.

HU-5.1 — Consultar información de una receta

Como usuario registrado,
quiero consultar la información detallada de una receta,
para conocer sus ingredientes, preparación e información nutricional antes de incluirla en mi planificación semanal.

Acceptance Criteria:

The user can open a recipe from the recipe catalog.
The system displays the recipe name and description.
The system displays the required ingredients.
The system displays the preparation instructions.
The system displays available nutritional information.
The recipe can be added to the user's weekly menu.
HU-5.2 — Agregar una receta al plan semanal

Como usuario registrado,
quiero agregar una receta a un día y momento de comida de mi semana,
para organizar anticipadamente mis comidas.

Acceptance Criteria:

The user can select a day of the week.
The user can select a meal type, such as breakfast, lunch, dinner, or snack.
The user can assign a recipe to that slot.
The system saves the menu assignment.
The assigned recipe is displayed in the weekly planner.
The user can modify or remove the assignment.
HU-5.3 — Generar lista de mercado

Como usuario registrado,
quiero generar automáticamente una lista de mercado a partir de las recetas de mi menú semanal,
para conocer los ingredientes que necesito comprar.

Acceptance Criteria:

The system analyzes the recipes assigned to the weekly menu.
The system consolidates repeated ingredients.
Ingredients are grouped by category when applicable.
The generated list displays the required quantities.
The user can mark an ingredient as purchased.
The system preserves the purchased status.
HU-5.4 — Descontar productos disponibles en la despensa

Como usuario registrado,
quiero que los ingredientes que ya tengo disponibles sean descontados de mi lista de mercado,
para evitar compras innecesarias.

Acceptance Criteria:

The user can register ingredients available in their pantry.
The system compares pantry quantities with menu requirements.
Available quantities are subtracted from the required quantities.
Only the remaining quantities are included in the shopping list.
Ingredients with sufficient available quantities do not appear as pending purchases.
HU-5.5 — Marcar productos como comprados

Como usuario registrado,
quiero marcar los productos de mi lista de mercado como comprados,
para llevar un control de las compras necesarias para mi planificación.

Acceptance Criteria:

Each shopping-list item has a purchased status.
The user can mark an item as purchased.
The user can undo the purchased status.
The system persists the status.
Purchased and pending items can be visually distinguished.
HU-5.6 — Modificar el menú semanal

Como usuario registrado,
quiero modificar las recetas asignadas a mi menú semanal,
para adaptar mi planificación a cambios de disponibilidad, preferencias o necesidades.

Acceptance Criteria:

The user can replace an assigned recipe.
The user can remove a recipe.
The user can move a recipe to another day or meal.
The system updates the weekly menu.
The shopping list can be recalculated according to the updated menu.
