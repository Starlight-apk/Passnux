> 🌐 **Language / 语言**: [English](setup.md) | [中文](../../setup.md)

# Environment Setup

## Prerequisites

- Debian 13 (trixie) or compatible Linux distribution
- ARM64 (aarch64) architecture
- Python >= 3.10
- Node.js >= 18
- Git

## Clone the Project

```bash
git clone <repository-url>
cd Passnux
```

## Backend Setup

```bash
# Create virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies (TBD)
pip install -r requirements.txt
```

## Frontend Setup

```bash
# Install dependencies (TBD)
cd src/frontend
npm install
```

## Verify Installation

```bash
# Check Python version
python3 --version

# Check Node.js version
node --version
```
