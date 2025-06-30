# Daikibo Telemetry Data Analysis (Tableau)

This project analyzes telemetry data collected by Daikibo to identify and visualize downtime.

## Project Goal
The primary objective was to calculate and visualize potential downtime per factory and per device type, and to create an interactive dashboard for exploring these insights.

## Data Source
The analysis uses daikibo-telemetry-data.json, which contains telemetry logs.

## Tools Used
* Tableau Desktop Public Edition

## Analysis Steps
1.  *Data Import:* Connected to the daikibo-telemetry-data.json file in Tableau.
2.  *Calculated Field - 'Unhealthy'*: Created a calculated field to represent downtime: IF [Status] = 'unhealthy' THEN 10 ELSE 0 END. (Each 'Unhealthy' status represents 10 minutes of potential downtime).
3.  *Chart 1 - Down Time per Factory*: A bar chart showing the sum of 'Unhealthy' minutes for each factory.
4.  *Chart 2 - Down Time per Device Type*: A bar chart showing the sum of 'Unhealthy' minutes for each device type.
5.  *Interactive Dashboard*: Combined both charts into a dashboard, enabling filtering where selecting a factory in the 'Down Time per Factory' chart filters the 'Down Time per Device Type' chart.

## Key Insights
* seiko named factory showed the highest downtime.
* LaserWelder device was a significant contributor to downtime.
* commonly four devices are high with down time : Furnace, HeavyDutyDrill, LaserWelder, LaserCutter.

## How to View
* *Interactive Dashboard:* You can view the interactive dashboard on https://public.tableau.com/views/book1_17512683824790/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link.



