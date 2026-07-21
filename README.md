# move-tech-orders-api-persistence

Ponto de partida do **Lab H3 — Validar a persistência**.

Parte do curso **Move Tech** — Magalu × Prósper Digital Skills
Formação em Cloud Computing para iniciantes

---

## Contexto

A aplicação já está configurada para usar o PostgreSQL via Kubernetes Secret. O pipeline já cria o Secret automaticamente a cada deploy.

Seu trabalho neste lab é **confirmar que os dados sobrevivem a um redeploy**.

---

## O que você vai fazer

- [ ] Criar pedidos pela API
- [ ] Confirmar os dados antes do redeploy
- [ ] Disparar o redeploy via pipeline
- [ ] Confirmar que os dados persistiram após o redeploy
- [ ] (Se necessário) Diagnosticar e corrigir

---

## Pré-requisito

Configure o GitHub Secret `DATABASE_URL` com a string de conexão do seu PostgreSQL antes de disparar o pipeline:

```
postgresql://move-tech-user:<senha>@<host>:5432/orders
```

---

## Secrets necessários no GitHub

Configure em Settings → Secrets and variables → Actions:

| Secret | Descrição |
|---|---|
| `MGC_REGISTRY_USER` | Usuário do Container Registry da MGC |
| `MGC_REGISTRY_PASSWORD` | Senha do Container Registry da MGC |
| `MGC_REGISTRY_NAME` | Nome do registry na MGC |
| `MGC_KUBECONFIG` | Conteúdo do kubeconfig.yaml |
| `DATABASE_URL` | String de conexão do PostgreSQL |

---

## Como rodar localmente

**Pré-requisito:** Docker Desktop instalado.

```bash
docker compose up --build
```

Acesse: http://localhost:8000/docs
