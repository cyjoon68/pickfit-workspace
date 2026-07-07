# PickFit Workspace

Personalized fit recommendation service.

Repos:
- `pickfit-workspace`: parent workspace and submodule root.
- `pickfit-fe`: Expo app, `ky` API client.
- `pickfit-be`: FastAPI recommendation API with ML-friendly vector ranking.

Architecture:
- FastAPI: recommendation and dashboard endpoints.
- ML libraries: vector scoring boundary, ready for sklearn model training.
- MySQL, Redis, RabbitMQ: catalog, cache, async retrain events.
- GitHub Actions + ArgoCD: CI and GitOps deployment.
- Datadog, Grafana, Sentry: logs, metrics, errors.

Resume bullets:
- Built FastAPI recommendation API with cosine ranking for fit personalization.
- Designed model-serving boundary with retrain/event hooks.
- Maintained multi-repo workspace with public org origin and personal mirror.

Run:
- `docker compose up -d`
- `cd pickfit-be && python -m pytest`
- `cd pickfit-fe && npm install && npm run typecheck`
PickFit git submodule workspace
