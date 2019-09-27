
# summary of shape and chunk size for SST (time,lon,lat ) dataset :20G of with chunk size 128M (output of debug16.ipynb)

| chunking scheme | chunk_size=128MB | global_mean | temporal_mean | climatology | anomaly |
|---|---|---|---|---|---|
|shape |(20834, 384, 320)|(384, 320)| (20834,)|(4, 384, 320)|(20834, 384, 320)|
|spatial | (20834, 28, 28) | (28, 28) | (20834,)|  (1, 28, 28) | (60, 28, 28)|
|temporal | (131, 384, 320) |  (384, 320)|  (131,)| (1, 384, 320)| (60, 384, 320)|
|auto |  (251, 192, 160)     | (192, 160)|  (251,)| (1, 192, 160)|  (60, 192, 160)|

Our benchmark use float8 for data precision.  128MB can have (128 ¥times 10**6 ) / 8 = 16 000 000 elements of float8. 

spatial have total  16333856 elements.  temporal have total 16097280 elements, automatic have total 7710720 elements.  
spatial and temporal have correct number of element but not automatic chunking scheme. 
i.e. automatic only have chunk size of 62MB??


# summary of shape and chunk size for SST (time,lon,lat ) dataset :20G of with chunk size 256M (output of debug8.ipynb)

| chunking scheme | chunk_size=128MB | global_mean | temporal_mean | climatology | anomaly |
|---|---|---|---|---|---|
|shape |(20834, 384, 320)|(384, 320)| (20834,)|(4, 384, 320)|(20834, 384, 320)|
|spatial |(20834, 40, 40)> |(40, 40)> |(20834,)> |(1, 40, 40)> |(60, 40, 40)>
|temporal |(261, 384, 320)> |(384, 320)> |(261,)> |(1, 384, 320)> |(60, 384, 320)>
|auto |(317, 192, 160)> |(192, 160)> |(317,)> |(1, 192, 160)> |(60, 192, 160)>

256 MB corresponds to 32000000 elements.
spatial have total  33334400 elements.  temporal have total 32071680 elements, automatic have total 9738240 elements.  

spatial and temporal have correct number of element but not automatic chunking scheme. 
i.e. Automatic only corresponds to chunk size 78MB?


# summary of shape and chunk size for SST (time,lon,lat ) dataset :20G of with chunk size 512M  (output of debug4.ipynb

| chunking scheme | chunk_size=128MB | global_mean | temporal_mean | climatology | anomaly |
|---|---|---|---|---|---|
|shape |(20834, 384, 320)|(384, 320)| (20834,)|(4, 384, 320)|(20834, 384, 320)|
|spatial |(20834, 56, 56)| (56, 56)| (20834,)| (1, 56, 56)| (60, 56, 56)|
|temporal |(521, 384, 320)| (384, 320)| (521,)| (1, 384, 320)| (60, 384, 320)|
|auto| (520, 384, 320)| (384, 320)| (520,)| (1, 384, 320)| (60, 384, 320)|


512 MB corresponds to 64000000 elements.

spatial have total  65335424 elements.  temporal have total 64020480 elements, automatic have total 63897600 elements.  

All 3 chunking schme have correct number of elements. 

# todo, rerun debug8.ipynb and debug16.ipynb and see if I get same result to be sure 
