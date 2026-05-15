# CityJSON Extension for the MultiRoofs project


## Computed from the 3D geometries
|                                | **who?** | **mandatory?**  |  **units**       | **name**         | **extra info**                      |
|:------------------------------ |:--------:|:---------------:|:----------------:|:----------------|:-----------------------------------|
| **Roof total area**            | tudelft  | yes             | m^2              | roof-total-area  | total of all RoofSurfaces |
| **Roof elevation**             | tudelft  | yes             | m                | roof-elevation   | which point do we use? MVRDV:Average Z-value of all vertices   |
| **Roof compactness**           | tudelft  | yes             | (no units)       | roof-compactness | what formula? MVRDV:Rooftop_Area / Rooftop_Perimeter-Length |
| **Roof slope**                 | tudelft  | yes             | degree           | roof-slope       | for each roof segment? or steepest? MVRDV:We used to calc for each segment, since we stored each segment as sub-roof |
| **Building mass** (volume)     | tudelft  | yes             | m^3              | building-volume  |  |
| **Roof sun hours**             | mvrdv    | yes             | hours            | roof-sun-hours   | hours/day in what month?! MVRDV:Full day, 21st March |
| **Roof solar irradiance**      | mvrdv    | yes             | kWh/m2           | roof-irradiance  | MVRDV:Calculated for entire year |
| **Good / Bad solar**           | mvrdv    | yes             | boolean          | roof-good-solar  | what the f is that? MVRDV:Boolean to speed up calculations. Threshold unclear|



## Provided by the LAs for each building

|                                     | **who?** | **mandatory?** | **units**   | **name**                    | **extra info** |
|:----------------------------------- |:--------:|:--------------:|:-----------:|:--------------------------- |:-------------- |
| **Building year of construction**   | each LA  | yes            | none        | building-year-construction  | |
| **Building foundation**             | each LA  | yes            | none        | building-foundation         | |
| **Building type**                   | each LA  | yes            | enum        | building-type               | which classification we use? MVRDV:Needs collective review |
| **Building function**               | each LA  | yes            | enum        | building-function           | which classification we use? MVRDV:Needs collective review|
| **Elevator presence**               | each LA  | no             | boolean     | building-has-elevator       | |
| **Rooftop mass**                    | each LA  | no             | kg?         | roof-mass                   | what is that? |
| **Building energy label**           | each LA  | MVRDV:no       |             | building-energy-label       | |
| **Building heritage status**        | each LA  | MVRDV:no       |             | building-heritage           | |
| **Building monument status**        | each LA  | yes            | boolean     | building-monument           | |
| **Building ownership**              | each LA  | MVRDV:no       |             | building-ownership          | |
| **Maximum building height allowed** | each LA  | MVRDV:no       | meter       | building-max-height         | | 
| **Roof visibility**                 | each LA  | MVRDV:no       |             |                             | MVRDV:supposed to measure how visible a roof is from the ground. never implemented|
| **Roof view quality**               | each LA  | MVRDV:yes      | MVRDV:degree| MVRDV:building-views        | MVRDV:internally generated from 3d model. measures number of unobstructed views from center of roof |



## Provided by the LAs for neighbourhoods ("urban preferences" called in RoofScape)

|                                       | **who?** | **mandatory?** | **units** | **name**               | **extra info** | 
|:------------------------------------- |:--------:|:--------------:|:---------:|:----------------------:|:--------------:|
| **Zone heritage monumenten**          | each LA  |  MVRDV:No      | MVRDV:bool|                        | |             
| **Zone noise disturbance**            | each LA  |  MVRDV:No      | dB        |                        | |             

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
