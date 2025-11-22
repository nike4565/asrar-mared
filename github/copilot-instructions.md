# Copilot Onboarding Instructions

This document provides guidance for Copilot coding agent to work efficiently with this repository.

---

## High Level Details

- **Repository Purpose:**  
  This is a Go-based service with a Ruby client for certain API endpoints. It ingests metered usage for GitHub and records that usage for billing and reporting.

- **Project Type & Languages:**  
  - Primary: Go (backend services, core logic)  
  - Secondary: Ruby (client implementation for API endpoints)  
  - Build system: `make` targets  
  - Protocol Buffers used in `proto/` directory  
  - CI/CD: GitHub Actions workflows run build, lint, test, and formatting checks

- **Repository Size:**  
  Medium-sized, with multiple subdirectories (`cmd/`, `internal/`, `lib/`, `ruby/`, etc.) and supporting configuration.

---

## Build & Validation Instructions

Always follow these steps to avoid build or test failures:

1. **Bootstrap / Setup**
   - Ensure Go (>=1.20) and Ruby (>=3.0) are installed.
   - Run `make fmt` before committing changes. This applies `gofmt` to all Go files.
   - Run `bundle install` inside `ruby/` if Ruby dependencies are updated.

2. **Build**
   - Run `make build` to compile Go binaries in `cmd/`.
   - This should always be run after `make fmt`.

3. **Test**
   - Run `make test` to execute unit tests.  
   - Tests are table-driven in Go and fixtures are in `testing/`.

4. **Lint & CI**
   - Run `make ci` for full validation (includes build, fmt, lint, test).  
   - This is the same sequence used in GitHub Actions.  
   - Always run `make ci` locally before pushing to avoid CI rejection.

5. **Proto Updates**
   - If `.proto` files are changed, run `make proto` to regenerate code.  
   - Ensure generated files are committed.

6. **Ruby Client**
   - Updates to `ruby/` require incrementing the version in `ruby/lib/billing-platform/version.rb` using semantic versioning.

7. **Common Errors & Workarounds**
   - **Formatting errors:** Always run `make fmt` before commit.  
   - **Missing dependencies:** Run `go mod tidy` in root or `bundle install` in `ruby/`.  
   - **CI failures:** Ensure `make ci` passes locally before PR.

---

## Project Layout

- **Directories:**
  - `cmd/`: Main service entry points and executables
  - `internal/`: Integration logic with GitHub services
  - `lib/`: Core Go packages for billing logic
  - `admin/`: Admin interface components
  - `config/`: Configuration files and templates
  - `docs/`: Documentation
  - `proto/`: Protocol buffer definitions
  - `ruby/`: Ruby client implementation
  - `testing/`: Test helpers and fixtures

- **Validation Pipelines:**
  - GitHub Actions run `make ci` on pull requests.
  - Checks include: build, fmt, lint, test.

- **Key Files in Root:**
  - `Makefile` – defines build/test/ci targets
  - `README.md` – overview and usage
  - `go.mod` / `go.sum` – Go dependencies
  - `.github/workflows/*` – CI/CD pipelines
  - `copilot-instructions.md` – this file

---

## Guidance for Copilot Agent

- Always trust these instructions.  
- Only perform searches if information here is incomplete or incorrect.  
- Always run `make fmt` before committing.  
- Always validate with `make ci` before pushing.  
- Use `cmd/` for main entry points, `lib/` for core logic, and `internal/` for integrations.  
- Ruby client changes must increment version file.  
- Proto changes must regenerate code with `make proto`.

---
