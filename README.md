# quantus-miner

Website: https://quantus.pearlfortune.org

Discord: https://discord.gg/bhWxDxn8cY

Github: https://github.com/pearlfortune/quantus-miner


## Get Started

#### Servers
```ini
quan.pearlfortune.org:33333
43.133.30.208:34567
```

#### Linux (NVIDIA)
```sh
## Downlaod
wget -c https://github.com/pearlfortune/quantus-miner/releases/download/v1.3.0/qpow-v1.3.0.tar.gz
tar vxzf qpow-v1.3.0.tar.gz
cd qpow

## Start - CUDA 12
./miner-cuda12 \
stratum \
--stratum-addr 43.133.30.208:34567 \
--worker-id QUANTUS_ADDRESS.hostname

## Start - CUDA 13
./miner-cuda13 \
stratum \
--stratum-addr 43.133.30.208:34567 \
--worker-id QUANTUS_ADDRESS.hostname
```

#### HiveOS (NVIDIA)
```sh
{
    "name": "quan",
    "isFavorite": false,
    "items": [
        {
            "coin": "QUAN",
            "pool_ssl": false,
            "dpool_ssl": false,
            "miner": "custom",
            "miner_alt": "qpow",
            "miner_config": {
                "url": "43.133.30.208:34567",
                "miner": "qpow",
                "template": "%WAL%.%WORKER_NAME%",
                "install_url": "https://github.com/pearlfortune/quantus-miner/releases/download/v1.3.0/qpow-v1.3.0.tar.gz"
            }
        }
    ]
}
````

#### Docker
```sh
## Start
docker run -d \
    --name quantus-miner \
    --restart always \
    --gpus all \
    pearlfortune/quantus-miner:v1.3.0 \
    stratum \
    --stratum-addr 43.133.30.208:34567 \
    --worker-id QUANTUS_ADDRESS.hostname

## Logs
docker logs -f quantus-miner
```
