# Método Cria Quiz - Deployment

Sistema de coleta de dados para o Método Cria. O quiz identifica em que ponto os empreendedores digitais estão "travados".

## 📋 O que é

- Quiz com 6 perguntas
- Coleta: Nome, Email, WhatsApp
- Dados salvos no Supabase
- Design premium (ouro/preto)
- 100% funcional ✅

## 🚀 Deployment Rápido

### Opção 1: Railway (Recomendado)

1. Crie um novo projeto em [railway.app](https://railway.app)
2. Selecione "Deploy from GitHub"
3. Conecte este repositório
4. Configure as variáveis de ambiente:
   - `PORT=3000` (já padrão)
5. Deploy automático!

Exemplo URL final:
```
https://seu-projeto.railway.app
```

### Opção 2: Vercel

```bash
npx vercel --prod
```

### Opção 3: Netlify

```bash
npm run build
npx netlify deploy --prod --dir=.
```

## 🔧 Desenvolvimento Local

```bash
npm install
npm start
```

Acesse: `http://localhost:3000`

## 📊 Dados no Supabase

Tabela: `quiz_responses`

Campos:
- `id` (UUID, auto)
- `name` (text)
- `email` (text)
- `whatsapp` (text)
- `answers` (jsonb - array de índices das respostas)
- `created_at` (timestamp, auto)

## ✅ Status

- Quiz funcionando: ✅
- Dados sendo salvos: ✅
- Diagnóstico concluído: ✅
- Pronto para produção: ✅

## 🔐 Segurança

- RLS desativado no Supabase (permitir inserts públicas)
- API key pública (publishable, apenas insert)
- Sem validação de CSRF (quiz público)

## 📞 Suporte

Para debug, adicione `?debug=true` na URL para ver o log de diagnóstico na tela final.
