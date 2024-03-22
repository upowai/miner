# Miner

Miner is a sophisticated Python-based mining client designed for participating in a distributed computing network. It connects to a mining pool, downloads computational sub-jobs, processes them, and submits the results. This guide provides instructions on how to set up and run Miner.

## Features

- Connects to a specified mining pool using WebSocket.
- Downloads and processes computational sub-jobs.
- Submits computed gradients back to the mining pool.

## Prerequisites

Before you begin, ensure you have the following installed:

- Python 3.6 or higher
- `pip` for installing Python packages
- An active internet connection

## Installation

1. **Clone the Repository**

   Clone the Miner repository to your local machine using:

   ```bash
   git clone https://github.com/upowai/miner.git
   ```

2. **Install Dependencies**

   Navigate to the cloned directory and install the required Python packages:

   ```bash
   pip3 install -r requirements.txt
   ```

3. **Prepare Your Development Environment**

   Depending on your operating system, you may need to install additional tools to ensure the `fastecdsa` Python package and other dependencies compile correctly:

   - **Ubuntu Users:**

     Install the necessary libraries by running:

     ```bash
     sudo apt-get update
     sudo apt-get install libgmp3-dev
     sudo apt-get install build-essential libssl-dev libffi-dev python3-dev
     ```

   - **Windows Users:**

     Install Visual Studio, which includes the necessary C++ build tools. Download it from [https://visualstudio.microsoft.com/vs/preview/](https://visualstudio.microsoft.com/vs/preview/) and ensure to select the C++ workload during installation.
     [wikihow Install Clang on Windows](https://www.wikihow.com/Install-Clang-on-Windows)

   - **macOS Users:**

     Install Xcode or the standalone Command Line Tools for Xcode, which include `clang`. This can be done by installing Xcode from the Mac App Store or by running the following command in the terminal:

     ```bash
     xcode-select --install
     ```

     For users who prefer not to install Xcode, downloading Command Line Tools for Xcode from [Apple Developer Downloads](https://developer.apple.com/download/more/) is an alternative.
     [https://ics.uci.edu/~pattis/common/handouts/macclion/clang.html](https://ics.uci.edu/~pattis/common/handouts/macclion/clang.html)

Please ensure these tools are correctly installed and configured on your system before proceeding with the installation of the Python package dependencies.

## Configuration

Miner requires specific command-line arguments to start:

- `--MINER_POOL_IP`: The IP address of the miner pool.
- `--MINER_POOL_PORT`: The port number of the miner pool.
- `--WALLET_ADDRESS`: Your wallet address for receiving mining rewards.

## Usage

To run Miner, use the following command:

```bash
python3 miner.py --MINER_POOL_IP "127.0.0.1" --MINER_POOL_PORT 5501 --WALLET_ADDRESS "your_wallet_address"
```

Replace `"127.0.0.1"`, `5501`, and `"your_wallet_address"` with the appropriate miner pool IP, port, and your wallet address.

## Logging

Miner provides detailed logging of its operations, including connection status, job processing, and error reports. This information is crucial for monitoring the miner's performance and troubleshooting issues.

## Contributing

Contributions to Miner are welcome. Please ensure that your code adheres to the project's coding standards and includes appropriate tests.
