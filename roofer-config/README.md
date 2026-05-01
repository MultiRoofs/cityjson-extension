
1. update line 3: `polygon-source = "wippolder.gpkg"` and put your own footprint datasets (the full path) 
2. update line 4: `output-directory = "output/"` to define the folder where the output file `*.city.jsonl` will be written 
3. update line 69: `source = ["wippolder.las"]` and put the path of your LAS/LAZ file (more than one possible this way: `source = ["wippolder.las", "mysecond.laz", "mythird.laz"])`
4. run Roofer this way: `roofer -c config_mr.toml`
5. voilà, it should work (touch wood)
