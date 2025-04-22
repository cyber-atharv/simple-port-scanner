# 🎯 Fast Asynchronous TCP Port Scanner

> A high-concurrency network port scanner built in modern C++ with Boost.Asio for rapid network reconnaissance and open service discovery.

[![Author](https://img.shields.io/badge/Made%20by-cyber--atharv-00ffcc?style=flat-square&logo=github)](https://github.com/cyber-atharv)
[![C++](https://img.shields.io/badge/C%2B%2B-20-00599C?style=flat-square&logo=cplusplus&logoColor=white)](https://isocpp.org)
[![CMake](https://img.shields.io/badge/CMake-3.25+-064F8C?style=flat-square&logo=cmake)](https://cmake.org)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)

---

## 📌 What is a Port Scanner?

Every network service (like web servers on port 80/443 or SSH on port 22) listens on a specific TCP/UDP port. In cybersecurity, **port scanning** is the foundation of network discovery. It maps active devices, identifies listening services, and finds exposed attack surfaces.

This scanner, written by **cyber-atharv**, utilizes asynchronous I/O (`Boost.Asio`) to scan hundreds of ports concurrently without blocking or suffering thread overhead.

---

## ✨ Key Features

- **Asynchronous Non-Blocking Engine:** Employs event-driven sockets to scan thousands of ports in seconds.
- **Flexible Port Syntax:** Scan single ports (`80`), lists (`22,80,443,8080`), or large ranges (`1-65535`).
- **Adjustable Concurrency:** Fine-tune scan speed (`--concurrency 200`) to balance network throughput and packet loss.
- **Accurate State Detection:** Accurately classifies ports as **Open** (connection accepted), **Closed** (RST received), or **Filtered** (timeout / drop).
- **Clean Terminal Output:** Displays scan summaries with response latency metrics.

---

## 🚀 Quick Start & Usage

### 1. Build using CMake
```bash
cd simple-port-scanner
mkdir build && cd build
cmake ..
cmake --build .
```

### 2. Examples

#### 🔹 Scan standard web and management ports
```bash
./simplePortScanner --target 192.168.1.1 --ports 22,80,443,8080
```

#### 🔹 Scan the top 1024 system ports
```bash
./simplePortScanner --target 127.0.0.1 --ports 1-1024 --concurrency 100
```

#### 🔹 Full port scan with custom timeout
```bash
./simplePortScanner --target 10.0.0.5 --ports 1-65535 --timeout 500 --concurrency 500
```

---

## 🧠 Why I Built This

Writing a port scanner in C++ from scratch is an essential milestone in systems and network security programming. It teaches the details of TCP 3-way handshakes (`SYN -> SYN-ACK -> ACK`), socket lifecycle states, asynchronous event loops, and POSIX networking APIs.

---

## ⚠️ Ethical & Legal Disclaimer

> Only scan targets, IP addresses, and subnets that you own or have explicit written permission to test.

---

## 📜 Author & License

- **Author:** [cyber-atharv](https://github.com/cyber-atharv)
- **License:** Open source under the MIT / AGPL License.
