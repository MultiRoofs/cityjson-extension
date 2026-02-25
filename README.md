# CityJSON Extension for the MultiRoofs project

Dump from the deliverable 1.1.something:

## Computed from the 3D geometries
|                                | **who provides it** | **mandatory?**  |  **units**       | **name**         | **extra info** |
|:------------------------------ |:-------------------:|:---------------:|:----------------:|:----------------:|:--------------:|
| **Roof area**                  | tudelft             | yes             | m^2              | roof-area        | total of all RoofSurfaces |
| **Roof elevation**             | tudelft             | yes             | m                | roof-elevation   | which point do we use?    |
| **Roof compactness**           | tudelft             | yes             | (no units)       | roof-compactness | what formula? |
| **Roof slope**                 | tudelft             | yes             | degree           | roof-slope       | for each roof segment? or steepest? |
| **Building mass** (volume)     | tudelft             | yes             | m^3              | building-volume  |  |
| **Roof sun hours**             | mvrdv               | yes             | hours            | roof-sun-hours   | hours/day in what month?! |
| **Roof solar irradiance**      | mvrdv               | yes             | kWh/m2           | roof-irradiance  |  |
| **Good / Bad solar**           | mvrdv               | yes             | boolean          | roof-good-solar  | what the f is that? |



## Provided by the LAs for each building

|                                     | **mandatory?** | **units**       | **name**                    | **extra info** |
|:----------------------------------- |:--------------:|:---------------:|:---------------------------:|:--------------:|
| **Building year of construction**   | yes            | none            | building-year-construction  | |
| **Building foundation**             | yes            | none            | building-foundation         | |
| **Building type**                   | yes            | enum            | building-type               | which classification we use? |
| **Elevator presence**               | no             | boolean         | building-has-elevator       | |
| **Rooftop mass**                    | no             | kg?             | roof-mass                   | what is that? |

## Provided by the LAs for neighbourhoods

|                                       | **mandatory?** | **units** | **name**               | **extra info** | 
|:------------------------------------- |:--------------:|:---------:|:----------------------:|:---------------|
| **Roof existing color usage**         | R_R_usage        | -         | text    | Internally generated                          | Local      |
| **Maximum building height allowed**   |                  |           | number  | Bestemmingsplan                               |            |
| **URBAN PREFERENCES**                 |                  |           |         |                                               |            |
| **Roof view quality**                 | P_R_view         | degree    | number  | Internally generated                          | Local      |
| **Roof visibility**                   | P_R_visibility   | -         | -       | -                                             | -          |
| **Building function**                 | P_B_function     | -         | text    | Kadaster BAG                                  | National   |
| **Building energy label**             | P_B_energy       | label     | text    | RVO Bouwen Energielabels                      | National   |
| **Building heritage status**          | P_B_heritage     | -         | text    | Gemeente Rotterdam                            | Municipal  |
| **Building ownership**                | P_B_ownership    | -         | -       | -                                             | -          |
| **Monument status**                   |                  | binary    | number  | Kadaster BAG                                  | National   |
| **Zone noise disturbance**            |                  | dB        | number  | Atlas Leefomgeving                            |            |
| **Zone green corridor**               | P_Z_green        | m         | number  | Gemeente Rotterdam  <br>Ingenieursbureau      | Municipal  |
| **Zone flood risk**                   | P_Z_flood        | -         | text    | Gemeente Rotterdam  <br>Rotterdams Weerwoord  | Municipal  |
| **Zone stedelijke hitte-eiland effect**   | P_Z_heat         | degree C  | number  | RIVM Atlas Natuurlijk Kapitaal                | National   |
| **Zone heritage monumenten**              | P_Z_heritage     | -         | Text    | Rijksdienst voor het  <br>Cultureel Erfgoed   | National   |
| **Zone access to public transportation**  | P_Z_transport    | -         | Text    | Internally generated                          | Municipal  |
| **Zone access to public space**           | P_Z_pspace       | -         | number  | Gemeente Rotterdam  <br>Voetgangerskaart      | Municipal  |
| **Type of owner**                         |                  |           |         |                                               |            |
| **Expected renovation year**              |                  |           |         | Client data                                   |            |
| **Location**                              |                  |           |         | Client data                                   |            |
