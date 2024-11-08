# P-SOPS

## Introduction
Examples of how to use sops for encryption

## Getting Started

### Prerequisites
- [Devbox](https://github.com/jetpack-io/devbox)
- [sops](https://github.com/getsops/sops)
- [age](https://github.com/FiloSottile/age)

## Examples
### Using age
Generate age key pair
```
age-keygen -o keys.txt
```
Add public keys to ```.sops.yaml``` file

Encrypt file
```
sops secrets/test.yaml
```
Set path of keys.txt file
```export SOPS_AGE_KEY_FILE="./keys.txt"```
Decrypt file 
```
sops -d secrets/test.yaml
```

