# Fitness and Nutrition Tracker

A command-line app to log workouts and meals, import entries from files, and see charts of your calories.

## Features

- Create and switch between user profiles (weight, height, fitness goal)
- Add workout and meal entries by hand
- Import entries from CSV or XML files
- View all your entries
- Chart: meal category distribution for a chosen month
- Chart: calories consumed vs. calories burned per day

## Requirements

- Python 3
- matplotlib

```
pip install matplotlib
```

## How to run

```
python FitnessandNutritionsTrack.py
```

Enter a profile name to start. A new profile is created if the name doesn't exist yet.

## Menu

| Option | What it does |
|---|---|
| 1 | Change profile |
| 2 | View your profile |
| 3 | Edit your profile |
| 4 | View all entries |
| 5 | Add a new entry |
| 6 | Import entries from CSV |
| 7 | Import entries from XML |
| 8 | Chart: meal distribution |
| 9 | Chart: calories consumed vs. burned |
| 0 | Exit |

## Entry fields

| Field | Description |
|---|---|
| type | `Workout` or `Meal` |
| category | Workout: Cardio, Strength, Aerobic, Flexibility. Meal: Breakfast, Brunch, Lunch, Dinner, Snack. You can also type your own. |
| duration_quantity | Duration of the workout or quantity of the meal |
| calories | Calories burned (workout) or consumed (meal) |
| date | Format `YYYY-MM-DD` |

## Import file formats

**CSV** (with a header row):

```
type,category,duration_quantity,calories,date
Workout,Cardio,30 min,250,2025-01-10
Meal,Lunch,1 plate,600,2025-01-10
```

**XML**:

```
<entries>
  <entry>
    <type>Meal</type>
    <category>Dinner</category>
    <duration_quantity>1 plate</duration_quantity>
    <calories>700</calories>
    <date>2025-01-10</date>
  </entry>
</entries>
```

## Notes

- Data is kept in memory only, so entries are lost when the program closes. Import a file again to reload them.
- Charts open in a window and close automatically after a few seconds.

## Built with

Python · matplotlib · csv · xml.etree.ElementTree · datetime
