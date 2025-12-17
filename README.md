# 📱 Hello World DApp - Flutter & Ethereum

**Yasser Daoud**
*Master's Student in Data Analytics and Artificial Intelligence*

📧 Email: [yasser.daoud@edu.uiz.ac.ma](mailto:yasser.daoud@edu.uiz.ac.ma)
🔗 LinkedIn: [https://www.linkedin.com/in/yasser-daoud-799893288/](https://www.linkedin.com/in/yasser-daoud-799893288/)

---

## 📖 Project Overview

This project is a **Decentralized Application (DApp)** that showcases the connection between a **Flutter** mobile application and an **Ethereum** blockchain backend.

The objective was to explore the intersection of mobile app development and blockchain technology by enabling users to interact with a smart contract on a local Ethereum testnet, allowing them to read and modify persistent data on the blockchain.

---

## 🚀 Key Features

* **Smart Contract Implementation:** A Solidity-based contract (`HelloWorld.sol`) that maintains and updates a string variable on the blockchain
* **Local Development Environment:** Utilizes **Ganache** as a personal Ethereum blockchain for development and testing
* **Automated Deployment:** Contract deployment and migration handled by **Truffle Framework**
* **Cross-Platform Interface:** A responsive Flutter application providing an intuitive user interface
* **Blockchain Connectivity:**

  * Integration with Ethereum using the `web3dart` library for JSON-RPC communication
  * Secure transaction signing using private key authentication
  * Reactive state management powered by the `Provider` package
  * HTTP-based connectivity compatible across multiple platforms

---

## 🛠️ Technology Stack

* **Mobile Framework:** Flutter (Dart)
* **Blockchain Development:** Solidity (v0.5.9)
* **Development Tools:** Truffle Suite, Ganache GUI
* **Supporting Libraries:** `web3dart`, `provider`, `http`

---

## ⚙️ Setup Instructions

### Prerequisites Installation

Ensure the following tools are installed on your system:

* [Node.js & NPM](https://nodejs.org/)
* [Flutter SDK](https://flutter.dev/docs/get-started/install)
* [Ganache](https://www.trufflesuite.com/ganache) (Desktop application)

### Repository Setup

```bash
git clone https://github.com/YOUR-USERNAME/ethereum-flutter-demo.git
cd ethereum-flutter-demo
```

### Dependency Installation

```bash
# Install Flutter packages
flutter pub get

# Install Truffle globally
npm install -g truffle
```

### Blockchain Configuration

1. Launch Ganache and start a new Ethereum workspace
2. Note the RPC server address (default: `http://127.0.0.1:7545`)

### Smart Contract Deployment

```bash
# Compile and deploy the contract
truffle compile
truffle migrate --reset
```

### Application Configuration

1. Update the contract address in `lib/config/contract_config.dart`
2. Add a test account private key from Ganache to the configuration file

### Launch the Application

```bash
flutter run
```

---

## 📁 Project Architecture

```text
ethereum-flutter-demo/
├── blockchain/
│   ├── contracts/               # Solidity smart contracts
│   ├── migrations/              # Deployment scripts
│   └── test/                    # Contract tests
├── lib/
│   ├── screens/                 # Application screens
│   ├── services/                # Blockchain service layer
│   ├── models/                  # Data models
│   ├── utils/                   # Utilities and helpers
│   └── widgets/                 # Reusable UI components
├── assets/                      # Static assets
│   └── abi/                     # Contract ABI files
└── test/                        # Application tests
```

---

## ⚡ Quick Start

For a quick demonstration:

1. Start Ganache and keep it running
2. Run `truffle migrate --reset` in the blockchain directory
3. Update the configuration with the new contract address
4. Launch the app with `flutter run`

---

## 🔧 Configuration Details

* **Network Configuration:** Update the RPC endpoint in `lib/services/web3_service.dart` to match your Ganache instance
* **Authentication:** Use private keys from Ganache accounts for development (never use real private keys in production)
* **Contract Integration:** The ABI file should be placed in `assets/abi/HelloWorld.json` after compilation

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` file for more information.

---

## 🙏 Acknowledgments

* [Flutter](https://flutter.dev/) for the cross-platform framework
* [Truffle Suite](https://www.trufflesuite.com/) for blockchain development tools
* [web3dart](https://pub.dev/packages/web3dart) for Ethereum integration
* All contributors and the open-source community

---

## ❓ Troubleshooting

### Common Issues:

1. **Connection Failed:**

   * Ensure Ganache is running
   * Verify RPC URL matches Ganache server address

2. **Transaction Errors:**

   * Check account has sufficient Ether in Ganache
   * Verify private key is correctly configured

3. **Contract Not Found:**

   * Run `truffle migrate --reset` to redeploy
   * Update contract address in configuration

4. **Flutter Build Issues:**

   * Run `flutter clean` and `flutter pub get`
   * Ensure Flutter SDK is up to date

---

*Note: Replace `YOUR-USERNAME` with your actual GitHub username in the clone URL.*
