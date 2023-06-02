# Sui Coin List

## Overview

This repository, maintained by the Suiet Wallet team, provides a verified list of coins for the Sui Blockchain. The data is contained in a `.json` file, enabling easy use and implementation across a variety of applications.

## Data Structure

Each coin is represented as a JSON object in the `coins.json` file, located in the `src` directory. The structure of each coin object is as follows:

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
- **source:** The origin of the coin. For wrapped coins, this is typically "bridge".
- **wrapped:** An optional object that provides more details for wrapped coins:
  - **bridger:** The service used to create the wrapped coin (e.g., "wormhole").
  - **chain:** The original blockchain of the coin before being wrapped (e.g., "eth").

## Usage

To use the `coins.json` file in your project, clone the repo or directly download the file, and import it as per your project's requirements.

Please ensure that your usage complies with the license and terms outlined in this repository.

## Contribution

We welcome contributions to this list. If you'd like to add or update a coin, please submit a pull request with the changes. Please ensure your data complies with the structure specified above.

## License

This project is licensed under the terms of the MIT LICENSE.

For any questions or issues, please open a new issue in this repository.
