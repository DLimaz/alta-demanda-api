API Sob Alta Demanda

API para gerenciamento de recursos escassos com alta concorrência. Gerencia 100 vagas com cota máxima de 2 por usuário, garantindo atomicidade e justiça.
Problema Resolvido

Em sistemas com recursos finitos (vendas de ingressos, processamento em lote, e-commerce), a demanda concentrada pode causar race conditions onde dois usuários conseguem alocar o mesmo recurso simultaneamente.

Esta API implementa uma solução atômica usando transações e updates condicionais no banco de dados.
Funcionalidades

    Pool global de exatamente 100 vagas

    Cota pessoal de máximo 2 vagas por usuário

    Operações atômicas - sem race conditions

    Autenticação JWT

    Containerizada com Docker

    Respostas padronizadas (200, 409, 401)

Tecnologias

    Node.js - Runtime JavaScript

    Express - Framework web

    SQLite - Banco de dados embutido

    JWT - Autenticação

    Docker - Containerização

Como Executar
Pré-requisitos

    Docker Desktop instalado

Passos
Bash

# 1. Clone o repositório
git clone https://github.com/seu-usuario/alta-demanda-api.git
cd alta-demanda-api

# 2. Execute com Docker
docker compose up --build

# 3. A API estará disponível em http://localhost:8080
