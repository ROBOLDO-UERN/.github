# 🤖 ROBOLDO — Laboratório de Automação e Robótica (LAR / UERN)

Bem-vindo à organização oficial do ecossistema **Roboldo** na **Universidade do Estado do Rio Grande do Norte (UERN)**.

O **Roboldo** é uma plataforma de robótica social interativa voltada para **educação, inclusão, acessibilidade (TEA/CAA), interação humano-robô (IHR) e navegação autônoma**.

---

## 🏛️ Gestão Centralizada na Organização (Tasks & Trabalhos)

Todas as tarefas, pesquisas (TCCs, PIBIC, artigos) e metas de desenvolvimento são gerenciadas **diretamente no nível da Organização** via **GitHub Projects**, integrando todos os repositórios dos subsistemas em um único fluxo:

👉 **[Acessar Painel Geral de Trabalhos & Subsistemas da Organização (Project #6)](https://github.com/orgs/ROBOLDO-UERN/projects/6)**

| Zona / Grupo de Pesquisa | Foco de Atuação | Quadro da Zona na Organização | Equipe Responsável (Team) |
| :--- | :--- | :--- | :--- |
| 🗺️ **Zona 1: SLAM & Navegação** | Mapeamento 2D (*Occupancy Grid*), fusão sensorial (LiDAR, Odometria e IMU), *Path Planning*, desvio de obstáculos e POIs. | [📋 Project Zona 1](https://github.com/orgs/ROBOLDO-UERN/projects/1) | `@ROBOLDO-UERN/zona-slam` |
| 🗣️ **Zona 2: Voz & Expressividade** | Síntese de voz neural offline (**Piper TTS** `pt-BR`), sincronia labial (*lipsync*), tela Nextion/DWIN, rostos e feedback sonoro. | [📋 Project Zona 2](https://github.com/orgs/ROBOLDO-UERN/projects/2) | `@ROBOLDO-UERN/zona-voz` |
| 🧠 **Zona 3: Inteligência Artificial & IHR** | Conversação natural com IA (STT + LLM local/cloud), personalidade educativa do Roboldo, emoções multimodais e IHR. | [📋 Project Zona 3](https://github.com/orgs/ROBOLDO-UERN/projects/3) | `@ROBOLDO-UERN/zona-ia` |
| ⚙️ **Zona 4: Mecânica, Elétrica & Hardware** | Modelagem CAD 3D, elétrica/BMS, IoT e firmware C/C++ (Dual-ESP32), sensores de toque, controle PID e segurança (*E-Stop*). | [📋 Project Zona 4](https://github.com/orgs/ROBOLDO-UERN/projects/4) | `@ROBOLDO-UERN/zona-mecanica-hardware` |
| 🎮 **Zona 5: Gamificação, Apps & Lojinha** | Jogos educativos em Flutter (*Roboldo Educa*, TEA/CAA), orquestrador *Orbit*, `Roboldo SDK`, Launcher e **Lojinha do Roboldo**. | [📋 Project Zona 5](https://github.com/orgs/ROBOLDO-UERN/projects/5) | `@ROBOLDO-UERN/zona-gamificacao-apps` |

---

## 🧩 Repositórios por Subsistema do Roboldo

Cada parte do projeto possui seu repositório dedicado com **CI/CD automatizado**, **CODEOWNERS** configurados e issues vinculadas aos **Projects da Organização**:

| Subsistema / Repositório | Tecnologia | Escopo & Trabalhos | Equipes Responsáveis (`CODEOWNERS`) |
| :--- | :--- | :--- | :--- |
| 🌐 **[Roboldo-Orbit](https://github.com/ROBOLDO-UERN/Roboldo-Orbit)** | Multi / Core | **Controlador Geral e Orquestrador Central**: Arquitetura modular (Core, HAL, Shell/Launcher) e SDK de comunicação entre todos os módulos do robô. | `@zona-gamificacao-apps` `@zona-mecanica-hardware` `@professores` `@bolsistas` |
| 🔌 **[Roboldo-IoT-Firmware](https://github.com/ROBOLDO-UERN/Roboldo-IoT-Firmware)** | C / C++ (ESP32 / PlatformIO) | **IoT & Sistemas Embarcados**: Firmware dos microcontroladores (Cabeça + Braços), controle cinemático/PID de motores, sensores de toque, telemetria IoT e *E-Stop*. | `@zona-mecanica-hardware` `@professores` `@bolsistas` |
| 🐍 **[Controlador-Roboldo](https://github.com/ROBOLDO-UERN/Controlador-Roboldo)** | Python (Pygame / PySerial) | **Algoritmo de Controlador em Python**: Interface de controle de juntas, cinemática de braços e comunicação serial/Bluetooth com o hardware. | `@zona-mecanica-hardware` `@professores` `@bolsistas` |
| 🧠 **[Roboldo-IA-Movimento](https://github.com/ROBOLDO-UERN/Roboldo-IA-Movimento)** | Python (LLM / Piper / SLAM) | **IA, Voz & Movimento (v1.0 & v2.0)**: Algoritmos em Python de conversação natural (STT/LLM), síntese de voz (Piper TTS), movimentação da v1.0 e navegação autônoma SLAM. | `@zona-ia` `@zona-voz` `@zona-slam` `@professores` `@bolsistas` |
| 🎮 **[Roboldo-Base](https://github.com/ROBOLDO-UERN/Roboldo-Base)** | Flutter / Dart / Node / Python | **Jogos em Flutter, Apps & Lojinha**: Jogos educativos (*Roboldo Educa — Perguntas e Respostas*, TEA/CAA), visualização de mapa/POIs, *RoboControl Studio* e Lojinha de Apps. | `@zona-gamificacao-apps` `@professores` `@bolsistas` |
| 🖥️ **[Roboldo-Display-Nextion](https://github.com/ROBOLDO-UERN/Roboldo-Display-Nextion)** | Nextion / DWIN HMI & Assets | **Tela, Imagens & Rostos**: Projetos da tela HMI (`.HMI` / `.TFT`), banco de imagens padronizadas das expressões faciais e sincronia labial (*lipsync*). | `@zona-voz` `@zona-ia` `@zona-mecanica-hardware` `@professores` |
| ⚙️ **[Roboldo-Hardware-CAD](https://github.com/ROBOLDO-UERN/Roboldo-Hardware-CAD)** | CAD 3D (STL / STEP) & KiCad | **Mecânica & Elétrica**: Modelagem 3D da estrutura física, chassi e suportes de sensores, diagramas elétricos, dimensionamento de energia e BOM. | `@zona-mecanica-hardware` `@professores` `@bolsistas` |

---

## 📋 Templates Oficiais para Novos Trabalhos (Com CI/CD Pronto)

Vai iniciar um novo trabalho, jogo ou módulo de pesquisa no Roboldo? Clique em **"Use this template"** em um dos nossos repositórios base já configurados com pipelines de CI/CD, linters e governança:

- 🐍 **[`roboldo-template-python`](https://github.com/ROBOLDO-UERN/roboldo-template-python)** — Template para novos algoritmos em Python (IA, visão, controle, voz ou navegação) com CI (`ruff` + `pytest`).
- 🔌 **[`roboldo-template-iot-cpp`](https://github.com/ROBOLDO-UERN/roboldo-template-iot-cpp)** — Template para novos projetos de IoT e firmware C/C++ (PlatformIO / ESP32 / Arduino) com compilação automática no GitHub Actions.
- 🎮 **[`roboldo-template-flutter-game`](https://github.com/ROBOLDO-UERN/roboldo-template-flutter-game)** — Template para novos jogos educativos e aplicativos em Flutter compatíveis com a **Lojinha do Roboldo** (`roboldo-app.json` + Flutter CI).

---

## 👥 Estrutura de Cargos e Governança

O projeto conta com três níveis de atuação integrados às **5 Zonas de Projetos**:

| Cargo | Team da Organização | Papel e Responsabilidade Principal |
| :--- | :--- | :--- |
| 🎓 **Professores** | `@ROBOLDO-UERN/professores` | Coordenação geral, orientação acadêmica/científica, validação arquitetural e aprovação de releases. |
| 🔬 **Bolsistas** | `@ROBOLDO-UERN/bolsistas` | Desenvolvimento dedicado, liderança técnica das Zonas, entregas de metas e revisão técnica de PRs. |
| 🤝 **Voluntários** | `@ROBOLDO-UERN/voluntarios` | Colaboração em tasks específicas das Zonas, criação de jogos/apps para a Lojinha, modelagem, testes e documentação. |

---

📍 **Mossoró, RN — Brasil** | 🏛️ **LAR / UERN**
