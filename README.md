coffee-shop/
├─ apps/
│  ├─ web/                         # FE: Next.js + TypeScript
│  │  ├─ app/                      # App Router (Next 14+)
│  │  ├─ components/               # UI components
│  │  ├─ features/                 # cart, menu, orders, auth...
│  │  ├─ lib/                       # axios/fetch utils, validators
│  │  ├─ public/
│  │  ├─ tests/                     # FE tests
│  │  ├─ next.config.ts
│  │  └─ package.json
│  │
│  ├─ api-ts/                       # BE Orders/Users/Payments (OOP, TS)
│  │  ├─ src/
│  │  │  ├─ modules/
│  │  │  │  ├─ orders/
│  │  │  │  ├─ users/
│  │  │  │  ├─ payments/
│  │  │  │  └─ notifications/
│  │  │  ├─ shared/                 # middleware, logger, errors
│  │  │  ├─ db/                     # Mongoose models, Mongo connection
│  │  │  ├─ cache/                  # Redis service
│  │  │  └─ main.ts
│  │  ├─ tests/                     # Jest unit/integration
│  │  ├─ Dockerfile
│  │  └─ package.json
│  │
│  ├─ api-laravel/                  # BE Catalog/CMS
│  │  ├─ app/
│  │  ├─ routes/api.php
│  │  ├─ config/database.php        # MongoDB driver config
│  │  ├─ database/                  # migrations (Mongo không cần, seed bằng script)
│  │  ├─ tests/
│  │  ├─ Dockerfile
│  │  └─ composer.json
│  │
│  ├─ svc-django/                   # BE Media Service
│  │  ├─ manage.py
│  │  ├─ src/
│  │  │  ├─ media_service/
│  │  │  │  ├─ apps/transcoder/     # AWS MediaConvert job → HLS
│  │  │  │  └─ apps/webhook/        # cập nhật DB Mongo qua API
│  │  │  └─ tests/
│  │  ├─ Dockerfile
│  │  └─ requirements.txt
│  │
│  ├─ gateway/                      # API Gateway / Nginx (dev)
│  │  ├─ nginx.conf
│  │  └─ Dockerfile
│
├─ packages/
│  ├─ shared-types/                  # DTO, OpenAPI types
│  ├─ eslint-config/
│  ├─ tsconfig/
│  └─ ui/
│
├─ contracts/
│  └─ openapi/
│     ├─ catalog.yaml
│     ├─ orders.yaml
│     └─ media.yaml
│
├─ infra/
│  ├─ terraform/
│  │  ├─ modules/
│  │  │  ├─ vpc/ s3/ redis/ mediaconvert/ ecs/ alb/ cloudfront/ ecr/
│  │  └─ envs/ dev/ staging/ prod/
│  └─ README.md
│
├─ ops/
│  ├─ docker/
│  │  ├─ web.Dockerfile
│  │  ├─ api-ts.Dockerfile
│  │  ├─ api-laravel.Dockerfile
│  │  ├─ svc-django.Dockerfile
│  │  └─ nginx.Dockerfile
│  ├─ compose.dev.yml                # local: MongoDB, Redis, services
│  └─ compose.min.yml
│
├─ .github/workflows/
│  ├─ web.yml
│  ├─ api-ts.yml
│  ├─ api-laravel.yml
│  ├─ svc-django.yml
│  └─ infra.yml
│
├─ docs/
│  ├─ ADRs/
│  ├─ RUNBOOKS/
│  └─ SECURITY.md
│
├─ .env.example
└─ README.md
