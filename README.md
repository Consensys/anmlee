# ANMLEE: A Nifty ML EE (pronounced a·nom·a·ly)

This repo demonstrates how a trained ML model could run inside an Ethereum 2 EE.

## Prerequisits

Install LLVM

```bash
brew install llvm
echo 'export PATH="/usr/local/opt/llvm/bin:$PATH"' >> ~/.bash_profile
```

Install the WebAssembly Binary Toolkit

```bash
brew install wabt
```

Install NinJa

```bash
brew install ninja
```

Install Wasmer: The Universal WebAssembly Runtime

```bash
curl https://get.wasmer.io -sSfL | sh
```

## Build 

Native:

```bash
make build-native
```

Wasm
```bash
make build-wasm
```

## Run

Native
```bash
./build/random-forest
```

Wasm
```bash
wasmer run build/random-forest.wasm 
```