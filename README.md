# BTC RPC Explorer

Simple, database-free Bitcoin blockchain explorer, via RPC. Built with Node.js, express, bootstrap-v4.

This tool is intended to be a simple, self-hosted explorer for the Bitcoin blockchain, driven by RPC calls to your own bitcoind node. This tool is easy to run but currently lacks features compared to database-backed explorers.

I built this tool because I wanted to use it myself. Whatever reasons one might have for running a full node (trustlessness, technical curiosity, supporting the network, etc) it's helpful to appreciate the "fullness" of your node. With this explorer, you can not only explore the blockchain (in the traditional sense of the term "explorer"), but also explore the functional capabilities of your own node.

Live demos are available at:

* BTC: https://btc.chaintools.io
* LTC: https://ltc.chaintools.io

# Features

* Browse blocks
* View block details
* View transaction details, with navigation "backward" via spent transaction outputs
* View JSON content used to generate most pages
* Search supports transactions, blocks, addresses (including bech32)
* Mempool summary, with fee, size, and age breakdowns
* RPC command browser and terminal
* Currently supports BTC, LTC (support for any Bitcoin-RPC-protocol-compliant coin can be added easily)

# Getting started

The below instructions are geared toward BTC, but can be adapted easily to other coins.

## Prerequisites

1. Install and run a full, archiving node - [instructions](https://bitcoin.org/en/full-node). Ensure that your node has full transaction indexing enabled (`txindex=1`) and the RPC server enabled (`server=1`).
2. Synchronize your node with the Bitcoin network.

## Instructions

1. Clone this repo
2. `npm install` to install all required dependencies
3. Edit the "rpc" settings in [credentials.js](app/credentials.js) to target your node
4. Optional: Change the "coin" value in [config.js](app/config.js). Currently supported values are "BTC" and "LTC".
5. `npm start` to start the local server
6. Visit http://127.0.0.1:3002/

## Run via Docker

1. `docker build -t btc-rpc-explorer .`
2. `docker run -p 3002:3002 -it btc-rpc-explorer`

# Screenshots

<table>
  <tr>
    <td valign="top">
      <h4>Homepage (list of recent blocks)</h4>
      <img src="public/img/screenshots/home.png" style="margin-right:5px; border: 1px solid #ccc;" />
    </td>
    <td valign="top">
      <h4>Node Details</h4>
      <img src="public/img/screenshots/node-details.png" style="margin-right:5px; border: 1px solid #ccc;" />
    </td>
    <td valign="top">
      <h4>Transaction Details</h4>
      <img src="public/img/screenshots/transaction.png" style="margin-right:5px; border: 1px solid #ccc;" />
    </td>
  </tr>
  <tr>
    <td valign="top">
      <h4>Browse Blocks</h4>
      <img src="public/img/screenshots/blocks.png" style="margin-right:5px; border: 1px solid #ccc;" />
    </td>
    <td valign="top">
      <h4>Block Details</h4>
      <img src="public/img/screenshots/block.png" style="margin-right:5px; border: 1px solid #ccc;" />
    </td>
    <td valign="top">
      <h4>Mempool Summary</h4>
      <img src="public/img/screenshots/mempool-summary.png" style="margin-right:5px; border: 1px solid #ccc;" />
    </td>
  </tr>
  <tr>
    <td valign="top">
      <h4>Transaction, Raw JSON</h4>
      <img src="public/img/screenshots/transaction-raw.png" style="margin-right:5px; border: 1px solid #ccc;" />
    </td>
    <td valign="top">
      <h4>RPC Browser</h4>
      <img src="public/img/screenshots/rpc-browser.png" style="margin-right:5px; border: 1px solid #ccc;" />
    </td>
    <td valign="top">
      <h4>Connect via RPC</h4>
      <img src="public/img/screenshots/connect.png" style="margin-right:5px; border: 1px solid #ccc;" />
    </td>
  </tr>
</table>

# Donate

To support continued development of this tool and/or to support the hosting of the live demo site:

* [Bitcoin](bitcoin:3NPGpNyLLmVKCEcuipBs7G4KpQJoJXjDGe): 3NPGpNyLLmVKCEcuipBs7G4KpQJoJXjDGe
* [Litecoin](litecoin:ME4pXiXuWfEi1ANBDo9irUJVcZBhsTx14i): ME4pXiXuWfEi1ANBDo9irUJVcZBhsTx14i

