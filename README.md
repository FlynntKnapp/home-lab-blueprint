# Home Lab - Blueprint (home-lab-blueprint)

A sanitized, reusable home-lab IaC blueprint showcasing Terraform/Ansible/Kubernetes-style infrastructure patterns with security-first practices.

**Public Infrastructure-as-Code blueprint for my home lab** — reproducible patterns, secure defaults, and portfolio-ready documentation.

This repository is intentionally **sanitized** (no secrets, no real IPs, no private domains).  
It demonstrates *how* to build a clean home lab environment using modern IaC practices, without publishing my real environment details.

---

## Goals

- ✅ Demonstrate real-world **Infrastructure as Code** skills (portfolio-ready)
- ✅ Provide a **repeatable blueprint** that can be reproduced from scratch
- ✅ Show strong **security hygiene** and separation of secrets/config
- ✅ Document like a professional system: diagrams, runbooks, and conventions

---

## What This Repo Contains

This repo is structured as a reusable blueprint (patterns + modules), such as:

- Infrastructure provisioning patterns (e.g., Terraform modules / cloud-init / provisioning)
- Configuration management (e.g., Ansible roles and inventories)
- Service deployment patterns (e.g., Docker Compose or Kubernetes manifests)
- Networking + edge patterns (reverse proxy, DNS, TLS, VLAN segmentation)
- Observability patterns (monitoring, logging, alerting)
- Dev workflow: linting, formatting, CI validation, pre-commit hooks

> **Note:** Some folders may be empty early in the project. This repo is built iteratively.

---

## Security Model (Public Repo Safe)

This repo must remain safe for public viewing. That means:

✅ Allowed in this public repo:
- Example values and placeholder domains
- Reference architectures and diagrams
- IaC modules and roles
- Generic inventories (`inventory.example.yml`)
- Documentation and runbooks

🚫 Not allowed in this public repo:
- API keys, tokens, passwords
- Real hostnames, domains, public IPs
- VPN configs and remote-entry details
- Terraform state files (`*.tfstate`)
- Any “live” inventory values

---

## Repo Companion: Private Live Config

This blueprint is designed to work with a private companion repo:

- **`home-lab-live` (private):** real environment values + inventory + secrets references  
- **`home-lab-blueprint` (public):** sanitized patterns + reusable code + documentation

This separation mirrors professional infrastructure practices.

---

## Quick Start (Example / Non-Live)

> This section is the “hello world” workflow of the blueprint.
> Replace these steps as tooling solidifies (Terraform / Ansible / Docker / Kubernetes).

### Prerequisites
- Git
- Make (optional, but recommended)
- A Linux host (or WSL) for running automation tooling

### Clone
```bash
git clone https://github.com/FlynntKnapp/home-lab-blueprint.git
cd home-lab-blueprint
````

### Validate (placeholder example)

```bash
make validate
```

---

## Planned Roadmap

This repo will be developed in stages:

* [ ] Establish repo structure + conventions
* [ ] Add Terraform modules (core infrastructure patterns)
* [ ] Add Ansible roles (baseline hardening + service installs)
* [ ] Add container deployment patterns (Docker Compose)
* [ ] Add Kubernetes deployment patterns (optional)
* [ ] Add observability stack (monitoring + logging)
* [ ] Add CI checks (lint, validate, security scans)
* [ ] Add diagrams + runbooks for “rebuild from scratch”

---

## Repository Layout (Draft)

```text
home-lab-blueprint/
  docs/
  terraform/
  ansible/
  docker/
  k8s/
  scripts/
  .github/
```

---

## Documentation

* `docs/ARCHITECTURE.md` — High-level overview and diagram(s)
* `docs/SECURITY.md` — Threat model, separation of secrets, safe defaults
* `docs/RUNBOOKS/` — Runbooks for common operations (build, upgrade, recover)
* `docs/DECISIONS/` — Architecture decision records (ADR-style)

---

## Tooling (Expected)

This repo may include or migrate between tools as the blueprint matures:

* Terraform / OpenTofu
* Ansible
* Cloud-init / Packer (optional)
* Docker Compose
* Kubernetes (optional)
* CI validation (GitHub Actions)

---

## Conventions

### Naming

* Repos: kebab-case (example: `home-lab-blueprint`)
* Services: lower-case identifiers
* Environments: `dev`, `prod`, `lab`, etc.

### Secrets

Secrets never live in Git. This repo only contains `.example` files.

---

## License

This project may be licensed for learning and portfolio use.
(Choose MIT/Apache-2.0 or “All Rights Reserved” depending on your preference.)

---

## Author

**Flynnt Knapp**
Home lab + IaC portfolio work for learning, practice, and professional demonstration.
