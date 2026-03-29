# 🏫 Frequência Bolsa Família — PWA

Calculadora de frequência escolar para controle do **Bolsa Família** e **Pé-de-Meia**, desenvolvida para a EE Professora Malba Thereza Ferraz Campaner.

## ✨ Funcionalidades

- 📄 **Leitura automática de PDF** do Bolsa Família (extrai nome, NIS, turno)
- 🧮 **Cálculo anual ou por bimestre** com alertas de Bolsa Família e Pé-de-Meia
- 👥 **Gestão de alunos** com status: Ativo, Transferido, Formado
- 📤 **Exportação CSV** por status
- 📱 **PWA instalável** — funciona offline
- 🖨️ **Impressão de comprovantes** em PDF

## 🚀 Deploy no Vercel

### Opção 1 — Via GitHub (recomendado)

1. Crie um repositório no GitHub (ex: `frequencia-bolsa-familia`)
2. Faça upload de todos os arquivos desta pasta
3. Acesse [vercel.com](https://vercel.com) e clique em **"Add New Project"**
4. Importe o repositório do GitHub
5. O Vercel detecta o `vercel.json` automaticamente
6. Clique em **Deploy** ✅

### Opção 2 — Via Vercel CLI

```bash
npm i -g vercel
cd bolsa-familia-pwa
vercel --prod
```

## 📁 Estrutura do Projeto

```
bolsa-familia-pwa/
├── public/
│   ├── index.html          ← App principal
│   ├── manifest.json       ← Configuração PWA
│   ├── sw.js               ← Service Worker (cache offline)
│   ├── register-sw.js      ← Registro do Service Worker
│   └── icons/
│       ├── icon-192.png    ← Ícone PWA pequeno
│       └── icon-512.png    ← Ícone PWA grande
├── vercel.json             ← Configuração do Vercel
└── .gitignore
```

## ⚙️ Configurações do Vercel

O `vercel.json` configura:
- **outputDirectory**: `public/` (sem build necessário)
- **Cache do SW**: `no-cache` (sempre atualizado)
- **Cache de ícones**: 7 dias
- **SPA routing**: todas as rotas → `index.html`

## 📱 Instalar como App

**Android (Chrome):**
1. Abra o site no Chrome
2. Toque nos 3 pontinhos → "Adicionar à tela inicial"

**iOS (Safari):**
1. Abra o site no Safari
2. Toque em Compartilhar → "Adicionar à Tela de Início"

## 🔧 Desenvolvimento Local

Não precisa de servidor Node.js. Use qualquer servidor estático:

```bash
npx serve public
# ou
python3 -m http.server 3000 --directory public
```

## 📊 Regras de Frequência

| Benefício | Mínimo | Turno Manhã | Turno Tarde | Turno Noite |
|-----------|--------|-------------|-------------|-------------|
| Bolsa Família | 75% | 6 aulas/dia | 3 aulas/dia | 5 aulas/dia |
| Pé-de-Meia (Médio) | 80% | 6 aulas/dia | 3 aulas/dia | 5 aulas/dia |

---

Desenvolvido para a **EE Professora Malba Thereza Ferraz Campaner** · São José dos Campos, SP
