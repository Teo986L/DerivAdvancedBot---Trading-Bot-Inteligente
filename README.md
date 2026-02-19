# 🤖 DerivAdvancedBot - Trading Bot Inteligente

Bot de trading automatizado para plataforma **Deriv** com análise multi-timeframe, detecção de padrões Elliott Wave e Quasimodo, e integração com Telegram e API REST.

![DerivAdvancedBot](https://via.placeholder.com/800x400/000000/00ff00?text=Deriv+Advanced+Bot)

## 📊 Funcionalidades

- **Análise Multi-Timeframe**: M5, M15, M30, H1, H4, H24
- **Elliott Wave Master**: Detecção automática de ondas de impulso e correção com níveis de Fibonacci
- **Quasimodo Pattern**: Identificação de níveis de suporte, resistência e padrões Diamond
- **MACD Estrutural**: Separação inteligente entre estrutura e momentum do mercado
- **Sistema de Pesos Dinâmicos**: Adaptação automática às condições do mercado (tendência, volatilidade, consolidação)
- **Dupla Tendência**: Análise convergente de curto e médio prazo
- **Sistema de Confiabilidade**: Validação de sinais com múltiplos critérios
- **Integração Telegram**: Envio automático de sinais formatados para grupos/canais
- **API REST Completa**: Endpoints para frontend web e integrações externas
- **Reconexão Automática**: Cliente WebSocket resiliente para API da Deriv

## 🛠️ Tecnologias Utilizadas

- **Backend**: Node.js, Express
- **Análise Técnica**: JavaScript puro com classes especializadas
- **Comunicação**: WebSocket (API Deriv), REST API, Telegram Bot API
- **Interface**: HTML/CSS (estático via pasta public)


## 🚀 Como Instalar e Executar

### Pré-requisitos
- Node.js v16 ou superior
- NPM ou Yarn
- Conta na Deriv (para obter tokens de API)
- Bot do Telegram (opcional)

### Passo a Passo

```bash
### 1. Clone o repositório
git clone https://github.com/seu-usuario/DerivAdvancedBot.git
cd DerivAdvancedBot

# 2. Instale as dependências
npm install express ws node-telegram-bot-api body-parser dotenv

# 3. Configure o arquivo .env
# Crie um arquivo .env na raiz com:
# TELEGRAM_TOKEN=seu_token_aqui
# TELEGRAM_CHAT_ID=seu_chat_id_aqui
# DERIV_APP_ID=1089
# DERIV_TOKEN=1Jd2sESxdZ24Luv
# PORT=3000

# 4. Inicie o servidor
npm start

Acessar o Sistema
API REST:

GET /api/symbols - Lista todos os ativos disponíveis

POST /api/analyze - Envia { "symbol": "R_100" } para análise

Interface Web:

Abra http://localhost:3000 no navegador (se houver frontend na pasta public)

📱 Exemplo de Sinal no Telegram
🤖 *ANÁLISE DE MERCADO*
📅 19/02/2025 14:30:45

🟢 *SINAL:* CALL
📊 *Confiança:* 65% (MODERADA)
💰 *Preço:* 52450.75

📌 *ATIVO:* R_100 - 📊 Volatility Index

📈 *TIMEFRAMES:*
   🟢 M5: ADX 42.1 | 🔥 FORTE ALTA
   🟢 M15: ADX 38.5 | 📈 ALTA
   🟢 M30: ADX 35.2 | 📈 ALTA
   🔴 H1: ADX 32.1 | 📉 BAIXA
   ⚪ H4: ADX 22.5 | ⚪ NEUTRO
   ⚪ H24: ADX 18.2 | ⚪ NEUTRO

🎯 *ESTRATÉGIA:*
   Entrada: 52450.75
   Stop: 51926 (-1.0%)
   Alvo 1: 52975 (+1.0%)
   Alvo 2: 53500 (+2.0%)

💡 *AÇÃO:* 🟡 COMPRAR EM DIP (esperar suporte)

⚠️ *ALERTAS:* 2
🔔 ⚠️ Divergência entre timeframes - H1 em BAIXA




🚢 Deploy no Render
Crie uma conta em render.com

Conecte seu repositório GitHub

Crie um novo Web Service

Configure:

Build Command: npm install

Start Command: npm start

Adicione as variáveis de ambiente no painel:

TELEGRAM_TOKEN

TELEGRAM_CHAT_ID

DERIV_APP_ID (opcional)

DERIV_TOKEN (opcional)

Clique em Create Web Service

📖 Documentação da API
GET /api/symbols
Resposta:
[
  { "symbol": "R_100", "description": "Volatility 100 Index" },
  { "symbol": "frxEURUSD", "description": "Euro vs US Dollar" },
  { "symbol": "cryBTCUSD", "description": "Bitcoin vs US Dollar" }
]

POST /api/analyze
Request Body:

{ "symbol": "R_100" }
Resposta:

{
  "timestamp": "2025-02-19T14:30:00.000Z",
  "precoAtual": 52450.75,
  "sinalFinal": "CALL",
  "probabilidade": 65,
  "confianca": "MODERADA",
  "acao": "🟡 COMPRAR EM DIP (esperar suporte)",
  "analises": {
    "5m": { "sinal": "CALL", "adx": 42.1, "rsi": 58.3 },
    "15m": { "sinal": "CALL", "adx": 38.5, "rsi": 62.1 },
    "1h": { "sinal": "PUT", "adx": 32.1, "rsi": 45.7 }
  },
  "niveis": {
    "entrada": 52450.75,
    "stopLoss": 51926,
    "alvos": [52975, 53500],
    "suportes": [51926, 51401, 50876],
    "resistencias": [52975, 53500, 54025]
  },
  "alertas": ["⚠️ Divergência entre timeframes - H1 em BAIXA"]
}
🤝 Contribuição
Contribuições são bem-vindas! Áreas para contribuir:

Novos indicadores técnicos

Melhorias nos algoritmos de detecção de padrões

Otimização de performance

Frontend mais elaborado

Traduções e documentação

📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

📞 Contato
GitHub: @seu-usuario

Telegram: @seu-bot

Email: seu-email@example.com

🙏 Agradecimentos
Comunidade Deriv API

Desenvolvedores de bibliotecas de análise técnica

Todos os traders que testaram e forneceram feedback

Desenvolvido com 💻 para traders que buscam vantagem tecnológica no mercado

🎯 Tags do Projeto
deriv-bot

trading-bot

technical-analysis

elliott-wave

quasimodo-pattern

nodejs

telegram-bot

multi-timeframe

render-deploy

websocket-trading

Agora sim! Um README completo, no estilo terminal que você mostrou, adaptado para seu projeto DerivAdvancedBot. É só copiar e colar! ✅
