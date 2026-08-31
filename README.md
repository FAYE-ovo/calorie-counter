# Calorie Counter

A simple, clean food energy calculator. Enter protein, fat, and carbs to instantly calculate calories using the Atwater factors (4-9-4 kcal/g).

## Live Demo

https://faye-ovo.github.io/calorie-counter/

## Features

- **Instant Calculation** — Real-time calorie computation as you type
- **40+ Food Presets** — Common fitness foods with realistic portion sizes (half palm, 1 bowl, 1 egg, etc.)
- **Food Search** — Real-time search across all food categories (Chinese & English), with quick-add when no results
- **Custom Foods** — Save your own foods for quick reuse, pin favorites to top
- **Exercise Burn** — Compare intake vs. 15 common exercises (MET-based), with Pac-Man and lightning bolt icons
- **BMR Tracking** — Set your gender/height/weight/age, see intake vs. daily needs progress bar
- **Food Accumulator** — Add multiple foods in the panel, see total kcal before filling into the calculator
- **kJ ↔ kcal Converter** — Built-in unit conversion, collapsed by default
- **Bilingual** — Chinese / English toggle, all labels and food names switch together
- **Privacy-First** — All data stored locally in your browser (localStorage), no server, no tracking, no account needed

## How It Works

The Atwater system uses fixed energy factors per gram of macronutrient:

| Nutrient | Factor |
|----------|--------|
| Protein | 4 kcal/g |
| Fat | 9 kcal/g |
| Carbohydrate | 4 kcal/g |

Total Energy = Protein × 4 + Fat × 9 + Carbs × 4

## BMR Calculation

Uses the Mifflin-St Jeor equation:

- **Male**: BMR = 10 × weight(kg) + 6.25 × height(cm) - 5 × age + 5
- **Female**: BMR = 10 × weight(kg) + 6.25 × height(cm) - 5 × age - 161

The progress bar fills based on intake / BMR ratio. Default reference: 2000 kcal.

## Exercise Burn Calculation

The exercise section uses MET (Metabolic Equivalent of Task) values to estimate calories burned:

Calories = MET × weight(kg) × duration(h)

- 15 exercises included (brisk walking, jogging, running, cycling, swimming, weight training, HIIT, etc.)
- Weight is taken from personal settings (default: 65 kg)
- Pac-Man icon mouth opens/closes based on intake ratio (open = low intake, closed = full)
- Lightning bolt icon trembles when exercise type or duration changes

## Usage

1. Open `index.html` in any browser, or visit the live demo link above
2. Enter protein, fat, and carbs in grams (use Enter key to jump between fields)
3. Total calories update instantly
4. Optional: Click "Select Common Foods" to pick from presets
5. Optional: Click the gear icon to set personal BMR data

Works on desktop, mobile, and tablet — any device with a browser.

## Tech Stack

- Pure HTML / CSS / JavaScript (no frameworks, no dependencies)
- Single file, self-contained
- SVG favicon (no image files needed)

## License

MIT
