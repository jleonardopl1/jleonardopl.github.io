# 🚀 Guia de Deploy — GitHub Pages
**Publicar seu portfólio online em 10 minutos. Zero conhecimento técnico necessário.**

---

## O que você vai ter no final

✅ URL pública: `https://SEU_USUARIO.github.io/portfolio`
✅ Portfólio acessível por qualquer pessoa no mundo
✅ Link para colocar no LinkedIn
✅ Atualizações automáticas sempre que você editar o arquivo
✅ Custo: **R$ 0,00**

---

## PASSO 1 — Criar o repositório no GitHub

1. Acesse **[github.com](https://github.com)** e faça login
2. Clique no botão **"+"** no canto superior direito
3. Selecione **"New repository"**
4. Preencha:
   - **Repository name:** `portfolio`
   - **Description:** `Portfólio profissional — Data Analyst & BI`
   - Marque: ✅ **Public**
   - Marque: ✅ **Add a README file**
5. Clique em **"Create repository"**

---

## PASSO 2 — Fazer upload dos arquivos

1. No seu repositório recém-criado, clique em **"Add file"** → **"Upload files"**
2. Arraste ou selecione os seguintes arquivos:
   - `index.html` ← **obrigatório** (este é o seu portfólio)
   - `README.md` ← substitui o README criado automaticamente
   - `DESIGN_SYSTEM.md` ← documentação técnica
   - `DEPLOY_GUIDE.md` ← este arquivo
3. No campo **"Commit changes"**, escreva:
   ```
   feat: portfólio inicial v1.0
   ```
4. Clique em **"Commit changes"**

---

## PASSO 3 — Ativar o GitHub Pages

1. No seu repositório, clique em **"Settings"** (aba no topo)
2. No menu lateral esquerdo, clique em **"Pages"**
3. Em **"Source"**, selecione:
   - Branch: **`main`**
   - Folder: **`/ (root)`**
4. Clique em **"Save"**
5. Aguarde **2–5 minutos**
6. Uma mensagem aparecerá:
   > ✅ *Your site is live at `https://SEU_USUARIO.github.io/portfolio`*

---

## PASSO 4 — Colocar o link no LinkedIn

1. Acesse seu perfil no LinkedIn
2. Clique em **"Editar perfil"** (lápis)
3. Role até a seção **"Destaque"** ou **"Links"**
4. Clique em **"Adicionar link"** ou **"+"**
5. Cole a URL: `https://SEU_USUARIO.github.io/portfolio`
6. Título: `Portfólio — Data Analytics & BI`
7. Salve

> 💡 **Dica pro:** No LinkedIn, você também pode adicionar o link na seção **"Sobre"** e no campo **"Site"** do perfil. Quanto mais visível, melhor.

---

## Como ATUALIZAR o portfólio no futuro

Quando quiser atualizar seu portfólio (adicionar projeto, corrigir texto, etc.):

### Opção A — Pelo navegador (mais fácil)

1. Acesse **github.com/SEU_USUARIO/portfolio**
2. Clique no arquivo `index.html`
3. Clique no ícone de **lápis** (Edit this file)
4. Faça as alterações diretamente no navegador
5. Role para baixo, escreva uma mensagem como:
   ```
   feat: adiciona projeto Capex Dashboard
   ```
6. Clique em **"Commit changes"**
7. Aguarde 2 minutos → o site atualiza automaticamente ✅

### Opção B — Fazer upload de nova versão

1. Edite o `index.html` no seu computador
2. Acesse github.com/SEU_USUARIO/portfolio
3. Clique em `index.html` → clique nos **3 pontos** → **"Delete file"**
4. Confirme o delete com um commit
5. Clique em **"Add file"** → **"Upload files"**
6. Suba a nova versão do `index.html`
7. Commit → site atualiza em 2 minutos ✅

---

## Como nomear seus commits (versionamento)

Use este padrão para manter um histórico organizado:

```
feat: adiciona projeto Capex Dashboard        ← nova funcionalidade/projeto
fix: corrige gráfico de forecast              ← correção de bug/erro
update: atualiza dados de 2024                ← atualização de dados
style: ajusta cores dos cards de habilidades  ← mudança visual
docs: atualiza README                         ← documentação
```

---

## Histórico de Versões

| Versão | Data | O que mudou |
|---|---|---|
| v1.0 | Fev/2025 | Lançamento — Portfólio inicial com Revolução Verde 2.0 |
| v1.1 | *(a definir)* | Dashboard Capex — Louis Dreyfus |
| v1.2 | *(a definir)* | Análise de Rebates — Agro Amazônia |
| v2.0 | *(a definir)* | Responsividade mobile completa |

---

## Domínio personalizado (opcional, futuro)

Se um dia quiser ter uma URL como `jonasleondardo.com.br`:

1. Compre o domínio no **Registro.br** (~R$ 40/ano)
2. No GitHub Pages Settings → **"Custom domain"** → cole seu domínio
3. Configure o DNS no Registro.br conforme instruções do GitHub
4. Aguarde até 24h para propagar

Não é necessário agora. O GitHub Pages gratuito já é mais do que suficiente.

---

## Solução de problemas comuns

| Problema | Solução |
|---|---|
| Site não atualiza | Aguarde 5 min e force refresh: `Ctrl + Shift + R` |
| Gráficos não aparecem | Verifique conexão — Chart.js carrega via CDN |
| URL retorna 404 | Verifique se o arquivo se chama exatamente `index.html` |
| Fontes não carregam | Verifique conexão — Google Fonts carrega via CDN |

---

## Suporte

Se travar em algum passo, abra uma **Issue** no repositório ou entre em contato:
📧 jleonardopl@gmail.com

---

*Guia criado para Jonas Leonardo · Portfolio v1.0 · Fevereiro 2025*
