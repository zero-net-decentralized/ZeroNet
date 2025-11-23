# ZeroNet Open source — built by enthusiasts.

## Why?

* We believe in open, free, and uncensored network and communication.
* No single point of failure: Site remains online so long as at least 1 peer is
  serving it.
* No hosting costs: Sites are served by visitors.
* Impossible to shut down: It's nowhere because it's everywhere.
* Fast and works offline: You can access the site even if Internet is
  unavailable.


## Features
 * Real-time updated sites
 * Namecoin .bit domains support
 * Easy to setup: unpack & run
 * Clone websites in one click
 * Password-less [BIP32](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)
   based authorization: Your account is protected by the same cryptography as your Bitcoin wallet
 * Built-in SQL server with P2P data synchronization: Allows easier site development and faster page load times
 * Anonymity: Full Tor network support with .onion hidden services instead of IPv4 addresses
 * TLS encrypted connections
 * Automatic uPnP port opening
 * Plugin for multiuser (openproxy) support
 * Works with any browser/OS


## How does it work?

* After starting `zeronet` you will be able to visit zeronet sites using
  `http://127.0.0.1:43110/{zeronet_address}` (eg.
  `http://127.0.0.1:43110/1HeLLo4uzjaLetFx6NH3PMwFP3qbRbTf3D`).
* When you visit a new zeronet site, it tries to find peers using the BitTorrent
  network so it can download the site files (html, css, js...) from them.
* Each visited site is also served by you.
* Every site contains a `content.json` file which holds all other files in a sha512 hash
  and a signature generated using the site's private key.
* If the site owner (who has the private key for the site address) modifies the
  site, then he/she signs the new `content.json` and publishes it to the peers.
  Afterwards, the peers verify the `content.json` integrity (using the
  signature), they download the modified files and publish the new content to
  other peers.

## Screenshots

![Screenshot](https://i.imgur.com/H60OAHY.png)

## How to join

### Windows

 - Download [ZeroNet-win64.zip](../../releases)
 - Unpack anywhere
 - Run `ZeroNet.exe`

## Current limitations

* ~~No torrent-like file splitting for big file support~~ (big file support added)
* ~~No more anonymous than Bittorrent~~ (built-in full Tor support added)
* File transactions are not compressed ~~or encrypted yet~~ (TLS encryption added)
* No private sites


## How can I create a ZeroNet site?

 * Click on **⋮** > **"Create new, empty site"** menu item on the site ZeroHello.
 * You will be **redirected** to a completely new site that is only modifiable by you!
 * You can find and modify your site's content in **data/[yoursiteaddress]** directory
 * After the modifications open your site, drag the topright "0" button to left, then press **sign** and **publish** buttons on the bottom


