# Crypto Ingestion Platform

A distributed backend platform for reliable cryptocurrency market data ingestion, processing, and storage.

## Overview

Crypto Ingestion Platform is a backend engineering project focused on building a scalable, fault-tolerant system for collecting and managing cryptocurrency market data from external APIs.

The platform is designed to support historical data ingestion, scheduled synchronization, asynchronous task processing, and efficient bulk database operations.

**Project Status:** Early Development

## Architecture

The planned architecture consists of several independent components:

- **FastAPI** — REST API, authentication, authorization, and task management.
- **PostgreSQL** — Persistent storage for market data, users, and ingestion tasks.
- **Redis** — Message broker for asynchronous task processing.
- **Celery Worker** — Data ingestion, validation, and batch database operations.
- **Celery Beat** — Scheduled ingestion and periodic synchronization.
- **Binance API** — External cryptocurrency market data source.

The system separates HTTP request handling from background processing to support reliable and scalable data ingestion.

## Tech Stack

**Backend**

`Python` · `FastAPI` · `SQLAlchemy` · `Pydantic`

**Data & Task Processing**

`PostgreSQL` · `Redis` · `Celery` · `Alembic`

**Development & Infrastructure**

`uv` · `Ruff` · `pytest` · `Docker` · `Docker Compose`

**CI/CD & Deployment (Planned)**

`GitHub Actions` · `GHCR` · `Kubernetes`

## Getting Started

### Requirements

- Python 3.14
- uv

### Installation

Clone the repository:

```bash
git clone https://github.com/murbaniak25/crypto-ingestion-platform.git
cd crypto-ingestion-platform
```

Install project dependencies:

```bash
uv sync
```

### Development

Run code quality checks:

```bash
uv run ruff check .
uv run ruff format --check .
```

Run tests once the test suite is available:

```bash
uv run pytest
```

## Project Roadmap

**Project Setup**
- [x] Initialize Git repository
- [x] Configure Python environment with uv
- [x] Add Ruff and pytest
- [x] Configure project dependencies

**Database**
- [ ] Set up PostgreSQL with Docker Compose
- [ ] Design database schema
- [ ] Implement SQLAlchemy models
- [ ] Configure Alembic migrations

**Backend API**
- [ ] Implement REST API with FastAPI
- [ ] Implement ingestion task management
- [ ] Add JWT authentication and RBAC

**Data Ingestion**
- [ ] Configure Redis and Celery
- [ ] Implement Binance API integration
- [ ] Implement batch ingestion and UPSERT operations
- [ ] Add scheduled ingestion with Celery Beat
- [ ] Implement retry and failure recovery mechanisms

**Infrastructure & Deployment**
- [ ] Containerize application services
- [ ] Implement automated testing and CI/CD
- [ ] Configure container image publishing
- [ ] Deploy to a local Kubernetes cluster

## Engineering Goals

- Design reliable and idempotent data ingestion workflows.
- Handle asynchronous and concurrent task execution.
- Optimize PostgreSQL operations for large datasets.
- Implement monitoring and failure recovery.
- Build reproducible development and deployment environments.
- Apply production-oriented backend engineering practices.