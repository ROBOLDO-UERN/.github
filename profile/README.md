<div align="center">

# 🤖 ROBOLDO — Ecossistema de Robótica Social (LAR / UERN)

**Laboratório de Automação e Robótica (LAR) • Universidade do Estado do Rio Grande do Norte (UERN)**  
*Educação • Acessibilidade (TEA/CAA) • Interação Humano-Robô (IHR) • Inteligência Artificial • Navegação Autônoma*

[![Painel Geral da Organização](https://img.shields.io/badge/🏛️_Project_%236-Central_Geral_de_Trabalhos-0969da?style=for-the-badge)](https://github.com/orgs/ROBOLDO-UERN/projects/6)
[![Governança & Cargos](https://img.shields.io/badge/👥_Governança-Professores_•_Bolsistas_•_Voluntários-6f42c1?style=for-the-badge)](https://github.com/ROBOLDO-UERN/.github/blob/main/GOVERNANCE.md)
[![Licença](https://img.shields.io/badge/Licença-GPL--3.0-2ea44f?style=for-the-badge)](https://github.com/ROBOLDO-UERN/Roboldo-Base/blob/master/LICENSE)
[![Localização](https://img.shields.io/badge/📍_Mossoró,_RN-LAR_/_UERN-d93f0b?style=for-the-badge)](https://github.com/ROBOLDO-UERN)

</div>

---

## 🏗️ Arquitetura Modular do Ecossistema Roboldo

O projeto **Roboldo** é dividido em **7 repositórios de subsistemas especializados**, coordenados pelo orquestrador central (**Orbit**) e validados continuamente por pipelines de **CI/CD** e **Branch Protection Rules**:

```mermaid
flowchart TB
    subgraph IHR["🎓 Camada de Interação, Jogos, Voz & Inteligência"]
        BASE["🎮 Roboldo-Base\n(Jogos Flutter, TEA/CAA & Lojinha)"]
        IAMOV["🧠 Roboldo-IA-Movimento\n(Python: STT/LLM, Piper TTS & SLAM v1/v2)"]
        NEXTION["🖥️ Roboldo-Display-Nextion\n(Tela HMI .HMI/.TFT, Rostos & Lipsync)"]
    end

    subgraph CORE["🌐 Núcleo Orquestrador"]
        ORBIT["🌐 Roboldo-Orbit\n(Controlador Geral, Core, Shell/Launcher, HAL & SDK)"]
    end

    subgraph HW["⚙️ Camada de Controle, IoT Embarcado & Engenharia Física"]
        CTRL["🐍 Controlador-Roboldo\n(Algoritmo Python: Cinemática & Serial/BT)"]
        IOT["🔌 Roboldo-IoT-Firmware\n(C/C++ Dual-ESP32: PID, Sensores de Toque & E-Stop)"]
        CAD["⚙️ Roboldo-Hardware-CAD\n(Modelagem CAD 3D, Chassi, Elétrica & BMS)"]
    end

    BASE <-->|"Roboldo SDK / Eventos"| ORBIT
    IAMOV <-->|"Comandos de Voz, IA & Navegação"| ORBIT
    ORBIT -->|"Sincronia Facial & Visemas"| NEXTION
    IAMOV -->|"Lipsync Piper TTS"| NEXTION
    ORBIT <-->|"HAL / Telemetria"| CTRL
    ORBIT <-->|"Serial / IoT"| IOT
    CTRL <-->|"Comandos de Juntas"| IOT
    IOT ---|"Montagem & Eletrônica"| CAD
```

---

## 🧩 Mapa de Repositórios, CI/CD Ao Vivo & Equipes Responsáveis (`CODEOWNERS`)

Cada parte do Roboldo possui seu próprio repositório com **Branch Protection** na branch principal, revisão automática por equipe (`CODEOWNERS`) e testes automatizados:

| Subsistema / Repositório | Stack Principal | Status CI/CD | Códigos de Trabalho | Equipes Responsáveis (`CODEOWNERS`) |
| :--- | :--- | :---: | :--- | :--- |
| 🌐 **[Roboldo-Orbit](https://github.com/ROBOLDO-UERN/Roboldo-Orbit)**<br><sub>Controlador Geral, Orquestrador Central, HAL, Shell e SDK</sub> | Python / Core / Multi | [![Orbit CI](https://github.com/ROBOLDO-UERN/Roboldo-Orbit/actions/workflows/ci.yml/badge.svg)](https://github.com/ROBOLDO-UERN/Roboldo-Orbit/actions) | `ORB-01` a `ORB-03` | `@zona-gamificacao-apps`<br>`@zona-mecanica-hardware`<br>`@professores` `@bolsistas` |
| 🔌 **[Roboldo-IoT-Firmware](https://github.com/ROBOLDO-UERN/Roboldo-IoT-Firmware)**<br><sub>IoT & Firmware Embarcado (Dual-ESP32, PID, Sensores de Toque, E-Stop)</sub> | C / C++ (PlatformIO / ESP32) | [![IoT CI](https://github.com/ROBOLDO-UERN/Roboldo-IoT-Firmware/actions/workflows/ci.yml/badge.svg)](https://github.com/ROBOLDO-UERN/Roboldo-IoT-Firmware/actions) | `IOT-01` a `IOT-03` | `@zona-mecanica-hardware`<br>`@professores` `@bolsistas` |
| 🐍 **[Controlador-Roboldo](https://github.com/ROBOLDO-UERN/Controlador-Roboldo)**<br><sub>Algoritmo de Controlador de Juntas/Braços e Serial/Bluetooth</sub> | Python (Pygame / PySerial) | [![Controlador CI](https://github.com/ROBOLDO-UERN/Controlador-Roboldo/actions/workflows/controlador-ci.yml/badge.svg)](https://github.com/ROBOLDO-UERN/Controlador-Roboldo/actions) | `CTRL-01` | `@zona-mecanica-hardware`<br>`@professores` `@bolsistas` |
| 🧠 **[Roboldo-IA-Movimento](https://github.com/ROBOLDO-UERN/Roboldo-IA-Movimento)**<br><sub>IA Conversacional (STT/LLM), Voz (Piper TTS) e Movimento/SLAM (v1.0 & v2.0)</sub> | Python (LLM / Piper / SLAM) | [![IA & Movimento CI](https://github.com/ROBOLDO-UERN/Roboldo-IA-Movimento/actions/workflows/ci.yml/badge.svg)](https://github.com/ROBOLDO-UERN/Roboldo-IA-Movimento/actions) | `SLAM-01..03`<br>`IA-01` • `VOZ-01` | `@zona-ia` `@zona-voz`<br>`@zona-slam`<br>`@professores` `@bolsistas` |
| 🎮 **[Roboldo-Base](https://github.com/ROBOLDO-UERN/Roboldo-Base)**<br><sub>Jogos Educativos em Flutter (*Roboldo Educa*, TEA/CAA), Mapa POIs & Lojinha</sub> | Flutter / Dart / Node / Python | [![Roboldo-Base CI](https://github.com/ROBOLDO-UERN/Roboldo-Base/actions/workflows/roboldo-ci-cd.yml/badge.svg)](https://github.com/ROBOLDO-UERN/Roboldo-Base/actions) | `JOGO-01..02`<br>`LOJA-01..04`<br>`APPS-01` • `SLAM-04` | `@zona-gamificacao-apps`<br>`@professores` `@bolsistas` |
| 🖥️ **[Roboldo-Display-Nextion](https://github.com/ROBOLDO-UERN/Roboldo-Display-Nextion)**<br><sub>Projeto da Tela Nextion/DWIN (`.HMI`/`.TFT`), Imagens de Rostos & Lipsync</sub> | Nextion HMI & Assets | [![Display CI](https://github.com/ROBOLDO-UERN/Roboldo-Display-Nextion/actions/workflows/ci.yml/badge.svg)](https://github.com/ROBOLDO-UERN/Roboldo-Display-Nextion/actions) | `DISP-01` | `@zona-voz` `@zona-ia`<br>`@zona-mecanica-hardware`<br>`@professores` |
| ⚙️ **[Roboldo-Hardware-CAD](https://github.com/ROBOLDO-UERN/Roboldo-Hardware-CAD)**<br><sub>Modelagem Mecânica CAD 3D (`.STEP`/`.STL`), Chassi, Elétrica & BOM</sub> | CAD 3D & KiCad | [![Hardware CAD CI](https://github.com/ROBOLDO-UERN/Roboldo-Hardware-CAD/actions/workflows/ci.yml/badge.svg)](https://github.com/ROBOLDO-UERN/Roboldo-Hardware-CAD/actions) | `HW-01` • `CAD-01` | `@zona-mecanica-hardware`<br>`@professores` `@bolsistas` |

---

## 🏛️ Gestão Centralizada na Organização (GitHub Projects)

As tasks e identificações de trabalhos **não ficam presas a um único repositório**: toda a gestão de pesquisa (TCCs, PIBIC, artigos e metas de desenvolvimento) ocorre nos **Projects da Organização**:

> 👉 **[Acessar Project #6 — ROBOLDO: Central Geral de Trabalhos & Subsistemas](https://github.com/orgs/ROBOLDO-UERN/projects/6)**  
> *Visão unificada de todas as 23 tasks com filtros por **Identificação do Trabalho**, **Subsistema / Parte**, **Zona de Projeto** e **Cargo**.*

| Zona / Grupo de Pesquisa | Escopo Técnico | Quadro da Zona na Organização | Team no GitHub |
| :--- | :--- | :--- | :--- |
| 🗺️ **Zona 1: SLAM & Navegação** | Mapeamento 2D (*Occupancy Grid*), fusão sensorial (LiDAR, Odometria e IMU), *Path Planning* e POIs. | [📋 Abrir Project Zona 1](https://github.com/orgs/ROBOLDO-UERN/projects/1) | `@ROBOLDO-UERN/zona-slam` |
| 🗣️ **Zona 2: Voz & Expressividade** | Síntese de voz neural offline (**Piper TTS** `pt-BR`), sincronia labial (*lipsync*), tela Nextion e rostos. | [📋 Abrir Project Zona 2](https://github.com/orgs/ROBOLDO-UERN/projects/2) | `@ROBOLDO-UERN/zona-voz` |
| 🧠 **Zona 3: Inteligência Artificial & IHR** | Conversação natural com IA (STT + LLM local/cloud), personalidade educativa do Roboldo e IHR. | [📋 Abrir Project Zona 3](https://github.com/orgs/ROBOLDO-UERN/projects/3) | `@ROBOLDO-UERN/zona-ia` |
| ⚙️ **Zona 4: Mecânica, Elétrica & Hardware** | Modelagem CAD 3D, elétrica/BMS, firmware IoT C/C++ (Dual-ESP32), controlador Python, toque e *E-Stop*. | [📋 Abrir Project Zona 4](https://github.com/orgs/ROBOLDO-UERN/projects/4) | `@ROBOLDO-UERN/zona-mecanica-hardware` |
| 🎮 **Zona 5: Gamificação, Apps & Lojinha** | Jogos educativos em Flutter (*Roboldo Educa*, TEA/CAA), controlador geral *Orbit*, SDK e **Lojinha**. | [📋 Abrir Project Zona 5](https://github.com/orgs/ROBOLDO-UERN/projects/5) | `@ROBOLDO-UERN/zona-gamificacao-apps` |

---

## 📋 Templates Oficiais para Novos Trabalhos (1-Click Setup)

Vai começar um novo módulo, algoritmo de pesquisa ou jogo para o Roboldo? Utilize um dos **Templates Oficiais da Organização** (já configurados com CI/CD, linters, `.gitignore` e `CODEOWNERS`):

| Template Oficial | Uso Recomendado | Status do Template |
| :--- | :--- | :---: |
| 🐍 **[`roboldo-template-python`](https://github.com/ROBOLDO-UERN/roboldo-template-python)** | Novos algoritmos em **Python** (IA, visão computacional, controle, voz ou SLAM) com `ruff` + `pytest`. | [![Template Python CI](https://github.com/ROBOLDO-UERN/roboldo-template-python/actions/workflows/ci.yml/badge.svg)](https://github.com/ROBOLDO-UERN/roboldo-template-python/actions) |
| 🔌 **[`roboldo-template-iot-cpp`](https://github.com/ROBOLDO-UERN/roboldo-template-iot-cpp)** | Novos firmwares **IoT em C/C++** (PlatformIO / ESP32 / Arduino) com análise estática `cppcheck` e build `pio run`. | [![Template IoT CI](https://github.com/ROBOLDO-UERN/roboldo-template-iot-cpp/actions/workflows/ci.yml/badge.svg)](https://github.com/ROBOLDO-UERN/roboldo-template-iot-cpp/actions) |
| 🎮 **[`roboldo-template-flutter-game`](https://github.com/ROBOLDO-UERN/roboldo-template-flutter-game)** | Novos **jogos educativos e apps em Flutter** prontos para publicação na **Lojinha do Roboldo** (`roboldo-app.json`). | [![Template Flutter CI](https://github.com/ROBOLDO-UERN/roboldo-template-flutter-game/actions/workflows/ci.yml/badge.svg)](https://github.com/ROBOLDO-UERN/roboldo-template-flutter-game/actions) |

---

## 👥 Estrutura de Cargos & Como Contribuir (Onboarding)

O laboratório organiza seus membros em três níveis integrados às **5 Zonas de Projetos** (detalhes em [`GOVERNANCE.md`](https://github.com/ROBOLDO-UERN/.github/blob/main/GOVERNANCE.md)):

| Cargo | Team da Organização | Permissão Base | Responsabilidade Principal |
| :--- | :--- | :--- | :--- |
| 🎓 **Professores** | `@ROBOLDO-UERN/professores` | `Admin` / `Maintain` | Coordenação geral, orientação científica, validação arquitetural e homologação de releases. |
| 🔬 **Bolsistas** | `@ROBOLDO-UERN/bolsistas` | `Write` / `Maintain` | Desenvolvimento dedicado, liderança técnica das Zonas, entregas de metas e revisão de PRs. |
| 🤝 **Voluntários** | `@ROBOLDO-UERN/voluntarios` | `Triage` / `Write` | Colaboração em tasks das Zonas, criação de jogos para a Lojinha, modelagem 3D, testes e documentação. |

### 🚀 Passo a Passo para Membros da Equipe:
1. **Escolha ou Crie seu Trabalho**: Acesse o **[Painel Geral da Organização (Project #6)](https://github.com/orgs/ROBOLDO-UERN/projects/6)** ou o Project da sua Zona e verifique o código da sua task (ex.: `IOT-03`, `JOGO-01`, `SLAM-02`).
2. **Crie uma Branch no Repositório do Subsistema**: Trabalhe em uma branch dedicada (`feat/nome-da-entrega` ou `fix/correcao`). A branch principal é protegida por **Branch Protection Rules**.
3. **Abra um Pull Request**: O GitHub acionará automaticamente o **CI/CD** da organização e solicitará a revisão da equipe responsável configurada no `CODEOWNERS`.

---

<div align="center">
  <sub>🏛️ <b>Laboratório de Automação e Robótica (LAR)</b> — <b>Universidade do Estado do Rio Grande do Norte (UERN)</b> • Mossoró, RN, Brasil</sub>
</div>
