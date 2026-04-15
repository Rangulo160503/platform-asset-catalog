# Platform Asset Catalog (Infrastructure Governance)

##  Overview

This repository implements a **declarative asset catalog** used to standardize and govern infrastructure across multiple environments.

Each asset is defined as a YAML file describing:

* Ownership (teams, stakeholders)
* Access control (roles and permissions)
* Environment configuration (multi-environment setup)
* Metadata for tagging, cost allocation, and governance

This catalog acts as a **source of truth** for infrastructure automation, enabling consistent provisioning and reducing configuration drift.

---

##  Problem It Solves

In large-scale environments, infrastructure is often:

* inconsistently configured
* poorly documented
* difficult to audit

This project addresses those issues by:

* enforcing a **standardized structure for assets**
* enabling **automation through structured metadata**
* improving **traceability and governance**

---

##  Architecture

This repository follows a **repository-as-catalog pattern**:

* YAML files represent **individual assets**
* Each file follows a defined schema
* Changes are managed through **Git workflows (PRs, reviews, validation)**

The catalog integrates with:

* Infrastructure-as-Code tools (Terraform / Terragrunt)
* CI/CD pipelines
* Cloud environments

---

##  Technologies

* YAML (declarative configuration)
* Git / GitHub
* GitHub Actions (CI validation)
* Jenkins (pipeline integration)
* Pre-commit hooks (linting and validation)
* Multi-environment cloud infrastructure
* HashiCorp Vault (optional secrets integration)

---

##  Structure

Each asset is defined as a YAML file:

```yaml
asset:
  name: example-asset
  infrastructure: false

  globalMetadata:
    lob: example-lob
    scrumTeam: example-team
    applicationGroup: example-group

  owners:
    stakeholders: []
    productOwners: []
    technicalExperts: []

  users:
    admins: []
    maintainers: []
    developers: []

  environments:
    dev:
      envType: dev
      accountId: "123456789"
```

---

##  Governance & Access Control

Each asset defines:

* **Admins** → full access across environments
* **Maintainers** → limited production access
* **Developers** → development-level access

This structure enables:

* controlled access to infrastructure
* secure environment separation
* consistent permission models

---

##  DevOps Workflow

* Changes are submitted via **Pull Requests**
* Validation is enforced using:

  * YAML linting
  * Pre-commit hooks
* CI pipelines validate structure before merge
* Assets are consumed by downstream automation (IaC pipelines)

---

##  Impact

This approach enables:

* Standardized infrastructure definitions
* Improved governance and compliance
* Better cost tracking through metadata
* Reduced configuration drift
* Faster onboarding for teams

---

##  Notes

* This repository does not deploy infrastructure directly
* It acts as a **configuration source** consumed by automation pipelines
* Sensitive data and internal identifiers have been removed for public use

---

##  Author

Ronald Angulo
Backend / DevOps Engineer
