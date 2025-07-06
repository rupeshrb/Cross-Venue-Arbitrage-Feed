# 🚀 Cross-Venue Arbitrage Feed - GoQuant Assignment

## 📌 Overview
A high-performance backend system in modern C++17 that detects real-time spot arbitrage opportunities across multiple cryptocurrency exchanges (Binance, OKX, Bybit). Built with Boost.Beast, multithreading, and SIMD-optimized processing.

## 🎯 Objective
- Ingest L2 orderbook data via WebSocket
- Process real-time bid/ask prices from each exchange
- Detect arbitrage within 10ms latency
- Stream opportunities via WebSocket & expose monitoring API

## ⚙️ Tech Stack
- Language: C++17
- Libraries: Boost.Beast, Boost.ASIO, nlohmann/json
- Concurrency: `std::thread`, `std::mutex`, `boost::lockfree::queue`
- Optimization: SIMD (`<immintrin.h>`), custom memory handling

## 🔧 How to Build

### Prerequisites
- C++17 compiler (tested on `g++ 13+`)
- OpenSSL
- Boost 1.76+

### Build Instructions
```bash
g++ -std=c++17 -o arbitrage_engine src/main.cpp -lssl -lcrypto -lws2_32 -lwsock32
./arbitrage_engine
