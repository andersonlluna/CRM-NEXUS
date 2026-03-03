# Nexus CRM Dashboard
Dashboard de CRM hospedado no GitHub Pages. Atualização semanal via CSV.

---

## 📁 Estrutura do Projeto

```
nexus-crm/
├── index.html   → Dashboard (não precisa editar)
├── dados.csv    → Seus dados (edite toda semana)
└── README.md    → Este arquivo
```

---

## 🚀 Deploy no GitHub Pages (primeira vez)

### 1. Crie o repositório
- Acesse https://github.com/new
- Nome: `nexus-crm` (ou outro de sua preferência)
- Marque como **Public**
- Clique em **Create repository**

### 2. Suba os arquivos
Na tela do repositório criado, clique em **"uploading an existing file"**:
- Arraste os 3 arquivos: `index.html`, `dados.csv`, `README.md`
- Clique em **Commit changes**

### 3. Ative o GitHub Pages
- Vá em **Settings** → **Pages** (menu lateral esquerdo)
- Em **Source**, selecione `Deploy from a branch`
- Em **Branch**, selecione `main` e pasta `/ (root)`
- Clique em **Save**

### 4. Acesse seu dashboard
Após 1-2 minutos, seu link será:
```
https://SEU_USUARIO.github.io/nexus-crm/
```

---

## 📅 Atualização Semanal (todo semana)

### Edite o arquivo dados.csv diretamente no GitHub:

1. Acesse seu repositório
2. Clique no arquivo `dados.csv`
3. Clique no ícone de **lápis** (editar) no canto superior direito
4. Adicione as linhas da nova semana no final do arquivo
5. Clique em **Commit changes**
6. Em ~1 minuto o dashboard já estará atualizado!

---

## 📊 Formato do CSV

```
SEMANA,CLIENTE,SEGMENTO,VALOR,STATUS,RESPONSAVEL,DATA
```

| Coluna       | Descrição                          | Exemplo           |
|--------------|------------------------------------|-------------------|
| SEMANA       | Número da semana (1, 2, 3...)      | `7`               |
| CLIENTE      | Nome do cliente                    | `Empresa ABC`     |
| SEGMENTO     | Tipo de cliente                    | `Enterprise`      |
| VALOR        | Valor do negócio (só números)      | `45000`           |
| STATUS       | Status atual (ver opções abaixo)   | `Fechado`         |
| RESPONSAVEL  | Nome do responsável                | `Anderson`        |
| DATA         | Data no formato DD/MM/AAAA         | `10/03/2026`      |

### Status disponíveis:
- `Fechado` → negócio ganho ✅
- `Perdido` → negócio perdido ❌
- `Proposta` → proposta enviada 📄
- `Negociação` → em negociação 🔄

### Exemplo de nova semana (Semana 7):
```
7,Nova Empresa SA,Enterprise,78000,Fechado,Anderson,10/03/2026
7,Tech Startup,Startup,12500,Proposta,Carlos,10/03/2026
7,Distribuidora X,SMB,19800,Perdido,Marina,10/03/2026
7,Grupo Industrial,Mid-Market,55000,Negociação,Anderson,10/03/2026
```

---

## ✨ O que o dashboard calcula automaticamente

- **Receita total** por semana e comparação com semana anterior
- **Taxa de conversão** (Fechados ÷ Fechados + Perdidos)
- **Ticket médio** dos negócios fechados
- **Gráfico de barras** de todas as semanas
- **Distribuição por status** (pipeline)
- **Top clientes** por receita acumulada
- **Seletor de semanas** para filtrar o período

---

## 🎨 Personalização rápida

No arquivo `index.html`, linha 7–8:
```html
<div class="logo-text">Nexus</div>      ← Nome do sistema
<div class="logo-sub">CRM Platform</div> ← Subtítulo
```

Linha do usuário (~360):
```html
<div class="user-name">Anderson Luna</div>  ← Seu nome
<div class="user-role">Admin · Gestor</div>  ← Seu cargo
```
