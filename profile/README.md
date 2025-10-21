# Organization-wide .github


This repository provides **organization-level community health files** and
a suite of **reusable GitHub Actions** you can call from any repository in the org. Community health files 
here are automatically discovered by GitHub for repos that don’t override them.

Example .github/workflows/ci.yml inside a consumer repo:

```yml
name: CI
on: [push, pull_request]
jobs:
  dotnet:
    uses: ORG/.github/workflows/ci-dotnet.yml@main
    with:
      dotnet_version: "8.0.x"
  codeql:
    uses: ORG/.github/workflows/codeql-reusable.yml@main
    with:
      languages: csharp,javascript
```
Replace ORG with your GitHub organization handle and [YOUR‑DOMAIN] with your domain/email.
