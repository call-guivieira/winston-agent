# Winston — Content Agent

Gerador de conteúdo editorial para a Call Winston.
Gera case completo, legenda de Instagram e post de LinkedIn — PT + EN — a partir de campos manuais, PDFs e imagens.

---

## Deploy em 5 passos

### 1. Crie uma conta no GitHub
Acesse https://github.com e crie uma conta gratuita se ainda não tiver.

### 2. Crie um repositório novo
- Clique em "New repository"
- Nome: `winston-agent`
- Deixe como Public
- Clique em "Create repository"

### 3. Suba os arquivos
Arraste os seguintes arquivos/pastas para o repositório pelo browser:
```
api/
  generate.js
public/
  index.html
vercel.json
```

Ou, se tiver Git instalado:
```bash
git init
git add .
git commit -m "primeiro commit"
git remote add origin https://github.com/SEU_USUARIO/winston-agent.git
git push -u origin main
```

### 4. Deploy no Vercel
- Acesse https://vercel.com e crie conta com o GitHub
- Clique em "Add New Project"
- Selecione o repositório `winston-agent`
- Clique em "Deploy" — sem mudar nada

### 5. Configure a API Key
Após o deploy:
- Vá em Settings → Environment Variables
- Clique em "Add"
- Name: `ANTHROPIC_API_KEY`
- Value: sua chave (começa com `sk-ant-api03-`)
- Clique em Save
- Vá em Deployments → clique nos três pontinhos → "Redeploy"

Pronto. O agente vai estar em `https://winston-agent.vercel.app` (ou o nome que você escolheu).

---

## Custo estimado

Cada geração completa (Case + Instagram + LinkedIn) usa ~2.000-3.000 tokens de saída.
Com Claude Sonnet 4: aproximadamente R$ 0,10–0,20 por geração.

---

## Estrutura do projeto

```
winston-agent/
├── api/
│   └── generate.js     # Proxy para a API do Anthropic (resolve CORS)
├── public/
│   └── index.html      # Interface do agente
└── vercel.json         # Configuração de rotas
```

---

*Call Winston — callwinston.me — Based in Americana, working worldwide.*
