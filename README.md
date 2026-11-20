# Transaction Dispute Portal

A full-stack system where bank customers view their transactions, dispute the ones they don't recognise, and follow every dispute they've raised. Dispute agents work a queue of open disputes, review them and approve or reject them, and the customer sees each decision in their dispute history.

This repository holds the **.NET 10 API** and the **Docker Compose** setup for the whole stack. The React web app lives in [`transaction-dispute-portal-web`](https://github.com/McebisiMK/transaction-dispute-portal-web).

| Brief requirement | Where it's covered |
|---|---|
| Customers view their transactions | `GET /api/v1/transactions`, the Transactions page (search, status and date filters, paging) |
| Customers dispute transactions | `POST /api/v1/disputes`, the Dispute page, enforced by the [dispute rules](#dispute-rules) |
| Historic view of disputed transactions | `GET /api/v1/disputes`, the My Disputes page and each dispute's status timeline |
| Production grade | [Production readiness](#production-readiness), [tests](#testing), [design decisions](#design-decisions) |
| Runnable Dockerfile | `Dockerfile` (API), the web repo's `Dockerfile` (nginx), `docker-compose.yml` for the full stack |
| README covering build, run and test | This file and the web app's README |
