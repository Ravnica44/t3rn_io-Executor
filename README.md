Update @t3rn_io executor release v0.32.0

https://docs.t3rn.io/executor/become-an-executor/binary-setup

screen -S Executor # or the one you have setup

Ctrl + C

rm -rf ~/executor

wget https://github.com/t3rn/executor-release/releases/download/v0.32.0/executor-linux-v0.32.0.tar.gz

tar -xvzf executor-linux-v0.32.0.tar.gz

cd ~/executor/executor/bin

export NODE_ENV=testnet
export LOG_LEVEL=debug
export LOG_PRETTY=false
export EXECUTOR_PROCESS_ORDERS=true
export EXECUTOR_PROCESS_CLAIMS=true
export ENABLED_NETWORKS='arbitrum-sepolia,base-sepolia,optimism-sepolia,l1rn'
export PRIVATE_KEY_LOCAL=0x... # Enter your private key
# export PROMETHEUS_PORT=9090 # use only if port issue

./executor
