# Update @t3rn_io executor release v0.38.0

https://docs.t3rn.io/executor/become-an-executor/binary-setup

```shell
screen -S Executor
```

```shell
rm -rf ~/executor
```

```shell
wget https://github.com/t3rn/executor-release/releases/download/v0.38.0/executor-linux-v0.38.0.tar.gz
```

```shell
tar -xvzf executor-linux-v0.38.0.tar.gz
```

```shell
cd ~/executor/executor/bin
```

```shell
export NODE_ENV=testnet
export LOG_LEVEL=debug
export LOG_PRETTY=false
export EXECUTOR_PROCESS_ORDERS=true
export EXECUTOR_PROCESS_CLAIMS=true
export ENABLED_NETWORKS='arbitrum-sepolia,base-sepolia,optimism-sepolia,l1rn'
export PRIVATE_KEY_LOCAL=0x... # Enter your private key
export PROMETHEUS_PORT=9090 # use only if port issue
```

```shell
./executor
```
