# 🐯 CTR — Sistema de Controle de Munição
## Clube de Tiro do Recôncavo

> Sistema web completo para gestão de munição, clientes e habitualidade do clube.
> Acesso pelo navegador — computador ou celular. Sem instalação.

---

## 📌 Acesso ao Sistema

| Modo | Como acessar |
|---|---|
| 🌐 Online (recomendado) | `https://seu-usuario.github.io/ctr-municao` |
| 💻 Offline | Abrir o arquivo `index.html` no Chrome |
| 📱 Celular como app | Abrir o link → 3 pontinhos → "Adicionar à tela inicial" |

---

## 🗂️ Estrutura — 7 Abas do Sistema

---

### 📊 Dashboard
Tela inicial com visão geral em tempo real.
- Total de munição em estoque
- Tipos de munição cadastrados
- Total de clientes
- Retiradas do dia
- Alertas de estoque baixo
- Últimas movimentações

---

### 🎯 Retirada
Registrar saída de munição para um cliente.

1. Selecionar o cliente
2. Confirmar a data
3. Clicar ➕ Adicionar Item (pode adicionar vários calibres de uma vez)
4. Selecionar munição e digitar quantidade
5. Clicar 🔴 Confirmar Retirada
6. O estoque é descontado automaticamente

**Retiradas por Dia:** abas clicáveis abaixo do formulário mostram quem retirou em cada dia.

---

### 📦 Estoque
Controle de entrada de munição.

1. Selecionar a munição (cadastrada em 🔫 Munições)
2. Digitar a quantidade recebida
3. Definir quantidade mínima para alerta
4. Clicar ✅ Registrar Entrada

Tabela mostra status colorido: 🟢 OK / 🟡 BAIXO / 🔴 ESGOTADO

---

### 🔫 Munições
Cadastro livre de qualquer tipo/calibre de munição.

| Campo | Exemplo |
|---|---|
| Nome | Pistola 9mm FMJ CBC 115gr |
| Calibre | 9mm / .40 / .380 / .38 SPL / 5.56 |
| Tipo de Ponta | FMJ / JHP / Chumbo / Frangível |
| Fabricante | CBC / Magtech / Fiocchi |
| Grão | 115 / 124 / 147 / 180 |
| Arma/Uso | Pistola / Revólver / Fuzil / Espingarda |
| Preço unitário | R$ 2,50 |

⚠️ Cadastre as munições ANTES de lançar no estoque ou retiradas.

---

### 👤 Clientes
Cadastro completo dos atiradores.

| Campo | Descrição |
|---|---|
| Nome Completo | Nome do atirador |
| CPF | Chave de identificação |
| Telefone / E-mail | Contato |
| Nº Sócio / Filiado | Número no clube |
| Vínculo | Afiliado / Visitante / Instrutor / Funcionário |

Clique em 👁️ para ver ficha completa com histórico de retiradas do cliente.

---

### 📋 Histórico
Todas as movimentações organizadas por mês, a partir de Maio/2025.

- Abas clicáveis por mês
- Cada mês mostra: entradas, saídas, saldo, clientes atendidos
- Agrupado por dia dentro do mês
- Filtro por tipo e por cliente
- Exportar CSV do mês selecionado

---

### 🏆 Habitualidade
Relatório de disparos por cliente — para lançar no sistema oficial do clube.

**Filtros:**
- 📅 Esta Semana — filtra semana atual automaticamente
- 📅 Este Mês — filtra mês completo
- Período personalizado (de/até)
- Busca por nome ou CPF

**O relatório mostra:**

| Coluna | Descrição |
|---|---|
| Nome Completo | Nome do atirador |
| CPF | Identificação |
| Nº Filiado | Número do sócio |
| Vínculo | Afiliado / Visitante |
| Sessões | Quantos dias atirou |
| Total Disparos | Total de munição retirada |
| Calibres | Quais calibres utilizou |
| Último Disparo | Data da última atividade |

**Exportar:** ⬇️ CSV (para qualquer sistema) ou 🖨️ Imprimir

---

### ⚙️ Configurações
- Alterar nome e sigla do clube
- Trocar logo (clique na onça no topo)
- Conectar ao Google Sheets (colar URL do Web App)
- Backup e restauração de dados

---

## ☁️ Google Sheets — Abas Criadas

| Aba | Conteúdo |
|---|---|
| 📦 Estoque | Inventário com status colorido |
| 🔫 Munições | Calibres cadastrados |
| 👤 Clientes | Todos os atiradores |
| 📋 Histórico | Todas as movimentações |
| 📊 Resumo Mensal | Totais mês a mês (Mai/2025 em diante) |
| 📅 Por Dia | Resumo diário |
| 🏆 Habitualidade | Relatório de disparos por atirador |

**Backups automáticos a cada sincronização:**
```
📁 Pasta do Clube (Drive)
   └── 📁 CTR - Clube de Tiro do Recôncavo
          📁 Sistema de Munição  ← index.html aqui
          📁 Backups             ← JSONs automáticos (últimos 10)
          📁 Exportações CSV     ← CSVs mensais
```

---

## 💾 Onde ficam os dados

| Local | O que salva |
|---|---|
| Navegador (localStorage) | Dados locais em tempo real |
| Google Sheets | Cópia sincronizada na nuvem |
| Google Drive | Backups JSON automáticos |

⚠️ Use sempre o mesmo navegador OU sincronize com o Google para não perder dados.

---

## 🔄 Fluxo de Uso Diário

```
1. Abrir o sistema
2. Cadastrar munição recebida    →  📦 Estoque
3. Registrar retiradas            →  🎯 Retirada
4. Final de semana               →  🏆 Habitualidade → Exportar CSV
5. Sincronizar tudo              →  ⚙️ Config → ☁️ Sincronizar
```

---

## 📁 Arquivos

| Arquivo | Função |
|---|---|
| `index.html` | Sistema completo — abre direto no navegador |
| `CTR_GoogleAppsScript.gs` | Cola no Apps Script do Google Sheets |
| `README.md` | Este manual |

---

*CTR — Clube de Tiro do Recôncavo · Versão 3.0 · Maio/2025*
