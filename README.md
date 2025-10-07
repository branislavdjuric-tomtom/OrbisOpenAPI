# Orbis OpenAPI

This repository contains the OpenAPI (Swagger) specification for the Orbis API and simple viewers to explore the spec easily.

## Structure

- docs/openapi.yaml — OpenAPI 3.0.x specification
- docs/index.html — Swagger UI viewer
- docs/redoc.html — Redoc viewer
- README.md — This file

## Getting started

View the API docs
- Online (preferred): use the links above after enabling GitHub Pages.
- Locally (no extra dependencies):
  1. From the repo root run:
     ```bash
     python3 -m http.server 8080 --directory docs
     ```
  2. Open http://localhost:8080 for Swagger UI
  3. Open http://localhost:8080/redoc.html for Redoc

## Editing the spec

- Edit docs/openapi.yaml (OpenAPI 3.0.x).
- Keep consistent operationId naming (e.g., getHealth, listUsers).
- Document response schemas and examples wherever possible.
- Update info.version when making breaking changes.

Recommended tools
- Visual edit: Stoplight Studio, Redocly, or VS Code + OpenAPI extensions.
- Linting: Spectral CLI
  ```bash
  npm i -g @stoplight/spectral-cli
  spectral lint docs/openapi.yaml
