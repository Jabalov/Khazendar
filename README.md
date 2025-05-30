# 🧠 Feature Store Simulator

A fully modular, production-like Feature Store framework built from scratch — supporting batch and real-time feature engineering, metadata tracking, and feature serving.

## 🧩 Core Components
- **Feature Registry**: PostgreSQL with FastAPI API for registering and managing features
- **Offline Store**: Parquet files (via PySpark) for batch feature generation and backfills
- **Online Store**: Redis for real-time feature serving
- **Materialization Tracker**: Auto-updates feature freshness + writes logs
- **Feature Syncer**: Moves batch features to Redis after materialization
- **Monitoring**: Prometheus + Grafana dashboard integration
- **Time-Travel Retrieval**: Point-in-time feature lookups for safe ML training

## 🔁 How to Use
```bash
make up             # Start Postgres + Redis + Spark
make serve          # Run FastAPI on http://localhost:8000
make sync           # Sync features to Redis
make test           # Run all unit tests
