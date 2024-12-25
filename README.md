[![Join our Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/hidden_coding)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/aero25x)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=x&logoColor=white)](https://x.com/aero25x)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@flaming_chameleon)

# GasZip to Eclipse by Aero25x


GasZip to Eclipse is a Python-based tool designed to facilitate the transfer of Ethereum (ETH) with custom input data derived from Solana addresses. This tool leverages the Web3.py library to interact with the Ethereum blockchain, allowing users to send ETH transactions seamlessly while embedding Solana address information.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
  - [Windows](#windows)
  - [macOS](#macos)
  - [Linux](#linux)
- [Configuration](#configuration)
- [Usage](#usage)
- [Example Output](#example-output)
- [Requirements](#requirements)
- [Troubleshooting](#troubleshooting)
- [License](#license)
- [Contact](#contact)

## Features

- **Secure Transactions**: Send ETH securely using your private key.
- **Custom Data Encoding**: Embed Solana address information into Ethereum transactions.
- **Flexible Configuration**: Customize gas limits, fees, and recipient addresses.
- **Cross-Platform Support**: Compatible with Windows, macOS, and Linux.
- **Environment Variable Support**: Safeguard sensitive information by using environment variables.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- **Python 3.7+**: Make sure Python is installed on your system. You can download it from [python.org](https://www.python.org/downloads/).
- **Ethereum Node Access**: An Infura project ID or another Ethereum node provider URL.
- **Private Key**: The private key of the Ethereum account you wish to send ETH from.
- **Solana Address**: A valid Solana address in Base58 format.

## Installation

Follow the steps below to install and set up GasZip to Eclipse on your operating system.

### Windows

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Aero25x/gaszip-send-native-to-eclipse-Network.git
   cd gaszip-send-native-to-eclipse-Network
   ```

2. **Create a Virtual Environment**
   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

### macOS

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Aero25x/gaszip-send-native-to-eclipse-Network.git
   cd gaszip-send-native-to-eclipse-Network
   ```

2. **Create a Virtual Environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

### Linux

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Aero25x/gaszip-send-native-to-eclipse-Network.git
   cd gaszip-send-native-to-eclipse-Network
   ```

2. **Create a Virtual Environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## Configuration

1. **Set Environment Variables**

   It's crucial to keep your private key secure. Use environment variables to store sensitive information.

   - **Windows**
     ```bash
     set PRIVATE_KEY=your_private_key_here
     set SOLANA_ADDRESS=your_solana_address_here
     set INFURA_PROJECT_ID=your_infura_project_id_here
     ```

   - **macOS/Linux**
     ```bash
     export PRIVATE_KEY=your_private_key_here
     export SOLANA_ADDRESS=your_solana_address_here
     export INFURA_PROJECT_ID=your_infura_project_id_here
     ```

2. **Update Provider URL**

   In the `send_native_from_base_to_elcipse` function within `main.py`, ensure you replace `YOUR_INFURA_PROJECT_ID` with your actual Infura project ID or another Ethereum node provider URL.

   ```python
   provider_url=f"https://mainnet.infura.io/v3/{os.getenv('INFURA_PROJECT_ID')}"
   ```

## Usage

Run the script using Python:

```bash
python main.py
```

The script will execute the following steps:

1. Display a stylized banner.
2. Generate a random ETH amount within a specified range.
3. Encode the provided Solana address into hexadecimal format.
4. Build and sign the Ethereum transaction.
5. Send the transaction to the Ethereum network.
6. Output the transaction hash upon success.

## Example Output

```plaintext
          _    _ _     _     _             _____          _
         | |  | (_)   | |   | |           / ____|        | |
         | |__| |_  __| | __| | ___ _ __ | |     ___   __| | ___
         |  __  | |/ _` |/ _` |/ _ \ '_ \| |    / _ \ / _` |/ _ \
         | |  | | | (_| | (_| |  __/ | | | |___| (_) | (_| |  __/
         |_|  |_|_|\__,_|\__,_|\___|_| |_|\_____\___/ \__,_|\___|

                    GasZip to Eclipse by Aero25x
                     https://t.me/hidden_coding


Sender Address: 0xYourEthereumAddressHere
Nonce: 12
Full hex data for gasZip: 0x03abcdef1234567890abcdef1234567890abcdef0148
Value (Wei): 1400000000000000
Max Priority Fee (Wei): 100000
Max Fee (Wei): 5428706
Transaction details:
  nonce: 12
  to: 0x391E7C679d29bD940d63be94AD22A25d25b5A604
  value: 1400000000000000
  gas: 21726
  maxPriorityFeePerGas: 100000
  maxFeePerGas: 5428706
  data: 0x03abcdef1234567890abcdef1234567890abcdef0148
  chainId: 8453
  type: 2
Transaction sent with hash: 0xYourTransactionHashHere
Transaction successful with hash: 0xYourTransactionHashHere
```

## Requirements

Ensure you have the following Python packages installed. You can install them using `pip` and the provided `requirements.txt`.

- Python 3.7+
- `web3`==6.5.0
- `base58`==2.1.1

**`requirements.txt`**

```plaintext
web3==6.5.0
base58==2.1.1
```

Install dependencies using:

```bash
pip install -r requirements.txt
```

## Troubleshooting

- **Connection Errors**: Ensure your Ethereum node provider URL (e.g., Infura) is correct and that you have an active internet connection.
- **Invalid Private Key**: Double-check that your private key is correct and securely stored in environment variables.
- **Insufficient Funds**: Ensure your Ethereum account has enough ETH to cover the transaction amount and gas fees.
- **Solana Address Issues**: Verify that your Solana address is valid and correctly formatted in Base58.

For further assistance, please reach out via the [Contact](#contact) section.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

- **Developer**: Aero25x
- **Telegram**: [@hidden_coding](https://t.me/hidden_coding)

Feel free to open issues or submit pull requests for improvements and feature requests.

---

© 2024 GasZip to Eclipse by Aero25x. All rights reserved.

[![Join our Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/hidden_coding)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/aero25x)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=x&logoColor=white)](https://x.com/aero25x)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@flaming_chameleon)
