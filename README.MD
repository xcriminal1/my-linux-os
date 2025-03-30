# My Linux OS

## Overview
This project is a custom Linux-based operating system built from scratch. The goal is to develop a minimal Linux OS that can run in VirtualBox or on any laptop, incorporating features from other Linux distributions over time.

## Features
- Custom-built Linux kernel
- Runs on VirtualBox or QEMU
- Minimal root filesystem
- GRUB bootloader integration
- Future enhancements: Custom UI, package manager, security features

## Getting Started

### Prerequisites
Ensure you have the following installed on your system:
- **WSL (Windows Subsystem for Linux) + Ubuntu** (if using Windows)
- **VS Code with Remote-WSL Extension**
- **Essential Linux packages:**
  ```bash
  sudo apt update
  sudo apt install build-essential gcc make flex bison libssl-dev grub-pc-bin qemu-system-x86

## Setup Instructions

### Clone the Repository
```bash
git clone https://github.com/xcriminal1/my-linux-os.git
cd my-linux-os
```

## Download the Linux Kernel

```bash
wget https://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.8.tar.xz
tar -xvf linux-6.8.tar.xz
mv linux-6.8 kernel
cd kernel
```

## Configure the Kernel

```bash
make menuconfig
```

## Compile the Kernel

```bash
make -j$(nproc)
make modules_install
make install
markdown
Copy
Edit
```

## Boot the Kernel in QEMU

```bash
qemu-system-x86_64 -kernel arch/x86/boot/bzImage
```

## Future Plans
- Add a user-friendly shell  
- Develop a package manager  
- Enhance security features  
- Improve system performance  

## Contributing
Feel free to contribute by submitting issues or pull requests.

## License
This project is licensed under the MIT License.
