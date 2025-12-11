# AlgoFi 🎨🎵

<div align="center">

![Algorand](https://img.shields.io/badge/Algorand-TestNet-00D4AA?style=for-the-badge&logo=algorand&logoColor=white)
![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-Express-339933?style=for-the-badge&logo=node.js&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**A decentralized NFT marketplace on Algorand where creators mint, showcase, and distribute digital art, music, and collectibles with lightning-fast transactions and minimal fees.**

[Demo](#) • [Documentation](#-resources) • [Report Bug](https://github.com/yourusername/algofi/issues) • [Request Feature](https://github.com/yourusername/algofi/issues)

</div>

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Why AlgoFi?](#-why-algofi)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Usage Guide](#-usage-guide)
- [API Reference](#-api-reference)
- [Smart Contracts](#-smart-contracts)
- [Security](#-security)
- [Troubleshooting](#-troubleshooting)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [Resources](#-resources)
- [License](#-license)

---

## 🌟 Overview

AlgoFi is a next-generation NFT marketplace built on the Algorand blockchain, designed to empower creators and collectors with a seamless, low-cost platform for minting, trading, and discovering digital assets. Whether you're an artist, musician, or collector, AlgoFi provides the tools you need to participate in the decentralized economy.

**What Makes It Special?**

- **Multi-Asset Support**: Native support for art, music, and digital collectibles
- **Flexible Monetization**: Create both purchasable assets and free-to-claim collectibles
- **Lightning Fast**: Transactions finalize in just 4.5 seconds
- **Minimal Costs**: Transaction fees as low as 0.001 ALGO (~$0.0002)
- **Eco-Friendly**: Built on Algorand's carbon-negative blockchain

---

## ✨ Key Features

### For Creators 🎨
- **🎭 Multi-Format NFT Minting**: Support for images (JPG, PNG, GIF), audio (MP3, WAV), and video files
- **💰 Flexible Pricing Models**: Set fixed prices or offer NFTs for free
- **📊 Creator Dashboard**: Real-time analytics on your minted NFTs and sales
- **🔐 Wallet-Based Authentication**: Secure, passwordless access via Pera Wallet

### For Collectors 🖼️
- **🔍 Advanced Search & Filtering**: Find NFTs by type, price range, creator, and more
- **💳 One-Click Purchases**: Seamless buying experience with instant confirmation
- **📱 Portfolio Management**: Track your collection value and transaction history
- **🎁 Free Claims**: Discover and claim non-purchasable NFTs from creators

### Technical Features ⚙️
- **Smart Contract Architecture**: Fully auditable on-chain logic for marketplace operations
- **Atomic Transactions**: Guaranteed execution with no partial failures
- **Platform Fee Distribution**: Transparent 2.5% fee structure
- **RESTful API**: Clean, documented endpoints for third-party integrations

---

## 🚀 Why AlgoFi?

| Feature | AlgoFi (Algorand) | Ethereum NFTs | Solana NFTs |
|---------|-------------------|---------------|-------------|
| **Transaction Speed** | 4.5 seconds | 12-20 seconds | ~1 second |
| **Transaction Cost** | ~$0.0002 | $5-50+ | $0.01-0.50 |
| **Carbon Footprint** | Carbon Negative | High | Medium |
| **Finality** | Instant | ~15 mins | ~1 min |

---

## 🛠️ Tech Stack

### Frontend Layer
- React 18.2.0 → Modern UI framework
- Tailwind CSS 3.3.0 → Utility-first styling
- React Router 6.x → Client-side routing
- Pera Wallet Connect → Algorand wallet integration

### Backend Layer
- Node.js 16+ → JavaScript runtime
- Express.js 4.x → Web framework
- Algorand SDK → Blockchain integration
- CORS → Cross-origin resource sharing

### Blockchain Layer
- PyTeal → Smart contract development
- TEAL → Algorand bytecode
- Algorand TestNet → Development network
- ASA Standard → Token standard

---

## 🚦 Getting Started

### Prerequisites

- **Node.js** v16+ ([Download](https://nodejs.org/))
- **Python** 3.7+ ([Download](https://python.org/))
- **Git** ([Download](https://git-scm.com/))
- **Pera Wallet** ([iOS](https://apps.apple.com/app/id1459898525) | [Android](https://play.google.com/store/apps/details?id=com.algorand.android))

### Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/algofi.git
cd algofi

# Backend setup
cd backend
npm install
cp .env.example .env
npm run dev

# Frontend setup (new terminal)
cd frontend
npm install
cp .env.example .env
npm start
```

**Application URLs:**
- Frontend: http://localhost:3000
- Backend: http://localhost:5000

### Environment Configuration

**Backend `.env`:**
```env
PORT=5000
ALGOD_SERVER=https://testnet-api.algonode.cloud
APP_ID=YOUR_DEPLOYED_APP_ID
PLATFORM_WALLET=YOUR_PLATFORM_WALLET_ADDRESS
PLATFORM_FEE=250  # 2.5% in basis points
```

**Frontend `.env`:**
```env
REACT_APP_API_URL=http://localhost:5000/api
REACT_APP_ALGOD_SERVER=https://testnet-api.algonode.cloud
REACT_APP_APP_ID=YOUR_DEPLOYED_APP_ID
REACT_APP_NETWORK=testnet
REACT_APP_PLATFORM_FEE=2.5
```

### Smart Contract Deployment

```bash
cd smart_contracts
pip install pyteal py-algorand-sdk
python algomint_contract.py

# Deploy using goal CLI
goal app create \
  --creator YOUR_WALLET_ADDRESS \
  --approval-prog approval.teal \
  --clear-prog clear.teal \
  --global-byteslices 1 \
  --global-ints 3 \
  --local-byteslices 5 \
  --local-ints 2
```

---

## 📖 Usage Guide

### For Creators: Minting NFTs

1. **Get TestNet ALGO**: Visit [Algorand TestNet Dispenser](https://bank.testnet.algorand.network/)
2. **Connect Wallet**: Click "Connect Wallet" and approve in Pera Wallet
3. **Navigate to Mint**: Click "Mint" in the navigation menu
4. **Fill NFT Details**:
   - Name: "Sunset Over Mountains"
   - Description: "A breathtaking view..."
   - Type: Art / Music / Standard
   - Upload File
   - Set as Purchasable (optional)
   - Set Price (if purchasable)
5. **Submit & Sign**: Click "Mint NFT" and confirm in Pera Wallet
6. **Success**: View your NFT in Portfolio or list on Marketplace

### For Collectors: Purchasing NFTs

1. **Browse Marketplace**: Use filters to find NFTs by type, price range, or creator
2. **View Details**: Click on any NFT to see full metadata and history
3. **Purchase**: Click "Buy Now" and confirm the transaction
4. **Opt-In** (first time): Sign opt-in transaction (0.001 ALGO), then complete purchase
5. **View Collection**: Check your Portfolio for all owned NFTs

---

## 🔌 API Reference

### Base URL
```
http://localhost:5000/api
```

### NFT Endpoints

#### Mint NFT
```http
POST /nfts/mint
```
**Request:**
```json
{
  "creator": "ALGORAND_ADDRESS",
  "name": "My Artwork",
  "description": "A beautiful piece",
  "type": "art",
  "fileUrl": "https://ipfs.io/ipfs/...",
  "purchasable": true,
  "price": 5000000
}
```

#### List NFT for Sale
```http
POST /nfts/list
```
**Request:**
```json
{
  "seller": "ALGORAND_ADDRESS",
  "assetId": 123456789,
  "price": 5000000
}
```

#### Buy NFT
```http
POST /nfts/buy
```
**Request:**
```json
{
  "buyer": "ALGORAND_ADDRESS",
  "assetId": 123456789,
  "seller": "SELLER_ADDRESS"
}
```

#### Get NFT Details
```http
GET /nfts/details/:assetId
```

#### Get Account NFTs
```http
GET /nfts/account/:address
```

#### Get Marketplace Listings
```http
GET /nfts/marketplace?type=art&minPrice=0&maxPrice=1000000000
```

**Query Parameters:**
- `type`: Filter by NFT type (art, music, standard)
- `minPrice`: Minimum price in microAlgos
- `maxPrice`: Maximum price in microAlgos
- `page`: Page number for pagination
- `limit`: Items per page (default: 20)

### Transaction Endpoints

#### Submit Signed Transaction
```http
POST /nfts/submit
```

#### Create Opt-In Transaction
```http
POST /nfts/opt-in
```

---

## 📜 Smart Contracts

### Global State Schema
```python
GlobalSchema:
  - platform_wallet (bytes): Address receiving platform fees
  - total_sales (int): Total completed sales
  - total_volume (int): Total trading volume in microAlgos
  - platform_fee (int): Fee percentage in basis points (250 = 2.5%)
```

### Local State Schema
```python
LocalSchema (per user):
  - listed_assets (bytes): Comma-separated asset IDs
  - total_minted (int): Number of NFTs minted
  - total_purchased (int): Number of NFTs purchased
  - sales_volume (int): Total sales volume for creator
```

### Core Functions

**Initialize Contract**
```python
def initialize(platform_wallet: abi.Address, fee: abi.Uint64)
```

**Mint NFT**
```python
def mint_nft(name: abi.String, unit_name: abi.String, url: abi.String)
```

**List NFT**
```python
def list_nft(asset: abi.Asset, price: abi.Uint64)
```

**Buy NFT**
```python
def buy_nft(asset: abi.Asset, seller: abi.Account)
# Handles payment distribution:
# - Seller receives (price - platform_fee)
# - Platform receives platform_fee
# - Asset transfers to buyer
```

---

## 🔒 Security

### Best Practices
- ✅ Environment variables for sensitive data
- ✅ Private keys never exposed to frontend
- ✅ Transaction verification before submission
- ✅ Rate limiting on API endpoints
- ✅ Input validation and sanitization
- ✅ CORS configuration for known origins

### Security Checklist
- [ ] Never commit `.env` files
- [ ] Use strong mnemonic phrases
- [ ] Verify transactions in Pera Wallet
- [ ] Keep dependencies updated (`npm audit fix`)
- [ ] Use TestNet for development
- [ ] Audit contracts before MainNet
- [ ] Implement rate limiting
- [ ] Enable HTTPS in production

### Reporting Vulnerabilities
Email: security@algofi.example.com (Do not open public issues)

---

## 🔧 Troubleshooting

### Wallet Won't Connect
- Clear browser cache
- Ensure Pera Wallet extension is installed
- Check TestNet network in Pera Wallet settings
- Try disconnecting and reconnecting

### Transaction Fails
```bash
# Check balance (need > 0.1 ALGO)
# Verify APP_ID in .env files
# Ensure wallet opted into application
goal app optin --app-id YOUR_APP_ID --from YOUR_ADDRESS

# Check transaction on explorer for error details
```

### Backend Connection Issues
```bash
# Verify backend is running
curl http://localhost:5000/api/health

# Check CORS configuration
# Ensure REACT_APP_API_URL matches backend URL
```

### NFT Not Appearing
- Wait for blockchain confirmation (~4.5 seconds)
- Refresh the page
- Check asset on [TestNet Explorer](https://testnet.algoexplorer.io/)
- Verify asset opt-in status

### Debug Mode
```bash
# Backend
DEBUG=* npm run dev

# Frontend
REACT_APP_DEBUG=true npm start
```

---

## 🗺️ Roadmap

### Phase 1: Core Functionality ✅
- [x] Basic NFT minting
- [x] Marketplace listing
- [x] Buy/sell transactions
- [x] Wallet integration
- [x] Portfolio view

### Phase 2: Enhanced Features 🚧
- [ ] IPFS integration for decentralized storage
- [ ] Royalty system for secondary sales
- [ ] Collection creation and management
- [ ] Advanced search and filtering
- [ ] Activity feed and notifications

### Phase 3: Social Features 📅
- [ ] User profiles and verification badges
- [ ] Follow/unfollow creators
- [ ] Like and comment on NFTs
- [ ] Share to social media
- [ ] Creator analytics dashboard

### Phase 4: Advanced Trading 📅
- [ ] Auction functionality (English & Dutch)
- [ ] Bundle sales and offers
- [ ] Price history charts
- [ ] Rarity scoring system
- [ ] Cross-chain bridging

### Phase 5: Platform Growth 📅
- [ ] Mobile app (React Native)
- [ ] MainNet deployment
- [ ] DAO governance
- [ ] Token rewards program
- [ ] API for third-party integrations

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Ways to Contribute
- 🐛 Report bugs and issues
- 💡 Suggest new features
- 📝 Improve documentation
- 🔧 Submit pull requests
- 🎨 Design UI/UX improvements

### Development Workflow

```bash
# 1. Fork and clone
git clone https://github.com/yourusername/algofi.git

# 2. Create feature branch
git checkout -b feature/amazing-feature

# 3. Make changes and commit
git commit -m "feat: add amazing feature"

# 4. Push and create PR
git push origin feature/amazing-feature
```

We follow [Conventional Commits](https://www.conventionalcommits.org/):
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation
- `style:` Formatting
- `refactor:` Code refactoring
- `test:` Tests
- `chore:` Maintenance

### Code Style

**JavaScript/React:**
```javascript
const MyComponent = ({ prop1, prop2 }) => {
  const [isLoading, setIsLoading] = useState(false);
  
  const handleConnect = async () => {
    // Implementation
  };
  
  return <div>...</div>;
};
```

**Python:**
```python
def mint_nft(name: str, url: str) -> int:
    """
    Mint a new NFT.
    
    Args:
        name: NFT name
        url: Metadata URL
        
    Returns:
        Asset ID of minted NFT
    """
    # Implementation
```

---

## 📚 Resources

### Algorand Documentation
- [Developer Portal](https://developer.algorand.org/)
- [Python SDK](https://py-algorand-sdk.readthedocs.io/)
- [JavaScript SDK](https://algorand.github.io/js-algorand-sdk/)
- [PyTeal Documentation](https://pyteal.readthedocs.io/)

### Tools & Services
- [Pera Wallet](https://perawallet.app/)
- [AlgoExplorer](https://algoexplorer.io/)
- [TestNet Dispenser](https://bank.testnet.algorand.network/)
- [Algorand Sandbox](https://github.com/algorand/sandbox)

### Learning Resources
- [Algorand Developer Bootcamp](https://developer.algorand.org/bootcamp/)
- [Algorand Solutions](https://developer.algorand.org/solutions/)
- [Community Forum](https://forum.algorand.org/)

### Community
- **Discord**: [discord.gg/algofi](https://discord.gg/algofi)
- **Twitter**: [@algofi_nft](https://twitter.com/algofi_nft)
- **Telegram**: [t.me/algofi](https://t.me/algofi)

### Support
- 📧 Email: support@algofi.example.com
- 💬 Discord: Join our community server
- 🐛 Issues: [GitHub Issues](https://github.com/yourusername/algofi/issues)
- 📚 Docs: [Full Documentation](https://docs.algofi.example.com)

---

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Algorand Foundation for the incredible blockchain platform
- Pera Wallet team for seamless wallet integration
- Open source community for inspiration and support
- All contributors who help make AlgoFi better

---

<div align="center">

**Built with ❤️ on Algorand**

[⬆ Back to Top](#algofi-)

</div>