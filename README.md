[![View Site](https://img.shields.io/badge/Live_Site-Visit-blue)](https://ardriaxv.github.io/BGS-Impact-Predictor)

Real Time BGS Impact Predictor
A lightweight, browser based Elite Dangerous Background Simulation forecaster

Overview
The Real Time BGS Impact Predictor is a fully client side HTML tool designed to help Elite Dangerous players and squadrons estimate how their daily actions will affect faction influence at the next BGS tick.

It provides:

Real time influence forecasting

State aware activity modelling

Soft cap influence simulation

Scenario planning (e.g., “What if we run 20 more missions?”)

A clean, responsive UI with no backend required

This tool is ideal for squadrons who want a fast, transparent way to understand how their work impacts the BGS without relying on external APIs or server side processing.

Features

🔹 Influence Prediction

Calculates predicted influence for up to three factions

Normalises influence to 100% (as in the real BGS)

Applies soft caps to prevent unrealistic swings

Uses state based multipliers (War, Boom, Election, etc.)

🔹 Activity Modelling

Supports the main BGS relevant actions:

Missions

Combat bonds / bounties

Trade profit or loss

Exploration data (cartographics)

Each action is converted into a unified pressure value.

🔹 Scenario Planner

Add hypothetical extra work (e.g., more missions) and instantly see:

Scenario influence

Additional swing

Risk indicators (conflict, retreat, expansion)

🔹 Zero Dependencies

100% client side

No frameworks

No external libraries

Works offline

Project Structure
Code
/
├── index.html        # Main application (UI + logic)
├── README.md         # Project documentation
└── LICENSE           # Optional license file
Everything is contained in index.html — HTML, CSS, and JavaScript.

How the Model Works
The predictor uses a simplified but realistic BGS model:

1. Action → Pressure Conversion
Each activity type is converted into “pressure” using logarithmic scaling.

2. Population Scaling
High population systems require more work to move influence.

3. State Modifiers
States like War, Boom, Election, etc. adjust the effectiveness of actions.

4. Soft Caps
Influence movement is limited to a realistic range (approx. ±6%).

5. Normalisation
Predicted influence is normalised so all factions sum to 100%.

This keeps the model transparent and predictable while still reflecting real BGS behaviour.

Usage
Open index.html in any modern browser.

Enter:

System name

Population

Faction names, states, and current influence

Today’s activity for each faction

(Optional) Add scenario activity

Click Predict Tick Outcome

Review:

Predicted influence

Scenario influence

Risk indicators

System pressure

Net swing

No installation required.

Code
![Screenshot](images/screenshot.png)
Development
Everything is contained in a single HTML file.
To modify the tool:

UI → Edit the HTML structure

Styling → Modify the <style> block

Logic → Edit the JavaScript at the bottom of the file

No build steps, no dependencies.

Contributing
Contributions are welcome!

Ideas for improvement:

Multi system support

More factions

Import/export JSON

Integration with EDMC or journals

Graphing influence over time

Calibration tools

To contribute:

Fork the repo

Create a feature branch

Commit your changes

Open a pull request

Star the repository

Share it with your squadron

Submit ideas or improvements

© 2026 D. Hughson. All rights reserved.
