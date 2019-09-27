
# summary of shape and chunk size for 20G SST datasize with chunk size 128M

| chunking scheme | chunk_size=128MB | global_mean | temporal_mean | climatology | anomaly |
|spatial| |shape=(20834, 384, 320), chunksize=(20834, 28, 28) | shape=(384, 320), chunksize=(28, 28) | shape=(20834,), chunksize=(20834,)| shape=(4, 384, 320), chunksize=(1, 28, 28) | shape=(20834, 384, 320), chunksize=(60, 28, 28)>

temporal | shape=(20834, 384, 320), chunksize=(131, 384, 320)| shape=(384, 320), chunksize=(384, 320)| shape=(20834,), chunksize=(131,)| shape=(4, 384, 320), chunksize=(1, 384, 320)| shape=(20834, 384, 320), chunksize=(60, 384, 320)|

auto | shape=(20834, 384, 320), chunksize=(251, 192, 160)| shape=(384, 320), chunksize=(192, 160)| shape=(20834,), chunksize=(251,)| shape=(4, 384, 320), chunksize=(1, 192, 160)| shape=(20834, 384, 320), chunksize=(60, 192, 160)|


