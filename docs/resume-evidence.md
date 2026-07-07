# pickfit Resume Evidence

Service summary:
- FastAPI ML recommendation serving.

Repository evidence:
- Origin workspace: https://github.com/pickfit-ai/pickfit-workspace
- Frontend repo: https://github.com/pickfit-ai/pickfit-fe
- Backend repo: https://github.com/pickfit-ai/pickfit-be
- Personal mirror: https://github.com/cyjoon68/pickfit-workspace

Implementation evidence:
- Frontend: Expo Router, feature-layer API via `ky`, Unistyles UI.
- Backend: domain API contract in `pickfit-be/openapi.yaml`.
- Data: MySQL catalog/recommendation schema plus Redis recommendation cache.
- Infra: Dockerfile, GitHub Actions, ArgoCD, Kubernetes, Grafana dashboard stub.
- Ops: MySQL, Redis, RabbitMQ, Datadog-style logging/telemetry, Sentry env boundary.

Interview proof:
- API: `POST /api/recommendations`, `POST /api/model/retrain`, `GET /api/dashboard`.
- ML rule: cosine similarity ranking over item/user vectors with deterministic smoke coverage.
- Async boundary: recommendation cache writes to Redis and retrain signals publish to RabbitMQ.
- Production angle: separate FE/BE repos, workspace submodules, GitOps manifest, CI rule gates.

Resume bullets:
- Implemented FastAPI ML recommendation serving with explicit API contract and data schema.
- Built public multi-repo Git submodule workspace with org origin and personal mirror.
- Added CI, Docker, GitOps, observability, and dependency-light self-check gates.

Verification:
- `node scripts/self-check.mjs`
- `cd pickfit-fe && npm run self-check`
- backend self-check in `pickfit-be/scripts`
