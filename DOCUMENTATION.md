# 📖 Guia de Documentação - Kernel Scanner v1.0

Este documento fornece instruções detalhadas sobre os requisitos, instalação e operação do **Kernel Scanner**.

---

## 🛠️ Requisitos do Sistema

### Para rodar o Executável (.exe)
- **SO:** Windows 10 ou superior.
- **Permissões:** Recomendado executar como **Administrador** (necessário para o Port Scanner funcionar com precisão).

### Para rodar o Script (.py)
- **Python:** Versão 3.8 ou superior.
- **Conectividade:** Acesso à internet para realizar as requisições HTTP aos alvos.

---

## 📦 Dependências (Apenas para Script Python)

Se você optar por rodar o código-fonte manualmente, instale as bibliotecas necessárias via Terminal/CMD:

```bash
pip install requests beautifulsoup4
```

*Nota: Se desejar recompilar o projeto com o ícone, também precisará do `Pillow` e `PyInstaller`.*

---

## 🚀 Como Utilizar (Passo a Passo)

### 1. Inicialização
Abra o programa. Ao iniciar, você verá o banner ASCII do **Kernel Scanner** e as informações do autor (@x64kernel).

### 2. Definir o Alvo
O sistema solicitará a URL alvo. 
- **Exemplo correto:** `https://exemplo.com` ou `http://192.168.1.1`
- *O scanner adicionará automaticamente `http://` caso você esqueça.*

### 3. Escolha do Módulo
Um menu numerado de **1 a 12** aparecerá:
- **Opção 1 (Scanner Completo):** Executa todas as verificações de uma vez (WAF, SQLi, XSS, etc.). Ideal para uma auditoria inicial rápida.
- **Opções Individuais (2-12):** Focam em uma vulnerabilidade específica para economizar tempo e evitar ruído no alvo.
- **Opção 0:** Encerra o programa com segurança.

### 4. Análise de Resultados
O scanner exibirá em tempo real no terminal:
- ⚪ **Branco:** Informações de progresso.
- 🔴 **Vermelho:** Vulnerabilidades encontradas ou alertas críticos.

### 5. Relatórios
Ao final de cada execução, o Kernel Scanner gera automaticamente um arquivo **JSON** na mesma pasta do programa.
- **Nome do arquivo:** `kernel_scan_[dominio]_[timestamp].json`
- Este arquivo pode ser aberto em qualquer editor de texto ou importado para outras ferramentas de análise.

---

## 🧪 Detalhes dos Módulos de Ataque

- **WAF Detection:** Verifica headers e tenta "provocar" o firewall para identificá-lo.
- **SQL Injection:** Testa diversos payloads (incluindo Time-based) em parâmetros de URL.
- **Sensitive Info Disclosure:** Busca por padrões de Emails, chaves de API do Google/AWS e chaves privadas SSH no código fonte.
- **Directory Brute Force:** Tenta acessar caminhos comuns como `/admin`, `/.env`, `/config` para encontrar arquivos expostos.

---

## ⚠️ Boas Práticas
- **Ética:** Use esta ferramenta apenas em sistemas onde você tenha autorização explícita para testar.
- **WAF:** Alguns módulos podem ser bloqueados se o site tiver proteções agressivas. Recomenda-se usar o módulo de Detecção de WAF primeiro.

---

> **Suporte & Atualizações:**  
> 💀 **Discord:** `@x64kernel`  
> 💻 **GitHub:** [bxbyrare/Kernel-Scanner](https://github.com/bxbyrare/Kernel-Scanner)
