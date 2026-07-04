💳 Digital Wallet & Loan Management System

Sistema full-stack de carteira digital com empréstimos, chat em tempo real e analytics financeiras.

⚠️ Realidade do projeto

Isto não é apenas um “app de carteira digital”. É um **mini-sistema bancário**.
Se for bem implementado, entra facilmente na categoria de projeto avançado de portfólio (Node.js + tempo real + regras financeiras + dados analíticos).

Mas também vou ser direto:
sem arquitetura bem feita, isto vira um **monólito confuso com Socket.IO e lógica espalhada**.

**🚀 Funcionalidades**

💰 Wallet Digital

* Gestão de saldo por utilizador
* Depósito e levantamento
* Histórico completo de transações
* Transferências internas entre contas

🏦 Sistema de Empréstimos

* Pedido de empréstimo por utilizador
* Fluxo de aprovação/rejeição (admin/banco)
* Liberação automática de fundos após aprovação
* Controlo de ciclo de vida do empréstimo


📉 Regras de Juros

* Juros base configuráveis por taxa
* Cálculo por tempo ativo do empréstimo
* Penalização por atraso:

  * Juros duplicam automaticamente

🔄 Motor de Transações

* Processamento em tempo real
* Validação de saldo antes de transferir
* Estados:

  * pending
  * success
  * failed
* Auditoria completa de operações

💬 Chat em Tempo Real

* Mensagens entre utilizadores
* WebSockets (Socket.IO)
* Estado online/offline
* Histórico persistente

📊 Dashboard Financeiro

* Visão geral de saldo
* Entradas vs saídas
* Status de empréstimos
* Gráficos interativos (Chart.js)


🔔 Sistema de Notificações

* Aprovação/rejeição de empréstimos
* Alertas de pagamento
* Avisos de atraso
* Confirmações de transação

🧠 Regras de Negócio

Fórmula de juros

```
Interest = Loan Amount × Rate × Time
```

### Penalização

```
Se atraso:
Interest = Interest × 2
```

---

Ciclo do empréstimo

1. Utilizador solicita empréstimo
2. Sistema valida critérios
3. Admin aprova/rejeita
4. Fundo é creditado na wallet
5. Pagamentos são rastreados
6. Juros são aplicados automaticamente
7. Penalização ativa se houver atraso


🧱 Stack

***Frontend***

* HTML5 / CSS3 / JavaScript
* Chart.js
* Socket.IO Client

***Backend***

* Node.js
* Express.js
* Socket.IO
* JWT Authentication

***Database***

* PostgreSQL


🔐 Segurança

* JWT para autenticação
* Hash de passwords (bcrypt)
* Validação de transações no backend (não no frontend)
* Rate limiting
* Logs de auditoria.
