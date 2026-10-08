# Daily Calorie Planner

A single page calorie planner. Enter your weight, height, age, sex, activity level and goal to get:

* A daily eating target and a daily exercise burn target (Mifflin St Jeor equation)
* A meal by meal calorie split
* A daily log of meals and workouts, with progress against your goal and a 7 day view

Live site: https://anasali12-ui.github.io/Health-App/

## Run it

Open `index.html` in any browser. No build step or server needed.

## Calorie lookup

Type a food and tap **Look up calories**. The page checks several sources and logs the **highest** calorie value found, so meals are never undercounted. When a food comes in more than one size (small, medium, large and so on), it asks which size you had before logging.

* **On GitHub Pages or any website:** the lookup searches [USDA FoodData Central](https://fdc.nal.usda.gov/) (survey foods with household sizes, plus branded foods) and [Open Food Facts](https://world.openfoodfacts.org/).
  * It uses USDA's shared `DEMO_KEY` by default, which allows about 30 lookups an hour per device.
  * For more, get a free key at https://fdc.nal.usda.gov/api-key-signup and paste it into the key box under the lookup results. The key is stored only in your browser and is never committed to this repo (USDA deactivates keys found in public code).
* **Inside claude.ai:** the lookup asks Claude, which also covers chain restaurant menus, and falls back to the databases above.

## Where the data is kept

* Inside claude.ai, logs sync to your Claude account.
* Anywhere else, logs are saved in your browser.

## Disclaimer

Estimates for healthy adults, not medical advice.
