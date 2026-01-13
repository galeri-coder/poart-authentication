# 🎨 İlhanArt Gallery - PoArt Authentication System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Gallery](https://img.shields.io/badge/Gallery-İlhanArt-green)](https://www.ilhanart.org)
[![Protocol](https://img.shields.io/badge/Protocol-PoArt%20v1.0-purple)](https://www.ilhanart.org/verify)
[![Artists](https://img.shields.io/badge/Artists-1-blue)](#artists)

> **Blockchain-based Art Authentication System**  
> *"Culture > Capital" - A 975-year civilizational-scale verification protocol*

---

## 📖 About

**PoArt (Proof of Art)** is a blockchain-based authentication system for art collections managed by İlhanArt Gallery. This repository serves as a permanent, cryptographically-secured authentication record for artworks.

### 🏛️ Gallery Information
- **Gallery**: İlhanArt Gallery
- **Location**: Ortaköy, İstanbul, Turkey
- **Website**: [ilhanart.org](https://www.ilhanart.org)
- **Protocol**: PoArt v1.0 (Proof of Art)
- **Philosophy**: Culture > Capital

---

## 🎯 PoArt Protocol Philosophy

```
Culture > Capital

This is not slowness.
This is civilization.
```

**Core Principles:**
- ✅ **365-day continuous cold wallet storage** requirement
- ✅ **Anti-speculation** through temporal commitment
- ✅ **Millennium-scale authentication** (2025-3000)
- ✅ **Mathematical resistance** to flash loans & whale dominance
- ✅ **Cultural preservation** over capital accumulation

---

## 👨‍🎨 Artists

### Current Collections

| Artist | Artworks | Authentication Date | Status | Directory |
|--------|----------|---------------------|--------|-----------|
| **[Ali Naki İlhan](artists/ali-naki-ilhan/)** | 32 | 2025-01-13 | ✅ Authenticated | [`/artists/ali-naki-ilhan/`](artists/ali-naki-ilhan/) |

*More artists will be added as they join the PoArt protocol.*

---

## 📁 Repository Structure

```
ilhanart-poart-authentication/
│
├── artists/                   # Artist-specific collections
│   └── ali-naki-ilhan/       # Ali Naki İlhan's authenticated artworks
│       ├── 01_originals/
│       ├── 02_original_hashes/
│       ├── 03_watermarked/
│       ├── 04_watermarked_hashes/
│       ├── 05_metadata/
│       ├── MASTER_AUTHENTICATION_RECORD.csv
│       └── README.md
│
├── README.md                  # This file
├── LICENSE                    # MIT License
├── CONTRIBUTING.md            # Contribution guidelines
├── GITHUB_SETUP.md           # Setup instructions
└── .gitignore                # Git ignore rules
```

---

## 🔐 Authentication Features

Each artwork receives:

### Digital Authentication
- ✅ **Unique Artwork ID**: Format: `ARTISTNAME_YEAR_XXX`
- ✅ **SHA-512 Cryptographic Hash**: 128-character hexadecimal
- ✅ **QR Code Verification**: Instant mobile authentication
- ✅ **JSON Metadata**: Complete provenance and authentication data
- ✅ **Dual Hash System**: Original + Watermarked verification

### Visual Watermark
```
┌─────────────────────────┐
│     [QR CODE]           │  → Verification URL
│  ilhanart.org/verify    │
│  © İLHAN ART • YEAR     │
│  Ortaköy, İstanbul      │
└─────────────────────────┘
```

**Design Features:**
- Premium green glassmorphism (#10b981)
- Semi-transparent overlay with blur effect
- Bottom-right positioning with 20px padding
- High-quality QR code (Error Correction Level H)

---

## 🚀 Quick Start

### Verify an Artwork

1. **Locate the artwork** in the appropriate artist directory
2. **Scan QR code** on the watermarked image
3. **Visit verification URL**: `https://www.ilhanart.org/verify?id=ARTWORK_ID`
4. **Compare SHA-512 hash** with your file
5. **Check JSON metadata** for complete provenance

### Calculate SHA-512 Hash

```bash
# Linux/Mac
shasum -a 512 artwork_file.png

# Windows PowerShell
Get-FileHash -Algorithm SHA512 artwork_file.png
```

### Search Authenticated Artworks

```bash
# Find specific artist
cd artists/ali-naki-ilhan/

# Search in master record
grep "ILHANART_2025_001" MASTER_AUTHENTICATION_RECORD.csv
```

---

## 🔬 Technical Specifications

### Cryptography
- **Algorithm**: SHA-512 (Secure Hash Algorithm 2)
- **Output Length**: 512 bits (128 hex characters)
- **Collision Resistance**: Cryptographically secure
- **Usage**: Dual hashing (original + watermarked)

### Image Processing
- **Format**: PNG (Portable Network Graphics)
- **Compression**: Lossless
- **Color Space**: RGB/RGBA
- **Watermark**: Alpha-blended overlay (200 alpha)

### QR Code
- **Library**: qrcode (Python)
- **Version**: 1 (21×21 modules)
- **Error Correction**: Level H (30% recovery capability)
- **Size**: 120×120 pixels
- **Content**: Verification URL with unique artwork ID

### Metadata
- **Format**: JSON (JavaScript Object Notation)
- **Encoding**: UTF-8
- **Schema**: Custom provenance structure
- **Fields**: 20+ authentication data points

---

## 📊 Statistics

| Metric | Value |
|--------|-------|
| **Total Artists** | 1 |
| **Total Artworks** | 32 |
| **Total Files** | 166+ |
| **Authentication Protocol** | PoArt v1.0 |
| **Timeline** | 2025-3000 (975 years) |
| **Repository Size** | ~86 MB |

---

## 🛠️ Development

### Prerequisites
- Python 3.8+
- Pillow (PIL)
- qrcode
- hashlib (built-in)

### Installation

```bash
# Clone repository
git clone https://github.com/yourusername/ilhanart-poart-authentication.git
cd ilhanart-poart-authentication

# Install dependencies
pip install pillow qrcode
```

### Verify Artwork Programmatically

```python
import hashlib

def calculate_sha512(file_path):
    """Calculate SHA-512 hash of a file"""
    sha512 = hashlib.sha512()
    with open(file_path, 'rb') as f:
        while chunk := f.read(8192):
            sha512.update(chunk)
    return sha512.hexdigest()

# Example usage
hash_value = calculate_sha512("artists/ali-naki-ilhan/01_originals/ILHANART_2025_001_original.png")
print(f"SHA-512: {hash_value}")
```

---

## 📜 License

This project is licensed under the **MIT License** - see [LICENSE](LICENSE) file for details.

**Important**: The authentication system (software, scripts, metadata) is MIT licensed. However, all artworks remain the exclusive intellectual property of their respective artists.

---

## 🤝 Contributing

We welcome contributions! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### How to Contribute
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📞 Contact

- **Gallery**: İlhanArt Gallery
- **Location**: Ortaköy, İstanbul, Turkey
- **Website**: [ilhanart.org](https://www.ilhanart.org)
- **Email**: info@ilhanart.org
- **Twitter**: [@Galerilhan](https://twitter.com/Galerilhan)
- **Verification**: [ilhanart.org/verify](https://www.ilhanart.org/verify)

---

## 🔗 Related Links

- **PoArt Protocol Documentation**: [ilhanart.org/poart](https://www.ilhanart.org/poart)
- **Founding Patrons Program**: [ilhanart.org/patrons](https://www.ilhanart.org/patrons)
- **Live Verification System**: [ilhanart.org/verify](https://www.ilhanart.org/verify)
- **Gallery Website**: [ilhanart.org](https://www.ilhanart.org)

---

## 🌟 Acknowledgments

- **İlhanArt Gallery** - For pioneering the PoArt protocol
- **Ali Naki İlhan** - For creating authenticated artworks
- **PoArt Community** - For supporting culture over capital
- **Contributors** - For improving the authentication system

---

## 🎨 Adding New Artists

To add a new artist to this repository:

1. Create directory: `artists/artist-name/`
2. Follow the structure in `artists/ali-naki-ilhan/`
3. Generate authentication files (SHA-512, watermarks, metadata)
4. Update this README with artist information
5. Submit a Pull Request

**Contact the gallery** for authentication services: info@ilhanart.org

---

<div align="center">

**Made with ❤️ for Culture, not Capital**

[![Website](https://img.shields.io/badge/Website-İlhanArt-blue)](https://www.ilhanart.org)
[![Verify](https://img.shields.io/badge/Verify-Artwork-green)](https://www.ilhanart.org/verify)
[![Twitter](https://img.shields.io/badge/Twitter-@Galerilhan-1DA1F2)](https://twitter.com/Galerilhan)

---

*This is not slowness. This is civilization.*

**PoArt Protocol v1.0** | 2025-3000

</div>
