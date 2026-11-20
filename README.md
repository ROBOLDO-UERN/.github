# ⚙️ `.github` — Padrões Globais, Governança e Reusable CI/CD (`ROBOLDO-UERN`)

Este repositório centraliza a identidade visual, governança, templates globais de Issues/Pull Requests e workflows reutilizáveis de **CI/CD** de todos os repositórios da organização **[ROBOLDO-UERN](https://github.com/ROBOLDO-UERN)**.

## 📂 Estrutura deste Repositório

- [`profile/README.md`](./profile/README.md) — Página inicial pública exibida no perfil da organização [`github.com/ROBOLDO-UERN`](https://github.com/ROBOLDO-UERN).
- [`GOVERNANCE.md`](./GOVERNANCE.md) — Estrutura de cargos (`Professores`, `Bolsistas`, `Voluntários`), permissões e mapa de `CODEOWNERS` por subsistema.
- [`CONTRIBUTING.md`](./CONTRIBUTING.md) & [`CODE_OF_CONDUCT.md`](./CODE_OF_CONDUCT.md) — Diretrizes de contribuição e código de conduta do LAR / UERN.
- [`ISSUE_TEMPLATE/`](./ISSUE_TEMPLATE/) — Templates globais de criação de tasks com seleção de **Subsistema**, **Zona**, **Cargo** e **Identificação do Trabalho**, integrados ao **[Project #6 da Organização](https://github.com/orgs/ROBOLDO-UERN/projects/6)**.
- [`PULL_REQUEST_TEMPLATE.md`](./PULL_REQUEST_TEMPLATE.md) — Checklist padrão de qualidade para Pull Requests em qualquer repositório do Roboldo.
- [`.github/workflows/`](./.github/workflows/) — **Reusable Workflows** chamados pelos repositórios dos subsistemas:
  - `reusable-python-ci.yml` (Python: `compileall`, `ruff` e `pytest`)
  - `reusable-cpp-iot-ci.yml` (C/C++ & IoT: `cppcheck` e compilação PlatformIO)
  - `reusable-flutter-ci.yml` (Flutter: `flutter pub get`, `flutter analyze` e `flutter test`)
  - `reusable-assets-cad-ci.yml` (Display Nextion & Hardware CAD: auditoria de documentação e assets)
