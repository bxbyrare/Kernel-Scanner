# 💀 KERNEL SCANNER v1.0

![Logo](https://raw.githubusercontent.com/bxbyrare/Kernel-Scanner/main/iconpng)

> **[ FEITO POR X64 ]**  
> **[ DISCORD: @x64kernel ]**

O **Kernel Scanner** é uma ferramenta de auditoria de segurança e ataque avançada, desenvolvida para pentesters e pesquisadores de segurança que buscam rapidez e precisão. Com uma interface minimalista e poderosa, ele combina múltiplas técnicas de varredura em um único binário otimizado.

---

## ⚡ Principais Funcionalidades

| Módulo | Descrição | Nível de Risco Detectado |
| :--- | :--- | :--- |
| **🛡️ WAF Detection** | Identifica firewalls como Cloudflare, Akamai e ModSecurity. | Info |
| **🔑 Security Headers** | Analisa a ausência de CSP, HSTS, X-Frame-Options, etc. | Baixo |
| **🌐 CORS Checker** | Testa misconfigurações de Cross-Origin Resource Sharing. | Médio |
| **🧪 SSTI Test** | Injeção de Template (Jinja2, Mako, Twig) em parâmetros. | Crítico |
| **📊 GraphQL Hunt** | Busca endpoints expostos e testa Introspecção habilitada. | Alto |
| **🔍 PII Disclosure** | Varredura em tempo real por Emails, API Keys, AWS Keys e chaves privadas. | Médio |
| **📂 Brute Force** | Localiza diretórios administrativos e arquivos sensíveis (/admin, /env). | Médio |
| **💉 SQL Injection** | Detecção baseada em erros e tempo (Time-based SQLi). | Crítico |
| **🎨 XSS Scanner** | Scanner abrangente para Cross-Site Scripting Refletido. | Alto |
| **🔌 Port Scan** | Scanner de portas ultra rápido integrado. | Info |

---

## 🚀 Como Usar (Closed Source)

Para garantir a segurança do algoritmo original, o código fonte não está disponível publicamente. Siga os passos abaixo para baixar e rodar:

1. Vá até a aba [**Releases**](https://github.com/bxbyrare/Kernel-Scanner/releases) do lado direito desta página.
2. Baixe a versão mais recente do arquivo `KernelScanner_v1.exe`.
3. Execute o programa (é recomendado rodar como Administrador para o Port Scan funcionar perfeitamente).
4. Digite a URL do alvo e escolha o módulo de ataque desejado.

---

## 🎨 Design & Estética
O Kernel Scanner foi construído com foco na experiência do usuário via terminal:
- **Esquema de Cores:** Branco, Vermelho e Cinza Escuro (Estilo Hacker/Underground).
- **Banner ASCII:** Design exclusivo com efeito de textura.
- **Relatórios:** Exportação automática em JSON para análise posterior.

---

## ⚠️ Aviso Legal
Este software foi criado exclusivamente para fins educacionais e testes de penetração autorizados. O autor não se responsabiliza por qualquer uso indevido ou danos causados por esta ferramenta. **Use com responsabilidade.**

---

**Siga no Discord para atualizações:** `@x64kernel` 💀🔥
