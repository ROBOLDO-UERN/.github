# 🤖 ROBOLDO — Laboratório de Automação e Robótica (LAR / UERN)

Bem-vindo à organização oficial do projeto **Roboldo** na **Universidade do Estado do Rio Grande do Norte (UERN)**.

O **Roboldo** é uma plataforma de robótica social interativa voltada para **educação, inclusão, acessibilidade, interação humano-robô (IHR) e navegação autônoma**.

---

## 🧭 Zonas de Projetos (Grupos de Pesquisa & Desenvolvimento)

O ecossistema do Roboldo é organizado em **5 Zonas de Projetos** multidisciplinares (acompanhadas via [Milestones](https://github.com/ROBOLDO-UERN/Roboldo-Base/milestones) e [Labels de Zona](https://github.com/ROBOLDO-UERN/Roboldo-Base/labels) no repositório central):

| Zona / Grupo | Foco de Atuação | Painel de Tasks (Milestone) | Label de Filtro |
| :--- | :--- | :--- | :--- |
| 🗺️ **Zona 1: SLAM & Navegação** | Mapeamento 2D (*Occupancy Grid*), fusão sensorial (LiDAR, Odometria e IMU), *Path Planning*, desvio de obstáculos e POIs. | [Ver Tasks da Zona 1](https://github.com/ROBOLDO-UERN/Roboldo-Base/milestone/1) | [`zona: slam`](https://github.com/ROBOLDO-UERN/Roboldo-Base/issues?q=is%3Aopen+label%3A%22zona%3A+slam%22) |
| 🗣️ **Zona 2: Voz & Expressividade** | Síntese de voz neural offline (**Piper TTS** `pt-BR`), sincronia labial (*lipsync* no display DWIN e Avatar Flutter), normalização de rostos e feedback sonoro. | [Ver Tasks da Zona 2](https://github.com/ROBOLDO-UERN/Roboldo-Base/milestone/2) | [`zona: voz`](https://github.com/ROBOLDO-UERN/Roboldo-Base/issues?q=is%3Aopen+label%3A%22zona%3A+voz%22) |
| 🧠 **Zona 3: Inteligência Artificial & IHR** | Conversação natural com IA (STT + LLM local/cloud), personalidade educativa do Roboldo, emoções multimodais e interação humano-robô. | [Ver Tasks da Zona 3](https://github.com/ROBOLDO-UERN/Roboldo-Base/milestone/3) | [`zona: ia`](https://github.com/ROBOLDO-UERN/Roboldo-Base/issues?q=is%3Aopen+label%3A%22zona%3A+ia%22) |
| ⚙️ **Zona 4: Mecânica, Elétrica & Hardware** | Modelagem CAD 3D e estrutura física, modelagem elétrica e BMS, arquitetura Dual-ESP32 (Cabeça + Braços), sensores de toque, cinemática/PID de motores e segurança física (*E-Stop*). | [Ver Tasks da Zona 4](https://github.com/ROBOLDO-UERN/Roboldo-Base/milestone/4) | [`zona: mecanica-hardware`](https://github.com/ROBOLDO-UERN/Roboldo-Base/issues?q=is%3Aopen+label%3A%22zona%3A+mecanica-hardware%22) |
| 🎮 **Zona 5: Gamificação, Apps & Lojinha** | Projetos de gamificação educacional e inclusiva (TEA/CAA, *Roboldo Educa — Perguntas e Respostas*), novos Apps Core, `Roboldo SDK`, Launcher e **Lojinha do Roboldo**. | [Ver Tasks da Zona 5](https://github.com/ROBOLDO-UERN/Roboldo-Base/milestone/5) | [`zona: gamificacao-apps`](https://github.com/ROBOLDO-UERN/Roboldo-Base/issues?q=is%3Aopen+label%3A%22zona%3A+gamificacao-apps%22) |

---

## 👥 Estrutura de Cargos da Equipe

O projeto conta com três níveis de atuação integrados às **5 Zonas de Projetos** (detalhados em [`GOVERNANCE.md`](https://github.com/ROBOLDO-UERN/Roboldo-Base/blob/master/GOVERNANCE.md)):

| Cargo | Team da Organização | Filtro de Tasks por Cargo | Responsabilidade Principal |
| :--- | :--- | :--- | :--- |
| 🎓 **Professores** | `@ROBOLDO-UERN/professores` | [`cargo: professor`](https://github.com/ROBOLDO-UERN/Roboldo-Base/issues?q=is%3Aopen+label%3A%22cargo%3A+professor%22) | Coordenação geral, orientação acadêmica/científica, validação arquitetural e aprovação de releases. |
| 🔬 **Bolsistas** | `@ROBOLDO-UERN/bolsistas` | [`cargo: bolsista`](https://github.com/ROBOLDO-UERN/Roboldo-Base/issues?q=is%3Aopen+label%3A%22cargo%3A+bolsista%22) | Desenvolvimento dedicado, liderança técnica das Zonas, entregas de metas e apoio na revisão de PRs. |
| 🤝 **Voluntários** | `@ROBOLDO-UERN/voluntarios` | [`cargo: voluntario`](https://github.com/ROBOLDO-UERN/Roboldo-Base/issues?q=is%3Aopen+label%3A%22cargo%3A+voluntario%22) | Colaboração em tasks específicas das Zonas, criação de apps para a Lojinha, modelagem, testes e documentação. |

---

## 📦 Repositórios Centrais

| Repositório | Descrição | Licença |
| :--- | :--- | :--- |
| **[Roboldo-Base](https://github.com/ROBOLDO-UERN/Roboldo-Base)** | Repositório principal do ecossistema: App Flutter (*Roboldo Educa*), *RoboControl Studio* (`ambiente-configuracao`), SDK e [Central de Zonas e Issues](https://github.com/ROBOLDO-UERN/Roboldo-Base/milestones). | `GPL-3.0` |
| **[Controlador-Roboldo](https://github.com/ROBOLDO-UERN/Controlador-Roboldo)** | Firmware e códigos de controle embarcado dos microcontroladores do Roboldo. | `GPL-3.0` |

---

📍 **Mossoró, RN — Brasil** | 🏛️ **LAR / UERN**
