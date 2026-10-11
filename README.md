# 🔐 OWASP Juice Shop Security Lab

Laboratório prático de **Segurança em Aplicações Web**, criado para aplicar conceitos de cibersegurança em um ambiente local, controlado e propositalmente vulnerável.

## 🎯 Objetivo

O objetivo deste projeto é estudar na prática como aplicações web se comunicam com o backend e como ferramentas de segurança podem auxiliar na identificação e análise de vulnerabilidades.

Todos os testes deste projeto são realizados exclusivamente em ambiente local e controlado.

## 🛠️ Ferramentas utilizadas

- Windows
- WSL
- Docker Desktop
- Docker
- OWASP Juice Shop
- Chrome DevTools
- OWASP ZAP
- Java / Eclipse Temurin JDK 17

## 🧪 Ambiente do laboratório

O OWASP Juice Shop foi executado através de um container Docker e disponibilizado localmente em:

`http://localhost:3000`

Estrutura simplificada:

    Navegador
        ↓
    OWASP ZAP
        ↓
    OWASP Juice Shop
        ↓
    Docker

## 🌐 Análise HTTP

Utilizando o Chrome DevTools, foram observados:

- Requisições HTTP
- Métodos HTTP
- Status Codes
- Request Headers
- Response Headers
- Endpoints da API
- Respostas JSON
- Conceitos de autenticação e sessão

Isso permitiu visualizar na prática o fluxo:

    Navegador
        ↓
    Requisição HTTP
        ↓
    Backend / API
        ↓
    Resposta HTTP
        ↓
    Navegador

## 🛡️ Análise com OWASP ZAP

O OWASP ZAP foi configurado como proxy para observar a comunicação entre o navegador e o Juice Shop.

Durante a navegação, o ZAP realizou análise passiva das requisições e respostas HTTP.

## 🔎 Alertas observados

Entre os alertas encontrados durante a análise estavam:

- Content Security Policy (CSP) Header Not Set
- Missing Anti-clickjacking Header
- X-Content-Type-Options Header Missing
- Private IP Disclosure
- Session ID in URL Rewrite

Os alertas automáticos são tratados como pontos de investigação e não automaticamente como vulnerabilidades confirmadas.

## 🔐 Autenticação x Autorização

Durante o laboratório também foram estudados dois conceitos importantes:

**Autenticação:** verifica quem é o usuário.

**Autorização:** determina quais recursos aquele usuário possui permissão para acessar.

Uma aplicação segura precisa implementar corretamente os dois mecanismos.

## 💾 Relação com SQL

Este laboratório complementa meus estudos de SQL e banco de dados.

Aplicações web recebem informações do usuário, processam essas informações no backend e podem realizar operações no banco de dados.

Entre as principais medidas contra SQL Injection estão:

- Prepared Statements
- Consultas parametrizadas
- Validação de entradas
- Princípio do menor privilégio

## 📊 Possíveis impactos em empresas

Vulnerabilidades em aplicações web podem resultar em:

- Exposição de informações
- Acesso não autorizado
- Comprometimento de contas
- Alteração ou exclusão de dados
- Indisponibilidade de serviços
- Prejuízos financeiros
- Danos à reputação
- Impactos relacionados à LGPD

## 📚 Aprendizados

Neste laboratório foram praticados conceitos relacionados a:

- HTTP
- APIs
- JSON
- Headers
- Autenticação
- Autorização
- Docker
- Containers
- Proxy de segurança
- Análise passiva
- Segurança de aplicações web

## 🚀 Próximas etapas

Este projeto continuará evoluindo com:

- Burp Suite
- SQL Injection em ambiente controlado
- SQLMap
- Testes de autenticação
- Testes de controle de acesso
- Análise e documentação de vulnerabilidades

## ⚠️ Uso responsável

Este projeto possui finalidade exclusivamente educacional.

Todos os testes são realizados somente em ambientes próprios, controlados ou explicitamente autorizados.
