# Developer Tools Setup and Overview

- [aeternity node](#aeternity-node): aeternity blockchain full node
- [sdk](#sdk): sdk to integrate aeternity
- [base-aepp](#base-aepp): aeternity developed pwa/native wallet app and aepps browser
- [aeproject](#aeproject): local contract development setup and 
- [aecli](#aecli): commandline tools to interact with aeternity
- [aeternity protocol](#aeternity-protocol): protocol definition of aeternity
- [sdk-testnet](#sdk-testnet): hosted aeternity testnet nodes
- [contracts editors](#contracts-editors): two different contract editors
- [sophia ide plugins](#sophia-ide-plugins): integrations for sophia language in vscode and jetbrains editors
- [middleware](#middleware): middleware to aggregate and index data from aeternity node
- [blockchain explorer](#blockchain-explorer): blockchain explorer for mainnet and testnet
- [faucet](#faucet): faucet to receive testnet tokens
- [compiler](#compiler): standalone sophia compiler
- [documentation-hub](#documentation-hub): hub for all gathered documentations (eventually outdated)
- [tutorials and sophia examples](#tutorials-and-sophia-examples): aeternity tutorials and sophia examples (eventually outdated)

## aeternity node
 - full node written in erlang
 - provides http api documented in https://api-docs.aeternity.io/ and available in [sdk-testnet](#sdk-testnet)
 - https://github.com/aeternity/aeternity
 - full sync takes 1-2 days
 - Usage-Documentation: https://github.com/aeternity/aeternity/tree/master/docs

## sdk
 - JS-SDK: https://github.com/aeternity/aepp-sdk-js
    - fully featured sdk for all aeternity functonallity
    - integration in base-aepp via `await Aepp()` interface
    - `npm i @aeternity/aepp-sdk` to install
    - sample setup for testnet
    ```
      await Universal({
        url: 'https://sdk-testnet.aepps.com/',
        internalUrl: 'https://sdk-testnet.aepps.com/',
        keypair: YOUR_KEYPAIR,
        networkId: 'ae_uat',
        compilerUrl: 'https://compiler.aepps.com'
      });
      ```
 - Python-SDK: https://github.com/aeternity/aepp-sdk-python
 - GO-SDK: https://github.com/aeternity/aepp-sdk-go
 - Elixir-SDK: https://github.com/aeternity/aepp-sdk-elixir
 - Java-SDK: https://github.com/kryptokrauts/aepp-sdk-java
    - community developed and maintained

## base-aepp
 - aeternity wallet aepp and aepps browser
 - provides wallet and signing access to aepps opened inside
 - available at https://base.aepps.com/ or https://github.com/aeternity/aepp-base
 - to run locally for development, clone, `npm i`, `npm run serve`, open in browser in responsive mode as iPhone

## aeproject
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

## aecli
 - commandline tools to interact with aeternity blockchain, e.g. create account and make transactions
 - Usage-Documentation: https://github.com/aeternity/aepp-cli-js
 - Install: `npm install -g @aeternity/aepp-cli`
 - Create Account: `aecli account create ACCOUNT_NAME`

## aeternity protocol
 - full aeternity protocol specification
 - https://github.com/aeternity/protocol
 - sophia language reference: https://github.com/aeternity/protocol/blob/master/contracts/sophia.md

## sdk-testnet
 - Api-Documentation: https://api-docs.aeternity.io/
 - URL: https://sdk-testnet.aepps.com/
 - Combines both internal and external endpoints of the node in one interface

## contracts editors
 - fire editor http://fireeditor.nikitafuchs.de/
 - old contracts editor https://testnet.contracts.aepps.com/

## sophia-ide-plugins
 - vscode: https://marketplace.visualstudio.com/items?itemName=MilenRadkov.sophia
 - jetbrains: https://plugins.jetbrains.com/plugin/12197-sophia-ternity

## middleware
 - middleware to aggregate and index data of aeternity node
 - provides websocket listeners to whats happening in the network
 - https://github.com/aeternity/aepp-middleware
 - Documentation: https://github.com/aeternity/aepp-middleware/blob/develop/docs/middleware-guide.md
 - Explorer frontend at: https://mdw.aepps.com/ and https://testnet.mdw.aepps.com/

## blockchain explorer
 - by middleware: https://mdw.aepps.com/ and https://testnet.mdw.aepps.com/
 - default explorer: https://explorer.aepps.com/ and https://testnet.explorer.aepps.com/
 - aeknow community explorer: http://aeknow.org/
 
## faucet
open https://testnet.faucet.aepps.com/ to receive testnet tokens

## compiler
 - compiler for sophia smart contracts
 - hosted at: https://compiler.aepps.com/
 - https://github.com/aeternity/aesophia and http wrapper at https://github.com/aeternity/aesophia_http

## documentation-hub
 - eventually outdated, use with care and prefer available documentation of single projects
 - http://aeternity.com/documentation-hub/

## tutorials and sophia examples
 - eventually outdated, use with care
 - https://github.com/aeternity/aepp-sophia-examples
 - https://github.com/aeternity/tutorials
