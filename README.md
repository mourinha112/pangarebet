# 🐎 Pangare Bet - Landing Page

Landing page premium para grupo VIP de sinais, mentoria e assessoria de investimentos em corridas de cavalos.

## 🚀 Tecnologias

- **Vite** - Build tool ultra-rápido
- **Vue 3** - Framework JavaScript progressivo
- **PrimeVue** - Biblioteca de componentes UI premium
- **PrimeIcons** - Ícones profissionais

## 📦 Instalação

```bash
npm install
```

## 💻 Desenvolvimento

```bash
npm run dev
```

Acesse: http://localhost:5173

## 🏗️ Build para Produção

```bash
npm run build
```

## 🌐 Deploy na Vercel

### Opção 1: Via Interface Web
1. Acesse [vercel.com](https://vercel.com)
2. Faça login ou crie uma conta
3. Clique em "Add New" → "Project"
4. Importe o repositório do GitHub
5. A Vercel detectará automaticamente que é um projeto Vite
6. Clique em "Deploy"

### Opção 2: Via CLI
```bash
# Instalar Vercel CLI
npm i -g vercel

# Deploy
vercel
```

## 📂 Estrutura

```
pangarebet/
├── public/
│   └── favicon.svg
├── src/
│   ├── App.vue          # Componente principal
│   ├── main.js          # Entrada do app
│   └── style.css        # Estilos globais
├── index.html
├── package.json
├── vercel.json          # Configuração Vercel
└── vite.config.js
```

## ✨ Features

- ✅ Design responsivo (mobile-first)
- ✅ Animações suaves
- ✅ Cores premium (dourado + preto)
- ✅ Seções: Hero, Serviços, Sobre, Depoimentos, CTA, Footer
- ✅ Integração WhatsApp e Telegram
- ✅ SEO otimizado
- ✅ Performance otimizada

## 🎨 Personalização

Para alterar cores, edite as variáveis CSS em `src/style.css`:

```css
:root {
  --gold-500: #D4AF37;
  --dark-800: #0D1117;
  /* ... outras variáveis */
}
```

## 📱 Contato

Edite os links de WhatsApp e Telegram em `src/App.vue`:

```vue
<a href="https://wa.me/SEU_NUMERO">...</a>
<a href="https://t.me/SEU_CANAL">...</a>
```

---

Feito com 💛 para Pangare Bet

