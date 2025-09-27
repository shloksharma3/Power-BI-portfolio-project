# Power-BI-portfolio-project
This repository contains a Power BI project (.pbix file) focused on data analysis and dashboarding for plant metrics.

1. Data Model
This is the backbone of the project. It contains all the data that has been imported and organized into a structured format.
Tables: The model likely includes tables such as ProductionData, MachineMaintenance, QualityControl, EmployeeShifts, and EnergyConsumption.
Relationships: These tables are interconnected through relationships. For example, the ProductionData table might be linked to the MachineMaintenance table by a MachineID, allowing you to analyze how maintenance events impact production output.
Data Types & Formatting: Each column in every table is assigned a specific data type (e.g., number, date, text) and formatted for clarity.


2. Power Query (Data Transformation - ETL)
Before the data enters the model, it is cleaned and shaped using Power Query. This is the "Extract, Transform, Load" (ETL) layer of the project.
Data Sources: The project connects to one or more raw data sources (which could be Excel files, CSVs, a SQL database, etc.).
Transformation Steps: A series of steps are applied to clean the data, such as removing errors, splitting columns, handling missing values, and unpivoting data to make it suitable for analysis. These steps are saved within the file and are reapplied every time the data is refreshed.


3. DAX Calculations (Measures and Calculated Columns)
Data Analysis Expressions (DAX) are formulas used to create powerful, custom calculations that provide business insights. This is where the core analytical logic resides.
Measures: These are dynamic calculations that respond to user interactions. Examples in this project might include:
Total Production Units = SUM(ProductionData[UnitsProduced])
Overall Equipment Effectiveness (OEE) = [Availability] * [Performance] * [Quality]
Average Downtime = AVERAGE(MachineMaintenance[DowntimeHours])
Calculated Columns: These are new columns added to a table based on a DAX formula, such as creating a "Pass/Fail" category based on a quality score.



5. Report View (Visualizations & Dashboard)
This is the front-end of the project—the interactive report that users see. It consists of one or more pages with various visuals that display the data from the model and the DAX measures.
Visuals: The dashboard likely uses a combination of charts, graphs, and cards to tell a story. This could include:
KPI Cards: To show critical metrics like OEE, Total Production, and Costs.
Line Charts: To track production trends over time.
Bar Charts: To compare the performance of different machines or shifts.
Pie/Donut Charts: To show the proportion of downtime reasons.
Tables and Matrices: For detailed, granular views of the data.
Interactivity: The report is interactive. Users can click on a visual element (like a specific machine in a bar chart) to filter the entire report page, or use Slicers to filter the data by date, shift, or plant location.
