# 🔐 Soluções para Segurança da Informação

## 🔥 Firewall
- **Barreira entre redes.**
- **Filtra o tráfego com base em regras.**
- Controla entrada/saída.
- Oculta detalhes da rede interna.
- Pode criar uma **DMZ** (zona desmilitarizada)
- ❗ Limitação: **não** detecta vírus nem ataques ocultos.
  - EXCEÇÃO: **recursos adicionais**, agem antes do antivírus
  - deep packet inspection
  - UTM
- Pode ser:
  - SW
  - SW e HW

## 🛡️ IDS (Intrusion Detection System)
- Detecta atividades suspeitas e invasões.
- Atua de forma **passiva**: apenas alerta.
- Pode ser:
  - HIDS (host-based)
  - NIDS (network-based)
  - Híbrido
- Técnicas:
  - Por assinatura
  - Por anomalia

## 🛑 IPS (Intrusion Prevention System)
- **Bloqueia ataques em tempo real**.
- Atua de forma **ativa**.
- Ex: encerra conexões, bloqueia IPs maliciosos.
- Diferença do IDS: não só alerta, **reage**.

## 📊 SIEM (Security Information and Event Management)
- Integra **monitoramento de eventos** com **análise de segurança**.
- Centraliza logs e gera alertas.
- Usa machine learning e correlação de eventos.
- Ajuda na resposta a incidentes e conformidade.

## 🌐 Proxy
- Intermediário entre estação e Internet.
- Filtra acessos (geralmente HTTP).
- Armazena páginas (cache).
- Pode bloquear categorias de sites.
- Ex: Squid Proxy.

## 👥 IAM (Identity and Access Management)
- **Gerencia identidades e permissões** de usuários.
- Controla quem pode acessar o quê, quando e como.
- Suporta autenticação multifator (MFA).
- Ex: Active Directory, Okta.

## 🔒 PAM (Privileged Access Management)
- Gerencia **acessos privilegiados** (ex: administradores).
- Monitora sessões críticas.
- Reduz riscos de abuso interno.
- Pode gravar sessões, aplicar senhas temporárias.

## 🛡️ Antivírus
- Detecta e remove malwares.
- Usa técnicas de:
  - Assinatura (padrões conhecidos)
  - Heurística (comportamento suspeito)
- Pode operar em tempo real.

## 📧 Antispam
- Filtra mensagens indesejadas ou maliciosas.
- Usa listas negras/brancas, filtros por conteúdo.
- Atua no gateway ou no servidor de e-mail.

## 🧠 UTM (Unified Threat Management)
- Solução unificada de segurança.
- Pode incluir:
  - Firewall
  - IDS/IPS
  - Antivírus
  - Antispam
  - VPN
