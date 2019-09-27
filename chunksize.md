
# summary of shape and chunk size for 20G SST datasize with chunk size 128M

| chunking scheme | chunk_size=128MB | global_mean | temporal_mean | climatology | anomaly |
|---|---|---|---|---|---|
|shape |(20834, 384, 320)|(384, 320)| (20834,)|(4, 384, 320)|(20834, 384, 320)|
|spatial | (20834, 28, 28) | (28, 28) | (20834,)|  (1, 28, 28) | (60, 28, 28)|
|temporal | (131, 384, 320) |  (384, 320)|  (131,)| (1, 384, 320)| (60, 384, 320)|
|auto |  (251, 192, 160)     | (192, 160)|  (251,)| (1, 192, 160)|  (60, 192, 160)|


spatial have total  16333856 elements.  temporal have total 16097280 elements, automatic have total 7710720 elements.

