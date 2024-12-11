# Auto WARP Config Generator 🔄

[![Update Configs](https://github.com/4n0nymou3/auto-warp-config/actions/workflows/update-configs.yml/badge.svg)](https://github.com/4n0nymou3/auto-warp-config/actions/workflows/update-configs.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Automated WARP configuration generator that updates IPv4 and IPv6 endpoints hourly. This project automatically fetches and rotates IP addresses and ports to maintain fresh and working configurations.

## 🌟 Features

- **Automated Updates**: Configurations are automatically updated every hour
- **Dual Protocol Support**: Supports both IPv4 and IPv6 endpoints
- **Failsafe System**: Includes fallback IPs if the main source is unavailable
- **GitHub Actions Integration**: Fully automated workflow
- **Flexible Configuration**: Easy to customize and extend

## 🚀 Getting Started

### Prerequisites

- A GitHub account
- Basic knowledge of Git and GitHub

### Fork and Setup

1. Fork this repository to your GitHub account
2. Enable GitHub Actions:
   - Go to your forked repository's **Settings**
   - Navigate to **Actions → General** (in the left sidebar)
   - Scroll to **Workflow permissions**
   - Select **"Read and write permissions"**
   - Click **Save**

> ⚠️ **Important**: The workflow permissions step is mandatory for both fork and original repository setup. Without this, the automatic updates will not work.

### 📦 Installation

No local installation is required. Once forked and properly configured, the repository will automatically:
- Generate new configurations hourly
- Update the `config.txt` file
- Commit and push changes

## 🔧 Configuration Structure

The generated `config.txt` file contains:
- 2 IPv4 configurations with unique endpoints
- 1 IPv6 configuration
- Standard headers and metadata
- Automatic timestamp updates

Example structure:
```plaintext
//profile-title: base64:8J+RvSBBbm9ueW1vdXM=
//profile-update-interval: 1
...
warp://[IPv4]:[PORT]/?ifp=50-100...#Anon-WoW-IPv4🇩🇪-1
```

## 🔄 How It Works

1. GitHub Actions triggers the workflow hourly
2. Python script fetches fresh IP addresses
3. Generates new configurations with random endpoints
4. Updates the repository with new configurations
5. Automatically commits and pushes changes

## 🛠️ Manual Update

To manually trigger an update:
1. Go to the **Actions** tab
2. Select the **Update Configs** workflow
3. Click **Run workflow**
4. Select **Run workflow** in the popup

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Feel free to submit issues and pull requests.

## ⭐ Support

If you find this project helpful, please give it a star to show your support!

## 🙏 Acknowledgments

Special thanks to:
- [IRCF Space](https://github.com/ircfspace) for providing and maintaining the IP endpoints database
- All contributors and users who help improve this project

---
Made with ❤️ by [4n0nymou3](https://github.com/4n0nymou3)