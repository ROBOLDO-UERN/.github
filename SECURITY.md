# 🛡️ Política de Segurança — ROBOLDO (LAR / UERN)

## Segurança de Software, Credenciais e Hardware

O ecossistema **Roboldo** envolve tanto software conectado (Flutter, APIs Web, LLMs, Lojinha) quanto hardware físico (baterias, motores, sensores e ESP32).

### 1. Segredos e Chaves de API
- **NUNCA** envie arquivos `.env`, chaves de API (OpenAI, Gemini, Firebase), senhas de rede Wi-Fi do laboratório ou tokens privados para os repositórios públicos da organização `ROBOLDO-UERN`.
- Utilize sempre variáveis de ambiente (`.env` listado no `.gitignore`) ou **GitHub Organization/Repository Secrets** para pipelines de CI/CD.

### 2. Segurança Física e Elétrica do Robô
- Alterações em firmware de controle de motores, malha PID, BMS/baterias ou sensores antiqueda/colisão devem ser obrigatoriamente testadas em bancada com o botão físico de **Parada de Emergência (E-Stop)** ativo antes de testes em solo.

### 3. Como Reportar Vulnerabilidades
Caso identifique uma falha de segurança ou exposição acidental de credencial em qualquer repositório da organização `ROBOLDO-UERN`, comunique imediatamente a coordenação do **LAR / UERN** ou abra um alerta privado na aba **Security** do repositório correspondente.
