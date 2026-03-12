# Real-Time Market Data Platform (Backend)

Real-time stock and cryptocurrency market data platform built with **Spring Boot microservices** and **React**.

The system uses **Apache Kafka** for event streaming, **Redis** for real-time caching, and **WebSocket** for live data delivery to the frontend dashboard.

---

# Microservices Architecture

## quote-service

### Responsibilities
- Receive real-time price streams
- Publish market price events to Kafka
- Provide REST APIs for market data

### APIs
- Company profile
- Financial metrics
- Analyst recommendations
- Market news

### Data Sources
- Finnhub API
- Binance API

---

## candle-service

### Responsibilities
- Provide historical candlestick (K-line) data
- Serve chart data for frontend visualization

### Data Source
- AlphaVantage API

---

## gateway-service

### Responsibilities
- Central API Gateway
- Route requests to microservices
- Provide REST and WebSocket endpoints
- Unified API entry point for frontend

---

# Technology Stack

## Backend

- Java
- Spring Boot
- Spring WebSocket
- Spring Kafka

## Infrastructure

- Apache Kafka
- Redis
- Docker

## Architecture

- Microservices Architecture
- Event-Driven Architecture

---

# System Flow

1. Market data is received from external APIs  
2. `quote-service` publishes events to Kafka  
3. Redis caches the latest market data  
4. `gateway-service` pushes updates via WebSocket  
5. React dashboard displays real-time market data  

---

# Features

- Real-time stock and crypto price streaming
- Interactive candlestick charts
- Company profile and financial metrics
- Analyst recommendation aggregation
- Market news integration
- Event-driven microservice architecture

## Architecture Highlights

- Microservices architecture
- Event-driven system design
- Real-time market data streaming
- Kafka-based event pipeline
- WebSocket live dashboard updates
- Redis real-time cache layer
