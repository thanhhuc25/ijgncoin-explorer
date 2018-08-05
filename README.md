# IJGN Coin Explorer

Simple, database-free Ijgncoin blockchain explorer, via RPC. Built with Node.js, express, bootstrap-v4.

This tool is intended to be a simple, self-hosted explorer for the Ijgncoin blockchain, driven by RPC calls to your own bitcoind node. This tool is easy to run but currently lacks features compared to database-backed explorers.

# Features

* Browse blocks
* View block details
* View transaction details, with navigation "backward" via spent transaction outputs
* View JSON content used to generate most pages
* Search supports transactions, blocks, addresses (including bech32)
* Mempool summary, with fee, size, and age breakdowns
* RPC command browser and terminal
* Currently supports BTC, LTC (support for any Ijgncoin-RPC-protocol-compliant coin can be added easily)

# Getting started

The below instructions are geared toward IJC, but can be adapted easily to other coins.

## Prerequisites

1. Install and run a ful. Ensure that your node has full transaction indexing enabled (`txindex=1`) and the RPC server enabled (`server=1`).
2. Synchronize your node with the Bitcoin network.

## Instructions

1. Clone this repo
2. `npm install` to install all required dependencies
3. Edit the "rpc" settings in [credentials.js](app/credentials.js) to target your node
4. `npm start` to start the local server
5. Visit http://127.0.0.1:3002/

