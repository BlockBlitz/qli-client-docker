# QLI-Client Docker

This Dockerfile and run script are all you need to run QLI-Client for CPU only mining. For alternative containers, see the [Qli-Cuda](https://github.com/BlockBlitz/qli-cuda-docker) image for Nvidia GPU mining or [Qli-Zluda](https://github.com/BlockBlitz/qli-zluda-docker) image for AMD GPU mining. 

***This project is not affiliated with [Qubic](http://discord.gg/qubic) or [Qubic.li](https://qubic.li/). Please report any bugs related to the docker container here and miner specific bugs to the respective miner owners.***

## Usage

The following environment variables are required:
| Name           | Description                                                      | Options                                                                  | Default |
|----------------|------------------------------------------------------------------|--------------------------------------------------------------------------|---------|
| ACCESS_TOKEN    | Your Qubic.li pool access token                                 |                                                                          |         |
| WORKER_NAME     | Your worker name/label visible in the pool                      |                                                                          |         | 
| THREAD_COUNT    | Number of CPU threads to use. Set to 0 to disable CPU Mining.   |                                                                          |         | 

This image does not currently suppot the Payment ID parameter for the pool.

The following command starts the container with the specified parameters

`docker run -e WORKER_NAME=my-worker -e ACCESS_TOKEN=my-access-token -e THREAD_COUNT=12 ghcr.io/BlockBlitz/qli-client:latest`

Or more favorably, via the included docker-compose file.

`docker compose up -d`

Qubic: GKLVMTZITKRXGEAKRCIFSNOHQWPDZNXJOAAEXMRIEFYQENRQZOTZBGMCWRAE
