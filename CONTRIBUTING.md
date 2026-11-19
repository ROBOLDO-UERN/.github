# 🤝 Guia de Contribuição — Organização ROBOLDO-UERN

Bem-vindo(a) à organização **ROBOLDO - LAR / UERN**! Este guia vale para **todos os repositórios** da organização e orienta **Professores**, **Bolsistas** e **Voluntários** sobre como colaborar nos projetos.

---

## 🧭 1. Escolha sua Zona de Projeto e Cargo

Nossos projetos são divididos em **5 Zonas de Pesquisa & Desenvolvimento**:
1. 🗺️ **Zona 1: SLAM & Navegação Autônoma** (`zona: slam`)
2. 🗣️ **Zona 2: Voz & Expressividade** (`zona: voz`)
3. 🧠 **Zona 3: Inteligência Artificial & IHR** (`zona: ia`)
4. ⚙️ **Zona 4: Mecânica, Elétrica & Hardware** (`zona: mecanica-hardware`)
5. 🎮 **Zona 5: Gamificação, Apps & Lojinha** (`zona: gamificacao-apps`)

E em **3 Cargos**:
- 🎓 **Professores** (`cargo: professor`)
- 🔬 **Bolsistas** (`cargo: bolsista`)
- 🤝 **Voluntários** (`cargo: voluntario`)

---

## 🛠️ 2. Fluxo Padrão de Desenvolvimento (Git Flow Simplificado)

1. **Verifique ou Crie uma Issue**: Toda atividade deve estar registrada em uma Issue com sua respectiva **Zona** e **Cargo**.
2. **Crie uma Branch descritiva**:
   - `feat/nome-da-funcionalidade` (novos recursos)
   - `fix/descricao-da-correcao` (correção de bugs)
   - `docs/nome-da-documentacao` (diagramas, modelagem elétrica/mecânica, manuais)
   - `hw/subsistema` (esquemáticos, CAD 3D, firmware ESP32)
3. **Padrão de Commits (Conventional Commits)**:
   - `feat(slam): adiciona filtro EKF de odometria`
   - `fix(voz): corrige latência do Piper TTS`
   - `docs(eletrica): adiciona diagrama de barramentos de bateria`
4. **Abra um Pull Request**:
   - Preencha o template indicando a **Zona**, seu **Cargo** e a **Issue relacionada** (`Closes #ID`).
   - Aguarde a verificação automática do **CI/CD (GitHub Actions)** e a revisão de um Bolsista líder da Zona ou Professor orientador.
