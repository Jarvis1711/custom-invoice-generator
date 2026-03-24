# Proof of Concept - Custom Invoice Generator

## Idea Reference
- Number: 25
- Title: Custom Invoice Generator
- Description: A PHP-based tool that generates professional PDFs with dynamic branding.

## PoC Scope
- App boots with Flask + SQLite persistence
- CRUD flow works via web UI (`/`, `/items/new`, `/items/<id>/edit`)
- API endpoints return valid JSON (`/api/health`, `/api/items`)
- Deployability assets included (`Dockerfile`, `docker-compose.yml`, `Procfile`)

## Run Evidence (to capture)
```bash
python app.py
curl http://localhost:5000/api/health
curl -X POST http://localhost:5000/api/items -H "Content-Type: application/json" -d '{"title": "Demo item", "details": "Created from PoC command", "status": "active"}'
curl http://localhost:5000/api/items
```

## Metadata
- Generated UTC: 2026-03-24T15:35:11.484537+00:00
- Status: Deployable full-template scaffold complete
