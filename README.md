# CityJSON Extension for the MultiRoofs project


## Computed from the 3D geometries
|                                | **who?** | **mandatory?**  |  **units**       | **name**         | **extra info**                      |
|:------------------------------ |:--------:|:---------------:|:----------------:|:----------------:|:-----------------------------------:|
| **Roof area**                  | tudelft  | yes             | m^2              | roof-area        | total of all RoofSurfaces |
| **Roof elevation**             | tudelft  | yes             | m                | roof-elevation   | which point do we use?    |
| **Roof compactness**           | tudelft  | yes             | (no units)       | roof-compactness | what formula? |
| **Roof slope**                 | tudelft  | yes             | degree           | roof-slope       | for each roof segment? or steepest? |
| **Building mass** (volume)     | tudelft  | yes             | m^3              | building-volume  |  |
| **Roof sun hours**             | mvrdv    | yes             | hours            | roof-sun-hours   | hours/day in what month?! |
| **Roof solar irradiance**      | mvrdv    | yes             | kWh/m2           | roof-irradiance  |  |
| **Good / Bad solar**           | mvrdv    | yes             | boolean          | roof-good-solar  | what the f is that? |



## Provided by the LAs for each building

|                                     | **who?** | **mandatory?** | **units**   | **name**                    | **extra info** |
|:----------------------------------- |:--------:|:--------------:|:-----------:|:---------------------------:|:--------------:|
| **Building year of construction**   | each LA  | yes            | none        | building-year-construction  | |
| **Building foundation**             | each LA  | yes            | none        | building-foundation         | |
| **Building type**                   | each LA  | yes            | enum        | building-type               | which classification we use? |
| **Building function**               | each LA  | yes            | enum        | building-function           | which classification we use? |
| **Elevator presence**               | each LA  | no             | boolean     | building-has-elevator       | |
| **Rooftop mass**                    | each LA  | no             | kg?         | roof-mass                   | what is that? |
| **Building energy label**           | each LA  |                |             | building-energy-label       | |
| **Building heritage status**        | each LA  |                |             | building-heritage           | |
| **Building monument status**        | each LA  | yes            | boolean     | building-monument           | |
| **Building ownership**              | each LA  |                |             | building-ownership          | |
| **Maximum building height allowed** | each LA  |                | meter       | building-max-height         | | 
| **Roof visibility**                 | each LA  |                |             |                             | |
| **Roof view quality**               | each LA  |                |             |                             | |



## Provided by the LAs for neighbourhoods ("urban preferences" called in RoofScape)

|                                       | **who?** | **mandatory?** | **units** | **name**               | **extra info** | 
|:------------------------------------- |:--------:|:--------------:|:---------:|:----------------------:|:--------------:|
| **Zone heritage monumenten**          | each LA  |                |           |                        | |             
| **Zone noise disturbance**            | each LA  |                |  dB       |                        | |             

## Stuff that should be cleaned:

|||||||
|:------------------------------------- |:--------:|:--------------:|:---------:|:----------------------:|:--------------:|
| **Zone noise disturbance**                |                  | dB        | number  | Atlas Leefomgeving                            |            |
| **Zone green corridor**                   | P_Z_green        | m         | number  | Gemeente Rotterdam  <br>Ingenieursbureau      | Municipal  |
| **Zone flood risk**                       | P_Z_flood        | -         | text    | Gemeente Rotterdam  <br>Rotterdams Weerwoord  | Municipal  |
| **Zone stedelijke hitte-eiland effect**   | P_Z_heat         | degree C  | number  | RIVM Atlas Natuurlijk Kapitaal                | National   |
| **Zone access to public transportation**  | P_Z_transport    | -         | Text    | Internally generated                          | Municipal  |
| **Zone access to public space**           | P_Z_pspace       | -         | number  | Gemeente Rotterdam  <br>Voetgangerskaart      | Municipal  |
| **Type of owner**                         |                  |           |         |                                               |            |
| **Expected renovation year**              |                  |           |         | Client data                                   |            |
| **Location**                              |                  |           |         | Client data                                   |            |
| **Roof existing color usage**         | R_R_usage        | -         | text    | Internally generated                          | Local      |
