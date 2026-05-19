# CityJSON Extension for the MultiRoofs project


## Computed from the 3D geometries
| |                                | **who?** | **mandatory?**  |  **units**       | **name**          | **extra info**                    |
|-|:------------------------------ |:--------:|:---------------:|:----------------:|:-----------------|:-----------------------------------|
| | **Roof total area**            | tudelft  | yes             | m^2              | roof-total-area   | total of all RoofSurfaces |
| | **Roof elevation**             | tudelft  | yes             | m                | roof-elevation    | which point do we use? median or 70-percentile|
| | **Roof compactness**           | tudelft  | yes             | (no units)       | roof-compactness  | (rooftop-total-area / rooftop-perimeter) |
| | **Roof slope**                 | tudelft  | yes             | degree           | roof-slope        | for each roof segment |
| | **Building mass** (volume)     | tudelft  | yes             | m^3              | building-volume   |  |
| | **Roof sun hours**             | mvrdv    | yes             | hours            | roof-sun-hours    | Full day, 21st March |
| | **Roof solar irradiance**      | mvrdv    | yes             | kWh/m2           | roof-irradiance   | Calculated for entire year |
|x| **Good / Bad solar**           | mvrdv    | yes             | boolean          | roof-good-solar   | MVRDV: Boolean to speed up calculations. Threshold unclear |
|x| ~~**Roof visibility**~~        | mvrdv    | no              |                  | roof-visibility   | supposed to measure how visible a roof is from the ground. **never implemented** |
|x| **Roof view quality**          | mvrdv    | yes             | degree           | roof-view-quality | internally generated from 3d model. measures number of unobstructed views from center of roof |



## Provided by the LAs for each building

| |                                     | **who?** | **mandatory?** | **units**   | **name**                    | **extra info** |
|-|:----------------------------------- |:--------:|:--------------:|:-----------:|:--------------------------- |:-------------- |
| | **Building energy label**           | each LA  | no             |             | building-energy-label       | |
|x| **Building foundation**             | each LA  | yes            | none        | building-foundation         | |
| | **Building function**               | each LA  | yes            | enum        | building-function           | MR-classification D1.2.3 - 4.2-usage|
|x| **Building heritage status**        | each LA  | **yes (right?)**|            | building-heritage           | =sort of the same as zone-heritage? |
| | **Building monument status**        | each LA  | yes            | boolean     | building-monument           | |
| | **Building ownership**              | each LA  | no             |             | building-ownership          | MR-classification D1.2.3 - 5|
| | **Building type**                   | each LA  | yes            | enum        | building-type               | MR-classification D1.2.3 - 4.2|
|x| **Building year of construction**   | each LA  | yes            | none        | building-year-construction  | years of construction era (MR-classification?) |
| | **Elevator presence**               | each LA  | no             | boolean     | building-has-elevator       | |
|x| **Maximum building height allowed** | each LA  | no             | meter       | building-max-height         | maybe use amount of extra levels? |
|x| **Rooftop mass**                    | each LA  | no             | kg          | roof-mass                   | what is that? |




## Provided by the LAs for neighbourhoods ("urban preferences" called in RoofScape)

|                                       | **who?** | **mandatory?** | **units** | **name**               | **extra info** | 
|:------------------------------------- |:--------:|:--------------:|:---------:|:----------------------:|:--------------:|
| **Urban district type**               | each LA  | no             | ?         |                        | MR-classification D1.2.3 - 6|
| **Zone heritage monument**            | each LA  | no             | boolean   | zone-heritage          | |             
| **Zone noise disturbance**            | each LA  | no             | dB        | zone-noise             | max dB allowed? |             


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
