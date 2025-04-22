# 🤖 Botzito — Agendamentos Inteligentes via WhatsApp

**Botzito** é um sistema completo de automação de agendamentos via WhatsApp, integrado com inteligência artificial, voltado para pequenas empresas que desejam oferecer um atendimento moderno, automatizado e humanizado — sem depender de painel ou app.

## 🚀 Funcionalidades

- 📅 Agendamento Automatizado: Clientes agendam serviços diretamente pelo WhatsApp.
- 🧠 Atendimento com IA: Interações totalmente humanizadas e contextuais com OpenAI (sem uso de mensagens padronizadas).
- 🕐 Horários Dinâmicos: Geração automática de horários com base nos serviços cadastrados e funcionamento da empresa.
- 📲 Integração via Evolution API: Recebimento e envio de mensagens do WhatsApp de forma estável e em tempo real.
- 📡 Processamento com Fila (RabbitMQ): Alta performance e processamento assíncrono de mensagens.
- 📦 Cache Inteligente: Redis melhora performance e reduz carga no banco de dados.
- 🛠️ Deploy via Railway: Simples, rápido e escalável.
- 📱 100% WhatsApp: O cadastro da empresa e todo o uso do sistema é feito via mensagens no WhatsApp — sem painel ou app externo.

## 🧱 Tecnologias Utilizadas

- Node.js + NestJS
- PostgreSQL com Prisma ORM
- RabbitMQ (mensageria)
- Redis (cache)
- OpenAI API (inteligência artificial)
- Docker (infraestrutura)
- Railway (deploy)

## 📁 Estrutura do Projeto

src/  
├── application/        # Casos de uso e estratégias de aplicação  
│   ├── strategy/  
│   └── use-cases/  
├── core/               # Regras e lógica principal  
│   ├── constants/  
│   ├── domain/  
│   └── logic/  
├── domain/             # Entidades, enums, interfaces e tipos  
│   ├── entities/  
│   ├── enum/  
│   ├── interface/  
│   └── types/  
├── infra/              # Camada de infraestrutura (adapters, serviços, libs externas)  
│   ├── database/  
│   ├── gateway/  
│   ├── initializer/  
│   ├── messaging/  
│   ├── openai/  
│   ├── rabbitmq/  
│   ├── redis/  
│   └── rest/  
├── utils/              # Funções utilitárias e helpers  
└── main.ts             # Ponto de entrada da aplicação

## 🛠️ Como Rodar Localmente

Siga os passos abaixo para rodar o Botzito localmente com Docker + Yarn:

```bash
# Clone o repositório
git clone git@github.com:botzito/core.git

# Acesse a pasta do projeto
cd botzito

# Copie o arquivo de variáveis de ambiente
cp .env.example .env

# Suba os serviços com Docker
docker-compose up -d

# Instale as dependências do projeto
yarn install

# Inicie a aplicação em modo desenvolvimento
yarn start:dev
```

## 📌 Observações

- Cada empresa cadastrada possui seu próprio contexto e fluxo.  
- A IA utilizada é baseada em `assistants` da OpenAI, com `threads` separadas por cliente.  
- O sistema já trata fusos horários, tempos individuais de serviço e evita colisões nos agendamentos.  
- Todas as interações são feitas via WhatsApp — sem necessidade de painel, aplicativo ou site.

## 📞 Contato

Para dúvidas, parcerias ou sugestões, fale com a gente via [WhatsApp](https://wa.me/SEUNUMERO) ou abra uma issue neste repositório.

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
