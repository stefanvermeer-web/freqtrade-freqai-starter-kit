# Freqtrade + FreqAI Docker Starter Architecture (Bitvavo EUR & Global USDT)

[![Freqtrade](https://img.shields.io/badge/Freqtrade-Ready-blue.svg)](https://www.freqtrade.io/)
[![FreqAI](https://img.shields.io/badge/FreqAI-LightGBMRegressor-teal.svg)](https://www.freqtrade.io/en/stable/freqai/)
[![Docker](https://img.shields.io/badge/Deployment-Docker%20Compose-2496ED.svg)](https://www.docker.com/)
[![Mode](https://img.shields.io/badge/Default%20Mode-Dry--Run%20Safe-success.svg)](#safety--disclaimer)

A clean, production-oriented architecture overview and starter blueprint for running **Freqtrade** with **FreqAI (`LightGBMRegressor`)** in **Docker** on 30-minute spot markets — tailored for both **Bitvavo (EUR)** and **global exchanges (USDT)**.

> **Looking for the complete plug-and-play package?**  
> **[Get the Full Freqtrade FreqAI Starter Kit on Gumroad →](https://vermeerist2.gumroad.com/l/freqtrade-freqai-starter-kit)**  
> *Includes ready-to-use configuration templates, V2 strategy structure, Docker Compose setup, and step-by-step quickstart documentation.*

---

## Overview

Setting up Freqtrade alongside FreqAI, Docker containers, FreqUI monitoring, and exchange-specific filters from scratch takes considerable trial and error. This project documents a structured, repeatable setup designed for 24/7 operation on a dedicated mini PC, home server, or VPS.

### Key Architectural Highlights
- **30m Spot Market Focus:** Evaluates 30-minute candles to balance signal quality with manageable noise.
- **Machine Learning + Classic Technical Confirmation:** Combines `LightGBMRegressor` predictions via FreqAI with trend, momentum, and volume filters (`RSI`, `ADX`, `EMA 20`, and volume thresholds).
- **Structured Risk & Exit Management:** Uses stepped profit targets (`minimal_roi`) and trailing stop logic once trades move into profit, rather than chasing impulsive entries.
- **Multi-Exchange Ready:** Separate configuration blueprints for European **Bitvavo (`EUR` pairs)** and international **USDT spot markets**.
- **Containerized & Observable:** Runs cleanly via Docker Compose with full **FreqUI** web dashboard access and `dry_run` enabled by default.

---

## What's Inside the Complete Starter Kit

1. **Exchange Configuration Templates (`config.json`):** Pre-structured configurations for **Bitvavo (EUR)** and **Global Exchanges (USDT)** with safe `"dry_run": true` defaults.
2. **V2 Strategy & FreqAI Blueprint:** Clean strategy layout combining `LightGBMRegressor` predictions with `RSI`, `ADX`, `EMA 20`, and volume confirmation.
3. **Docker & FreqUI Deployment Files:** Ready-to-run `docker-compose.yml` setup with local FreqUI monitoring.
4. **Quickstart & Setup Guide:** Step-by-step instructions from unzipping to launching your first `dry_run` session.

👉 **[Download the Freqtrade FreqAI Starter Kit on Gumroad](https://vermeerist2.gumroad.com/l/freqtrade-freqai-starter-kit)**

---

## Safety & Disclaimer

This repository and the linked Starter Kit are provided strictly for **educational, technical, and configuration purposes**. Nothing in this project constitutes financial or investment advice, and no trading profits are guaranteed. Always validate setups in `dry_run` mode first and never trade with capital you cannot afford to lose.
