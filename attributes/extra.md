
# Extra attributes 


## Per Building

| |                                     | **who?** | **units**   | **name**                    | **extra info** |
|-|:----------------------------------- |:--------:|:-----------:|:--------------------------- |:-------------- |
| | **Building function**               | each LA  | enum        | building-function           | MR-D1.2.3-4.2: "commercial", "industrial", "office", "public", "residential" | | | **Building energy label**           | each LA  | none        | building-energy-label       | A, B, C, etc.  |
| | **Building ownership**              | each LA  |             | building-ownership          | MR-D1.2.3-5: "corporate real estate owner", "homeowner association",  "housing corporation",  "industrial property owner", "institutional investor", "landlord",  "municipal real estate owner",  "private individual homeowner",  "private project developers", "religious institution"| 
| | **Building type**                   | each LA  | enum        | building-type               | MR-D1.2.3-4.2: "detached", "semi-detached", "terraced", "apartment" |
| | **Building monument status**        | each LA  | boolean     | building-monument           | |
|x| **Building foundation**             | each LA  | none        | building-foundation         | ground, load-bearing capacity: classification?  |
| | **Building year of construction**   | each LA  | none        | building-year-construction  | |
| | **Elevator presence**               | each LA  | boolean     | building-has-elevator       | |
| | **Maximum building height allowed** | each LA  | meter       | building-max-height         | |




## Per neighbourhoods

|                                       | **who?** | **mandatory?** | **units** | **name**               | **extra info** | 
|:------------------------------------- |:--------:|:--------------:|:---------:|:----------------------:|:--------------:|
| **Urban district type**               | each LA  | no             | ?         |                        | MR-classification D1.2.3 - 6|
| **Zone heritage monument**            | each LA  | no             | boolean   | zone-heritage          | |             
| **Zone noise disturbance**            | each LA  | no             | dB        | zone-noise             | max dB allowed? |




## Stuff that should be cleaned:

|||||||
|:------------------------------------- |:--------:|:--------------:|:---------:|:----------------------:|:--------------:|
| **Zone green corridor**                   | P_Z_green        | m         | number  | Gemeente Rotterdam  <br>Ingenieursbureau      | Municipal  |
| **Zone noise disturbance**                |                  | dB        | number  | Atlas Leefomgeving                            |            |
| **Zone flood risk**                       | P_Z_flood        | -         | text    | Gemeente Rotterdam  <br>Rotterdams Weerwoord  | Municipal  |
| **Zone stedelijke hitte-eiland effect**   | P_Z_heat         | degree C  | number  | RIVM Atlas Natuurlijk Kapitaal                | National   |
| **Zone access to public transportation**  | P_Z_transport    | -         | Text    | Internally generated                          | Municipal  |
| **Zone access to public space**           | P_Z_pspace       | -         | number  | Gemeente Rotterdam  <br>Voetgangerskaart      | Municipal  |
| **Expected renovation year**              |                  |           |         | Client data                                   |            |
