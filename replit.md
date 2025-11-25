# WorldBanc - Learn Linux Project

## Overview
This is a learning project from [Boot.dev](https://www.boot.dev) for the "Learn Terminals and Shells" course. It provides a simulated banking filesystem structure with CLI tools and scripts for practicing Linux/Unix command-line skills.

## Project Structure
- **worldbanc/private/** - Contains internal tools, scripts, and data
  - **bin/** - Shell scripts for various operations
  - **cmd/** - Go utilities for generating logs and transactions
  - **customers/** - Customer records (CSV)
  - **logs/** - System logs
  - **transactions/** - Transaction data and backups
  
- **worldbanc/public/** - Public-facing information
  - **products/** - Product descriptions for accounts, credit cards, loans, etc.
  - **company_info.md** - Company information
  - **key.txt** - Example private key (for learning purposes)

## Main Components

### Shell Scripts
- `worldbanc.sh` - Main CLI tool for interacting with the system
- `process_transactions.sh` - Process transaction data
- `genids.sh` - Generate IDs
- `malicious.sh` - Example script demonstrating signal handling
- `warn.sh` - Warning/alert script

### Go Utilities
- `genlogs` - Generates sample log files
- `gentransactions` - Generates sample transaction CSV files

## How to Use

### PATH Configuration
The `worldbanc/private/bin` directory has been added to your PATH in `~/.profile`, which means you can run any of the shell scripts (like `worldbanc.sh`) from any directory without specifying the full path.

To apply PATH changes in a new shell session:
```bash
source ~/.profile
```

### Run the Main CLI
The main WorldBanc CLI tool is set up as the default workflow and will prompt you for your name and email. You can also run it directly from any directory:
```bash
worldbanc.sh
```

### Build and Run Go Utilities
```bash
# Generate logs
cd worldbanc/private/cmd/genlogs
go run main.go

# Generate transactions
cd worldbanc/private/cmd/gentransactions
go run main.go
```

### Explore the Filesystem
This project is designed for practicing Linux commands like `cd`, `ls`, `cat`, `grep`, `find`, etc.

## Recent Changes
- 2025-11-25: Configured PATH in ~/.profile to allow running worldbanc.sh from any directory
- 2025-01-13: Initial setup in Replit environment
  - Added Go 1.24 toolchain
  - Made shell scripts executable
  - Created .gitignore for Go projects

## Notes
This is an educational project. The "private key" and other sensitive-looking files are intentionally placed for learning purposes and contain no real credentials.
