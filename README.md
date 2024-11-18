# Pre-compiled CCMiner for Termux:
This is a WIP repo for pre-compiled ccminer binaries with latest termux(v0.118.0) and latest clang(v17.0.6).

# **`Disclaimer: I accept no warranties or liabilities on this repo. Do it at your own risk!!!`**

# **`This is for ARM Cortex-A78 & Cortex-A55`**

# Installation:
1. Download & install latest arm64-v8a [Termux](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_arm64-v8a.apk):
```
https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_arm64-v8a.apk
```
2. Get Termux ready:
- Type `y` then enter key in any prompts!
```
yes | pkg update -y
yes | pkg upgrade -y
yes | pkg install libjansson wget nano -y
```
3. Download ccminer, config, start:
```
mkdir ccminer && cd ccminer
wget https://raw.githubusercontent.com/Darktron/pre-compiled/a78-a55/ccminer
wget https://raw.githubusercontent.com/Darktron/pre-compiled/a78-a55/config.json
wget https://raw.githubusercontent.com/Darktron/pre-compiled/a78-a55/start.sh
chmod +x ccminer start.sh
```
# Usage:

1. Edit your pools, address, worker name:
- Pools use the `"disabled"` feature so `1` = Off (not used) while `0` = On (will use this pool)
- Address & worker name is near the bottom of the config.json in format `address here.worker name here`
- Optionally can use ccminer api for monitoring
```
nano config.json
```
2. Start ccminer with:
```
~/ccminer/start.sh
```
3. Close ccminer with:
```
CTRL + c
```
# Tips & Tricks:
- If Termux can't complete update & upgrade please clear app cache and data.
- Disable battery manager, battery optimization for Termux app.
- If you long press anywhere within Termux then click `More` there is an option to `Keep screen on`.
- Use a pool with low latency to your location/internet.
- Give the miner/stratum time to stabilize hashrate(~30m-1h).

