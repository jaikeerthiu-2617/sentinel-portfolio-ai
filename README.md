# <p align="center">💎 Sentinel: Multimodal Portfolio Intelligence</p>

<p align="center">
  <b>An Event-Driven AI Pipeline for Indian Equity Markets</b><br>
  <i>Filtering Market Noise • Analyzing Visual Data • Automating Research</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Model-Gemini%203%20Flash-blue?style=for-the-badge&logo=google" />
  <img src="https://img.shields.io/badge/Orchestrator-Make.com-purple?style=for-the-badge&logo=make" />
  <img src="https://img.shields.io/badge/Interface-Telegram-0088cc?style=for-the-badge&logo=telegram" />
</p>

---

### 📖 Overview
**Sentinel** is a high-performance "Signal-to-Noise" engine built for the modern Indian investor. It ingests unstructured data from Telegram forwards, news tickers, and chart screenshots, then uses **Sectoral Heuristics** to determine if the news actually impacts a specific ₹7.5L portfolio.

> **The Problem:** Retail investors are flooded with "Information Overload." As a Data Engineer, I wanted a bot that ignores my professional/career news (e.g., Amazon AWS updates) and only alerts me when my actual capital (e.g., HAL, ONGC, HDFC Bank) is at risk.

---

### 🏗️ System Architecture
The pipeline is designed as a linear, event-driven flow:

```mermaid
graph TD
    A[📩 Telegram Webhook] --> B(🛠️ Data Ingestion & Binary Extract)
    B --> C{📸 Multimodal Analysis}
    C --> D[🤖 Gemini 3 Flash]
    D --> E[🔀 Sectoral Mapping Logic]
    E --> F{🎯 High-Conviction Filter}
    F -- SKIP --> G[🌑 Silent Drop]
    F -- ALERT --> H[📲 Telegram Dispatch]
