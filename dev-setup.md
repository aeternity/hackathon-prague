# Developer Tools Setup and Overview

- [sdk-testnet](#sdk-testnet): hosted aeternity testnet nodes
- [faucet](#faucet): faucet to receive testnet tokens
- [aeproject](#aeproject): local contract development setup and 

### sdk-testnet
 - Api-Documentation: https://api-docs.aeternity.io/
 - URL: https://sdk-testnet.aepps.com/
 - Combines both internal and external endpoints of the node in one interface

### faucet
open https://testnet.faucet.aepps.com/ to receive testnet tokens

### aeproject
 - Requirements: docker, docker-compose, nodejs
 - Install: `npm i -g aeproject`
 - Documentation: https://aeproject.gitbook.io/aeproject/
 - Basic usage:
    - create a new directory
    - `aeproject init` initializes project
    - `aeproject node` runs local testing nodes (`aeproject node --stop` to stop)
    - sample contract in `contracts/`
    - sample chain assert js tests for the contract in `test/`
    - `aeproject test` to run tests
    - `aeproject deploy -n testnet -s YOUR_FUNDED_TESTNET_SECRET_KEY` to deploy to testnet (as specified in `deployment/deploy.js`)
    
