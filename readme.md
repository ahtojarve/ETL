DATA

Metadata about air quality
http://airviro.klab.ee/

| Attr  | example value | unit    | Description                 |
| ----- | ------------- | ------- | --------------------------- |
| SO2   | 0,23          | µg/m³ | Vääveldioksiid            |
| NO2   | 0,02          | µg/m³ | Lämmastikdioksiid          |
| CO    | 0,24          | mg/m³  | Süsinikoksiid              |
| O3    | 70,05         | µg/m³ | Osoon                       |
| PM10  | 8,55          | µg/m³ | Peened osakesed             |
| PM2.5 | 4,72          | µg/m³ | Eriti peened osakesed       |
| TEMP  | 9,72          | C       | Temperatuur                 |
| WD10  | 204,40        | deg     | Tuule suund 10 m kõrgusel  |
| WS10  | 1,56          | m/s     | Tuule kiirus 10 m kõrgusel |

Process:

* Using Python script extract data from http://airviro.klab.ee/ (fetch_air.ipynb).
* Using Openrefine transform columns into correct format(use data_transform_steps.json)
* Using Openrefine export SQL that can be imported to any SQL based database.
* Create a sqlite3 database
* Create a table into database using air-2022-database-script.sql
* Using Python script create daily average table from existing table (create_daily.ipynb)
* Using Python script create monthly average table from existing table (create_monthly.ipynb)
