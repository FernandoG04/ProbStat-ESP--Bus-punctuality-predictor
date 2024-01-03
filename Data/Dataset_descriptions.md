## Datasets

### List of Datasets

1. **STM Bus Dataset**:

   - **Description:** Two datasets containing STM bus-related data. The first dataset contains data from October 2021 to December 2022, and the second dataset contains data from January 2023 to September 2023. 

   - **Data Dictionary:** 
   
      | Column Name | Format       | Description                                  |
      | ----------- | ------------ | -------------------------------------------- |
      | `date`      | `YYYY/MM/DD` | Date of the data point                       |
      | `ligne`     | `int`        | Bus line number                              |
      | `dir`       | `str`        | Direction of the bus (Nord, Sud, Est, Ouest) |
      | `id_voy`    | `str`        | Trip ID                                      |
      | `dep_pl`    | `HH:MM:SS`   | Scheduled departure time                     |
      | `dep_rl`    | `HH:MM:SS`   | Real departure time                          |
      | `arr_pl`    | `HH:MM:SS`   | Scheduled arrival time                       |
      | `arr_rl`    | `HH:MM:SS`   | Real arrival time                            |


   - **Source:** This data was provided by the Société de Transport de Montréal under the terms of the *Act respecting access to documents held by public bodies and the protection of personal information (R.S.Q., chapter A-2.1)*. [For more information, go to the STM site.](https://www.stm.info/en/about/corporate-governance/access-information)

   - **Format:** CSV

   - **Files:** [`STM_Data_2021_2022.csv`](../Data/Transit%20data/STM_Data_2021_2022.csv)   , [`STM_Data_2023.csv`](../Data/Transit%20data/STM_Data_2023.csv)
   
<br>

2. **Weather Dataset**

   - **Description:** Datasets containing Montreal weather data from the Airport-Trudeau station, from October 2021 to September 2023. The data is split into two datasets, one containing daily weather data, and the other containing hourly weather data.

   - **Data Dictionary:**  

      | Column Name | Format       | Description                                      | Data Frequency |
      | ----------- | ------------ | ------------------------------------------------ | -------------- |
      | `date`      | `YYYY-MM-DD` | Date of the data point                           | D/H            |
      | `time`      | `HH:MM`      | Time of the data point                           | H              |
      | `temp`      | `float`      | Temperature in degrees Celsius                   | H              |
      | `precip`    | `float`      | Precipitation in mm                              | H              |
      | `snow`      | `float`      | Total snow on ground in cm                       | D              |
      | `snow_yn`   | `str`        | Whether there is snow on the ground or not (Y/N) | D              |

   - **Source:** This data was retrieved from Environment and Climate Change Canada and is searchable on [their site](https://climate.weather.gc.ca/historical_data/search_historic_data_e.html).   

> [!NOTE]
> This dataset is preprocessed for the purpose of this project. The original dataset contains more information. The method of retrieving the data is described in the ["Weather data"](/Notebooks/3_1_2_Weather.ipynb) notebook.

   - **Format:** CSV
   - **Files:** [`daily_montreal_weather.csv`](../Data/Weather%20Data/daily_montreal_weather.csv) , [`hourly_montreal_weather.csv`](../Data/Weather%20Data/hourly_montreal_weather.csv)

<br>

3. **Traffic Dataset**

   - **Description:** Dataset containing Montreal  traffic-related data from November 26, 2019 to September 9, 2023.

   - **Data Dictionary (from source):**  
   
      | Column Name               | Format       | Description                                                      |
      | ------------------------- | ------------ | ---------------------------------------------------------------- |
      | `Id_Reference`            | `int`        | Unique identifier for each count                                 |
      | `Id_Intersection`         | `int`        | Intersection ID                                                  |
      | `Nom_Intersection`        | `str`        | Name of the intersection                                         |
      | `Date`                    | `YYYY-MM-DD` | Date of the count                                                |
      | `Periode`                 | `HH:MM:SS`   | Counting period                                                  |
      | `Heure`                   | `int`        | Start hour of the counting period                                |
      | `Minute`                  | `int`        | Start minute of the counting period                              |
      | `Seconde`                 | `int`        | Start second of the counting period                              |
      | `Code_Banque`             | `int`        | Number code classification of vehicles, pedestrians, and bikes   |
      | `Description_Code_Banque` | `str`        | Description of code_banque                                       |
      |                           |              | Possible values:                                                 |
      |                           |              | - `0`: Autos                                                     |
      |                           |              | - `1`: Light trucks                                              |
      |                           |              | - `2`: Heavy trucks                                              |
      |                           |              | - `10`: Pedestrians                                              |
      |                           |              | - `11`: Bicycles                                                 |
      |                           |              | - `12`: Bus                                                      |
      |                           |              | - `13`: School                                                   |
      |                           |              | - `14`: Trucks                                                   |
      |                           |              | - `15`: Truck carriers                                           |
      |                           |              | - `16`: Articulated trucks                                       |
      |                           |              | - `17`: Motorcycles                                              |
      |                           |              | - `20`: Not Used                                                 |
      |                           |              | - `21`: U-turns                                                  |
      |                           |              | - `22`: Illegal                                                  |
      |                           |              | - `40`: Others                                                   |
      |                           |              | - `100`: All                                                     |
      | `NBLT`                    | `int`        | Vehicle count, North Bound Left Turn                             |
      | `NBT`                     | `int`        | Vehicle count, North Bound Thru                                  |
      | `NBRT`                    | `int`        | Vehicle count, North Bound Right Turn                            |
      | `SBLT`                    | `int`        | Vehicle count, South Bound Left Turn                             |
      | `SBT`                     | `int`        | Vehicle count, South Bound Thru                                  |
      | `SBRT`                    | `int`        | Vehicle count, South Bound Right Turn                            |
      | `EBLT`                    | `int`        | Vehicle count, East Bound Left Turn                              |
      | `EBT`                     | `int`        | Vehicle count, East Bound Thru                                   |
      | `EBRT`                    | `int`        | Vehicle count, East Bound Right Turn                             |
      | `WBLT`                    | `int`        | Vehicle count, West Bound Left Turn                              |
      | `WBT`                     | `int`        | Vehicle count, West Bound Thru                                   |
      | `WBRT`                    | `int`        | Vehicle count, West Bound Right Turn                             |
      | `Approche_Nord`           | `str`        | Pedestrian or bike count, crosses north side of intersection     |
      | `Approche_Sud`            | `str`        | Pedestrian or bike count, crosses south side of intersection     |
      | `Approche_Est`            | `str`        | Pedestrian or bike count, crosses east side of intersection      |
      | `Approche_Ouest`          | `str`        | Pedestrian or bike count, crosses west side of intersection      |
      | `Localisation_X`          | `float`      | Location X in Québec Modified Transverse Mercator Zone 8 (NAD83) |
      | `Localisation_Y`          | `float`      | Location Y in Québec Modified Transverse Mercator Zone 8 (NAD83) |
      | `Longitude`               | `float`      | Longitude in WGS 84                                              |
      | `Latitude`                | `float`      | Latitude in WGS 84                                               |

   - **Source:** This dataset was retrieved from the data collection [Comptages des véhicules, cyclistes et piétons aux intersections munies de feux de circulation](https://donnees.montreal.ca/dataset/comptage-vehicules-pietons) from the City of Montreal's Open Data Portal.
   - **Format:** CSV
   - **File:** [`traffic_data.csv`](../Data/Traffic%20Data/traffic_data.csv)

<br>

4. **Master Datasets**

   - **Description:** Datasets containing the master data for the project. The master dataset for the first attempt merges the STM bus dataset with the weather dataset. The master dataset for the second attempt merges the STM bus dataset with the weather dataset and the traffic dataset.  

   > [!NOTE]
   > The master datasets are created in the Appendices of the notebooks. See [Appendix A.1: Bus Data](/Notebooks/6_1_1_Bus.ipynb), [Appendix A.2: Weather Data](/Notebooks/6_1_2_Weather.ipynb), [Appendix A.3: Traffic Data](/Notebooks/6_1_3_Traffic.ipynb)

   - **Format:** CSV
   - **Files:** [`master_data.csv`](../Data/master_data.csv) , [`master_data_traffic.csv`](../Data/master_data_traffic.csv) 
   