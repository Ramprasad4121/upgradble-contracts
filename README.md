# Upgradable Contracts

<!-- <div align="center">
  <a href="https://github.com/Ramprasad4121/upgradble-contracts">
    <img src="docs/images/upgradable-banner.png" alt="Upgradable Contracts Banner" width="600" height="300">
  </a>
</div> -->

<div align="center">
  Upgradable Smart Contracts with Proxy Patterns
  <br />
  <a href="#about"><strong>Explore the demo »</strong></a>
  <br />
  <br />
  <a href="https://github.com/Ramprasad4121/upgradble-contracts/issues/new?assignees=&labels=bug&template=01_BUG_REPORT.md&title=bug%3A+">Report a Bug</a>
  ·
  <a href="https://github.com/Ramprasad4121/upgradble-contracts/issues/new?assignees=&labels=enhancement&template=02_FEATURE_REQUEST.md&title=feat%3A+">Request a Feature</a>
  ·
  <a href="https://github.com/Ramprasad4121/upgradble-contracts/issues/new?assignees=&labels=question&template=04_SUPPORT_QUESTION.md&title=support%3A+">Ask a Question</a>
</div>

<div align="center">
<br />

[![Solidity](https://img.shields.io/badge/Solidity-^0.8.20-blue)](https://soliditylang.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green)](LICENSE)

</div>

<details open="open">
<summary>Table of Contents</summary>

- [Upgradable Contracts](#upgradable-contracts)
  - [About](#about)
    - [Built With](#built-with)
  - [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
  - [Usage](#usage)
    - [Local Development](#local-development)
    - [Testnet (Sepolia)](#testnet-sepolia)
    - [Testing](#testing)
    - [Other Commands](#other-commands)
  - [Roadmap](#roadmap)
  - [Support](#support)
  - [Project Assistance](#project-assistance)
  - [Contributing](#contributing)
  - [Authors \& Contributors](#authors--contributors)
  - [Security](#security)
  - [License](#license)
  - [Acknowledgements](#acknowledgements)

</details>

---

## About

A Foundry-based template for upgradable smart contracts using proxy patterns (e.g., UUPS/Transparent). Enables seamless upgrades without redeploying, with full testing, gas optimization, and deployment to local Anvil or Sepolia testnet.

Why this? To facilitate secure, evolvable contract development with OpenZeppelin upgrades plugin.

<!-- <details>
<summary>Screenshots</summary>
<br>

|                               Local Deployment Console                               |                               Gas Snapshot Report                               |
| :-------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| <img src="docs/images/deploy-local.png" title="Anvil Deployment" width="100%"> | <img src="docs/images/gas-snapshot.png" title="Gas Report" width="100%"> |

> Add screenshots of `make deploy` and `forge snapshot` outputs.

</details> -->

### Built With

- [Foundry](https://book.getfoundry.sh/) – Forge, Cast, Anvil
- [OpenZeppelin Upgrades](https://docs.openzeppelin.com/upgrades-plugins/) – Proxy management
- Solidity ^0.8.20
- [Make](https://www.gnu.org/software/make/) – Automation

## Getting Started

### Prerequisites

- Git (`git --version`)
- Foundry (`curl -L https://foundry.paradigm.xyz | bash && foundryup`; `forge --version`)

### Installation

1. Clone:
   ```bash
   git clone https://github.com/Ramprasad4121/upgradble-contracts.git
   cd upgradble-contracts
   ```

2. Build:
   ```bash
   forge build
   ```

3. Setup `.env` from `.env.example`: Add `SEPOLIA_RPC_URL` (e.g., Alchemy), `PRIVATE_KEY` (test only), `ETHERSCAN_API_KEY` (optional).

## Usage

### Local Development

- Start Anvil:
  ```bash
  make anvil
  ```

- Deploy (v1):
  ```bash
  make deploy
  ```

- Upgrade (v2):
  ```bash
  make upgrade
  ```

### Testnet (Sepolia)

1. Fund: [Sepolia Faucet](https://sepoliafaucet.com/).
2. Deploy:
   ```bash
   make deploy ARGS="--network sepolia"
   ```

### Testing

- Unit:
  ```bash
  forge test
  ```

- Coverage:
  ```bash
  forge coverage --report lcov
  ```

- Detailed:
  ```bash
  forge coverage --report debug
  ```

### Other Commands

- Gas snapshot: `forge snapshot` (outputs `.gas-snapshot`)
- Format: `forge fmt`
- Clean: `make clean`

## Roadmap

[Open issues](https://github.com/Ramprasad4121/upgradble-contracts/issues).

- Enhancements: Multi-proxy support, CI/CD
- Bugs: Vote with 👍

Future: Mainnet integration, frontend tools.

## Support

- [Issues](https://github.com/Ramprasad4121/upgradble-contracts/issues/new?assignees=&labels=question&template=04_SUPPORT_QUESTION.md&title=support%3A+)
- [X](https://x.com/0xramprasad)

## Project Assistance

- ⭐ [Star](https://github.com/Ramprasad4121/upgradble-contracts)
- Tweet: "#UpgradableContracts #Solidity"
- Blog: [Dev.to](https://dev.to/)

## Contributing

Fork, branch (`git checkout -b feature/xyz`), commit, PR. See [CONTRIBUTING.md](docs/CONTRIBUTING.md).

## Authors & Contributors

- [Ramprasad4121](https://github.com/Ramprasad4121)

[Contributors](https://github.com/Ramprasad4121/upgradble-contracts/contributors)

## Security

Proxy-secured; audit upgrades. Report: [SECURITY.md](docs/SECURITY.md). "As is."

## License

MIT License. See [LICENSE](LICENSE).

## Acknowledgements

- [OpenZeppelin](https://openzeppelin.com/) – Upgrades plugin
- [Foundry](https://getfoundry.sh/) – Toolkit
- Ethereum community.