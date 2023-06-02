# Sui Coin List

## Overview

This repository, maintained by the Suiet Wallet team, provides a verified list of coins for the Sui Blockchain. The data is contained in a `.json` file, enabling easy use and implementation across a variety of applications.

## Data Structure

Each coin is represented as a JSON object in the [`coins.json`](/src/coins.json) file, located in the `src` directory. The structure of each coin object is as follows:

```json
{
  "name": "Wrapped ETH",
  "symbol": "WETH",
  "coin_type": "0xaf8cd5edc19c4512f4259f0bee101a40d41ebed738ade5874359610ef8eeced5::coin::COIN",
  "decimals": 8,
  "icon_url": "",
  "project_url": "https://wormhole.com/",
  "source": "bridge",
  "wrapped": {
    "bridger": "wormhole",
    "chain": "eth"
  }
}
```

The fields of the JSON object are described as follows:

- **name:** The full name of the coin (e.g., "Wrapped ETH").
- **symbol:** The symbol by which the coin is commonly known (e.g., "WETH").
- **coin_type:** The unique identifier of the coin on the Sui Blockchain.
- **decimals:** The number of decimal places used by the coin.
- **icon_url:** The URL for the coin's icon. If there's no specific icon, this field is an empty string.
- **project_url:** The URL for the official project or organization related to the coin.
- **source:** The source of the coin, which can take one of two values:
  - "native": The coin is a native token issued on the Sui Blockchain.
  - "bridge": The coin is a wrapped token bridged from another blockchain.
- **wrapped:** An optional object that provides more details for wrapped coins:
  - **bridger:** The service used to create the wrapped coin (e.g., "wormhole").
  - **chain:** The original blockchain of the coin before being wrapped (e.g., "eth").

## Usage

To use the `coins.json` file in your project, clone the repo or directly download the file, and import it as per your project's requirements.

Please ensure that your usage complies with the license and terms outlined in this repository.

## Contribution

We warmly welcome contributions to this list. If you'd like to add or update a coin, please submit a pull request with the changes and ensure that your data adheres to the structure specified above.

When suggesting a coin for addition, it should meet one or more of the following criteria[^1]:

1. The coin has been listed on multiple renowned exchanges.
2. The coin is an asset bridged from a well-known cross-chain bridge.

[^1]: Please note that these standards may change over time as the environment evolves.

Before submitting a pull request, please ensure that you have done thorough research and that all the provided information is accurate to the best of your knowledge. Inaccurate or misleading submissions could impact the integrity of the list. We appreciate your support in maintaining the highest standard for the Sui Blockchain Verified Coin List.

## License

This project is licensed under the terms of the MIT LICENSE.

For any questions or issues, please open a new issue in this repository.
