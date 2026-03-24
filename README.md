# Custom Invoice Generator

## Solution Summary
Production-ready domain application.

This Phase-2 implementation is a domain-ready, deployable web application for **Business & Commerce** workflows.

## Core Capabilities
- Responsive dashboard with KPI cards and recent activity table
- Domain record lifecycle with full CRUD (web + API)
- Dynamic schema fields tailored to this use case
- Status pipeline: `draft, quoted, approved, fulfilled`
- Docker + Gunicorn deployment assets, CI checks, and Pytest tests

## Domain Model
- Primary entity: **Custom Invoice Order**
- Collection: **Custom Invoice Orders**
- Dynamic fields:
- Client Name (`client_name` / text)
- Estimated Value (`estimated_value` / number)
- Delivery Notes (`delivery_notes` / textarea)

## Operational Workflow
1. Create commercial record
2. Estimate value
3. Approve transaction
4. Complete fulfillment

## API
- `GET /api/health`
- `GET /api/schema`
- `GET /api/records`
- `POST /api/records`
- `GET /api/metrics`

## Run Locally
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Docker Run
```bash
docker compose up --build
```

## Proof of Concept
- [proof-of-concept.md](proof-of-concept.md)
- [proof/demo-output.txt](proof/demo-output.txt)
- [proof/ui-preview.svg](proof/ui-preview.svg)
