# quantus-miner

Website: https://quantus.pearlfortune.org

Discord: https://discord.gg/bhWxDxn8cY

Github: [https://github.com/pearlfortune/pearl-miner](https://github.com/pearlfortune/quantus-miner)

## 

:rocket: Quantus Mainnet

Quantus 主网将于 9 月 9 日正式上线！

届时我们将同步推出：
:pick: Quantus Mining Pool
:zap: 高性能优化 Miner

矿池及 Miner 详细信息将在主网上线后公布，敬请期待！:rocket:

矿池：https://quantus.pearlfortune.org/

⸻

:rocket: Quantus Mainnet 

Quantus Mainnet launches on September 9!

We will launch:
:pick: Quantus Mining Pool
:zap: Performance-Optimized Miner

Pool and miner details will be announced after the mainnet launch.

Stay tuned! :rocket:

Pool: https://quantus.pearlfortune.org/

## Get Started

#### Linux (NVIDIA)
```sh
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

````

#### Docker
```sh
## Start
docker run -d \
    --name quantus-miner \
    --restart always \
    --gpus all \
    pearlfortune/quantus-miner:vtest \
    stratum \
    --stratum-addr 43.133.30.208:34567 \
    --worker-id QUANTUS_ADDRESS.hostname

## Logs
docker logs -f quantus-miner
```
