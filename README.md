# Solana AI Trader — Deploy no Vercel

## O que este projeto faz
- Conecta com sua Phantom Wallet
- Busca preços reais de SOL, BTC e ETH via Jupiter DEX
- IA (Claude) analisa o mercado e recomenda COMPRAR, VENDER ou AGUARDAR
- Executa swaps reais na blockchain Solana via Jupiter DEX
- Você sempre aprova cada transação na Phantom

---

## Passo a passo para colocar no ar

### 1. Instale o Node.js
Baixe em: https://nodejs.org (versão LTS)

### 2. Instale o Vercel CLI
Abra o terminal e rode:
```
npm install -g vercel
```

### 3. Instale as dependências do projeto
Na pasta do projeto:
```
npm install
```

### 4. Faça login no Vercel
```
vercel login
```
(Crie uma conta grátis em vercel.com se não tiver)

### 5. Configure as variáveis de ambiente
No site do Vercel (vercel.com), vá em:
Settings → Environment Variables

Adicione:
- Nome: `ANTHROPIC_API_KEY`
- Valor: sua chave da API da Anthropic (https://console.anthropic.com)

### 6. Faça o deploy
```
vercel --prod
```

Pronto! O Vercel vai te dar um link como:
`https://solana-ai-trader.vercel.app`

---

## Estrutura do projeto
```
solana-ai-trader/
├── api/
│   ├── analyze.js   — IA analisa o mercado (usa Claude)
│   ├── quote.js     — Busca cotação no Jupiter DEX
│   ├── swap.js      — Monta transação de swap
│   └── price.js     — Busca preços reais dos tokens
├── public/
│   └── index.html   — Interface principal
├── package.json
└── vercel.json
```

---

## Aviso importante
Este projeto realiza transações REAIS na blockchain Solana.
Sempre teste com valores pequenos primeiro.
Nunca invista mais do que pode perder.
