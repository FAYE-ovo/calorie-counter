# Calorie Counter

A simple, clean food energy calculator. Enter protein, fat, and carbs to instantly calculate calories using the Atwater factors (4-9-4 kcal/g).

## Live Demo

https://faye-ovo.github.io/calorie-counter/

## Features

- **Instant Calculation** — Real-time calorie computation as you type
- **40+ Food Presets** — Common fitness foods with realistic portion sizes (half palm, 1 bowl, 1 egg, etc.)
- **Food Search** — Real-time search within the current language (Chinese or English), with quick-add when no results found
- **Custom Foods** — Save your own foods for quick reuse, pin favorites to top, right-click to manage
- **Exercise Burn** — Compare intake vs. 20 exercises (MET-based, strength training split into light/moderate/vigorous), multi-row accumulator for combined workouts, exercise descriptions on hover, MET hint, with Pac-Man chomp and lightning bolt icons
- **BMR Tracking** — Set your gender/height/weight/age, see intake vs. daily needs progress bar with dynamic gradient (light at low intake, deep at goal)
- **Food Accumulator** — Add multiple foods in the panel, see total kcal before filling into the calculator
- **kJ ↔ kcal Converter** — Built-in unit conversion, collapsed by default
- **Bilingual** — Chinese / English toggle, all labels, food names, exercise names, and descriptions switch together
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

The progress bar fills based on intake / BMR ratio with a dynamic gradient: colors shift from light amber (low intake) to deep warm brown (approaching goal). The gradient spans the full track width, so only the light portion is visible at low fill. Default reference: 2000 kcal.

## Exercise Burn Calculation

The exercise section uses MET (Metabolic Equivalent of Task) values to estimate calories burned:

Calories = MET × weight(kg) × duration(h)

- 20 exercises included: brisk walking, jogging, running, cycling, swimming (leisure & freestyle), weight training (light/moderate/vigorous), circuit training, HIIT (moderate/vigorous), jump rope, yoga, basketball, badminton, hiking, rowing, dancing, boxing
- Weight is taken from personal settings (default: 65 kg)
- Pac-Man icon: mouth opens wide at 0 intake, closes as intake approaches daily goal. Chomp animation (close → open) plays when intake value changes
- Lightning bolt icon: trembles 3× when exercise type or duration changes (not on intake change)
- Exercise descriptions: hover any exercise dropdown to see a brief explanation (bilingual)
- MET hint line below exercise list: "MET = exercise intensity · walking≈3 · jogging≈8 · sprint≈10"
- Multi-row accumulator: add multiple exercises, total burn = sum of all rows
- Intake and burn bars scale proportionally to the larger value; net calories shown below

## Usage

1. Open `index.html` in any browser, or visit the live demo link above
2. Enter protein, fat, and carbs in grams (use Enter key to jump between fields)
3. Total calories update instantly with a progress bar showing intake vs. BMR
4. **Food selection**: Click "Select Common Foods" to browse presets by category, or use the search bar to find foods instantly
5. **Custom foods**: Switch to the Custom tab to add your own foods — save for reuse or add once
6. **Personal settings**: Click the gear icon to set gender/height/weight/age for BMR calculation
7. **Exercise comparison**: Expand "Exercise Burn" to select an exercise and duration. Click "+ Add Exercise" to add more rows — total burn is the sum of all exercises. See intake vs. burn bars side by side
8. **Unit conversion**: Expand the kJ ↔ kcal converter for quick energy unit conversion

Works on desktop, mobile, and tablet — any device with a browser.

## Tech Stack

- Pure HTML / CSS / JavaScript (no frameworks, no dependencies)
- Single file, self-contained
- SVG favicon (no image files needed)
- localStorage for user settings and custom foods

## License

MIT
