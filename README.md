SmartGridAI — Smart Energy Microgrid & Demand Forecasting

Overview

SmartGridAI is a smart energy management prototype designed to forecast electricity demand and support intelligent grid-mode switching.

Problem Statement

Electricity demand changes throughout the day. Predicting demand and identifying high-load periods can help support better energy management and timely overload alerts.

Key Features

- Hourly electricity demand forecasting for the next 24 hours.
- QuickML-based demand prediction.
- Smart switching between Main Grid Mode and Renewable Storage Mode.
- Critical overload alerts for demand of 200 kW or higher.
- Interactive dashboard for predicted load, grid state, battery state of charge, and alerts.

Switching Logic

- If demand is above 160 kW or the time is between 18:00 and 22:00 inclusive, select Renewable Storage Mode.
- Otherwise, select Main Grid Mode.
- If demand is 200 kW or higher, trigger a Critical Overload Alert, regardless of the selected mode.

Project Files

- "predict.py" — Prediction interface for the published QuickML endpoint.
- "test_eval.py" — Pre-submission self-test.
- "train_telemetry.csv" — Training dataset.
- "sample_test_input.csv" — Sample prediction inputs.
- "PROBLEM_STATEMENT.md" — Project requirements.

Run the Self-Test

Install the required Python packages:

python -m pip install numpy pandas requests

Then run:

python test_eval.py

Model and Deployment

The prediction script is configured to use a Zoho Catalyst QuickML endpoint. The web dashboard and deployment must be completed and verified before the project is considered fully deployed.

Status

Prototype in development for HackSphere 3.0.
