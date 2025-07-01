# 🚀 GUIA COMPLETO: DEPLOY DIGITAL GARDEN

> **Status**: Git inicializado ✅ | Commit inicial feito ✅  
> **Próximo**: GitHub + Netlify deploy  
> **Tempo**: 15-20 minutos

## 📋 **STEP 2: CRIAR REPOSITÓRIO NO GITHUB**

### 1️⃣ **Acessar GitHub**
1. Acesse: https://github.com
2. Faça login na sua conta
3. Clique no botão **"+"** no canto superior direito
4. Selecione **"New repository"**

### 2️⃣ **Configurar Repositório**
- **Repository name**: `tcc-digital-garden-2025`
- **Description**: `TCC Multi-Agent Systems - Digital Garden | Framework DOE-LLM + ROI 5:1 Validado`
- **Visibility**: ✅ **Public** (para Netlify gratuito)
- **❌ NÃO marque**: "Add a README file" (já temos)
- **❌ NÃO marque**: "Add .gitignore" (já criamos)
- Clique **"Create repository"**

### 3️⃣ **Conectar Repositório Local**
Copie e execute estes comandos no terminal (substitua `SEU_USERNAME`):

```bash
# Adicionar remote origin
git remote add origin https://github.com/SEU_USERNAME/tcc-digital-garden-2025.git

# Renomear branch para main (padrão GitHub)
git branch -M main

# Push inicial
git push -u origin main
```

---

## 🌐 **STEP 3: DEPLOY NO NETLIFY**

### 1️⃣ **Preparar Netlify Configuration**
Vamos criar o arquivo de configuração do Netlify:

```toml
# netlify.toml
[build]
  publish = "/"
  command = "echo 'Static site ready'"

[build.environment]
  NODE_VERSION = "18"

[[headers]]
  for = "/*"
  [headers.values]
    X-Frame-Options = "DENY"
    X-XSS-Protection = "1; mode=block"
    X-Content-Type-Options = "nosniff"
    Referrer-Policy = "strict-origin-when-cross-origin"

[[redirects]]
  from = "/index.html"
  to = "/README"
  status = 301

[[redirects]]
  from = "/"
  to = "/README"
  status = 200
```

### 2️⃣ **Acessar Netlify**
1. Acesse: https://app.netlify.com
2. Faça login (pode usar conta GitHub)
3. Clique **"Add new site"** → **"Import an existing project"**

### 3️⃣ **Conectar GitHub**
1. Escolha **"Deploy with GitHub"**
2. Autorize Netlify a acessar seus repositórios
3. Busque e selecione: `tcc-digital-garden-2025`

### 4️⃣ **Configurar Deploy**
- **Branch**: `main`
- **Build command**: `echo 'Static site ready'`
- **Publish directory**: `/`
- Clique **"Deploy site"**

### 5️⃣ **Configurar Domínio (Opcional)**
1. Após deploy, vá em **"Site settings"**
2. **"Domain management"** → **"Options"** → **"Edit site name"**
3. Digite: `tcc-multi-agent-garden` (ou nome desejado)
4. Seu site ficará: `https://tcc-multi-agent-garden.netlify.app`

---

## 🔧 **STEP 4: INSTALAR PLUGIN DIGITAL GARDEN**

### 1️⃣ **No Obsidian**
1. **Settings** → **Community plugins** → **"Browse"**
2. Pesquise: **"Digital Garden"**
3. Instale o plugin by `oleeskild`
4. **Enable** o plugin

### 2️⃣ **Configurar Plugin**
1. **Settings** → **Digital Garden**
2. **GitHub repo**: `SEU_USERNAME/tcc-digital-garden-2025`
3. **GitHub username**: `SEU_USERNAME`
4. **GitHub token**: [Criar token GitHub](#github-token)
5. **Netlify site name**: `tcc-multi-agent-garden`
6. **Base URL**: `https://tcc-multi-agent-garden.netlify.app`

### 3️⃣ **Criar GitHub Token** {#github-token}
1. GitHub → **Settings** → **Developer settings**
2. **Personal access tokens** → **Tokens (classic)**
3. **"Generate new token (classic)"**
4. **Scopes**: ✅ `public_repo` (mínimo)
5. Copie o token e cole no plugin

---

## 📝 **STEP 5: CONFIGURAR NOTAS PARA PUBLICAÇÃO**

### 1️⃣ **Marcar Nota Home**
No arquivo `README.md`, adicione no YAML:
```yaml
dg-home: true
dg-pinned: true
```

### 2️⃣ **Verificar YAML de Todas as Notas**
Certifique-se que todas têm:
```yaml
dg-publish: true
```

### 3️⃣ **Publicar via Plugin**
1. Abra qualquer nota
2. **Ctrl+P** → **"Digital Garden: Publish Single Note"**
3. Ou use **"Digital Garden: Publish Multiple Notes"**

---

## 🎯 **TROUBLESHOOTING COMUM**

### ❌ **"Repository not found"**
**Solução**: Verificar se o repositório é público e o nome está correto

### ❌ **"Deploy failed"**
**Solução**: Verificar se o `netlify.toml` está na raiz do repositório

### ❌ **"GitHub token invalid"**
**Solução**: Gerar novo token com permissões corretas

### ❌ **"Site not updating"**
**Solução**: 
1. Verificar se commit foi feito
2. Netlify → **"Deploys"** → verificar status
3. Trigger manual deploy se necessário

---

## 🌟 **RESULTADO FINAL**

Após seguir todos os passos:

✅ **Site público**: `https://tcc-multi-agent-garden.netlify.app`  
✅ **Auto-deploy**: Cada commit = nova versão online  
✅ **HTTPS**: Certificado SSL automático  
✅ **CDN**: Performance global otimizada  

---

## 📞 **PRÓXIMOS PASSOS OPCIONAIS**

### 🎨 **Customizar Tema**
1. Netlify → **"Site configuration"** → **"Build & deploy"**
2. **Environment variables** → Add:
   - `THEME` = `dark`
   - `SITE_NAME` = `TCC Multi-Agent Systems`

### 📊 **Google Analytics**
1. Criar conta Google Analytics
2. Adicionar tracking ID nas configurações

### 🔍 **SEO Optimization**
1. Adicionar `sitemap.xml`
2. Configurar meta descriptions
3. Otimizar títulos das páginas

---

**🚀 Status**: Pronto para deploy!  
**⏱️ ETA**: 15-20 minutos execution  
**📈 Impact**: Democratização conhecimento científico online 