<p align="center">
<a href="https://github.com/anthonymengottii/igaming-platform_public"><img src="https://img.shields.io/badge/GitHub-Repository-blue?style=flat-square&logo=github" alt="GitHub Repository"></a>
<a href="https://github.com/anthonymengottii/igaming-platform_public/stargazers"><img src="https://img.shields.io/github/stars/anthonymengottii/igaming-platform_public?style=flat-square" alt="GitHub Stars"></a>
<a href="https://usealpa.online/"><img src="https://img.shields.io/badge/Site-Em%20Produção-green?style=flat-square" alt="Site em Produção"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Laravel Version"></a>
</p>

## 🎰 Plataforma iGaming - Projeto de Portfólio

Esta é uma **plataforma completa de iGaming** desenvolvida em PHP utilizando o Framework Laravel 10 e Vue 3,
com várias integrações com diferentes provedores de jogos e gateways de pagamento.

> **ℹ️ Sobre este Repositório:** Este repositório contém apenas a documentação e descrição do projeto. O código-fonte é mantido em repositório privado.

> **⚠️ Aviso Legal:** Este software é destinado apenas para uso em jurisdições onde o iGaming é legalmente permitido. Use-o com responsabilidade e consciência, e não o utilize para fins fraudulentos.

## 🚀 Tecnologias Utilizadas

- **Backend:** Laravel 10 (PHP 8.1+)
- **Frontend:** Vue 3, Pinia, Vue Router
- **UI Framework:** Filament 3, Tailwind CSS, Flowbite
- **Autenticação:** Laravel Sanctum, JWT Auth
- **Banco de Dados:** MySQL/MariaDB
- **WebSockets:** Laravel Echo, Pusher
- **Build Tool:** Vite

## ✨ Recursos Principais

### 🔐 Autenticação e Segurança
- Autenticação com Google OAuth
- Sistema de permissões e roles (Spatie Permissions)
- Middlewares de segurança personalizados (CheckAdmin, CheckAffiliate)
- Validação de tokens para transações de jogos
- Proteção contra fraudes em requisições de vitórias

### 🎮 Provedores de Jogos Integrados
- **Slotegrator** - Plataforma completa de jogos
- **Salsa Games** - Jogos de cassino
- **EverGame** - Provedor de jogos com validação de tokens
- **WorldSlot** - Integração completa com validação de segurança
- **Fivers** - Método Seamless para integração transparente
- **PlayFiver** - Provedor adicional de jogos
- **Nexus** - Integração de jogos
- **Drakon** - Provedor de jogos
- **Games2Api** - API de jogos
- **Vibra** - Plataforma de jogos
- **VeniX** - Provedor de jogos
- **PlayGaming** - Integração com validação de tokens
- **PrivateGames** - Jogos privados
- **KaGaming** - Provedor adicional

### 💳 Gateways de Pagamento
- **DigitoPay** - Gateway principal
- **Stripe** - Pagamentos internacionais
- **SuitPay** - Gateway de pagamento
- **BSPay** - Integração de pagamentos
- **UPay Brasil** - Gateway brasileiro com PIX

### 👥 Sistema de Afiliados
- Sistema de Afiliados com RevShare e CPA
- Painel de Afiliados separado e completo
- Sistema de Sub-afiliados
- Controle de comissões e saques
- Dashboard com estatísticas detalhadas
- Histórico completo de transações

### 🎯 Funcionalidades do Sistema

#### Painel Administrativo Completo (Filament 3)
- Gerenciamento de usuários, jogos e provedores
- Controle de depósitos e saques
- Gestão de banners e slides
- Configurações avançadas
- Sistema de missões
- Controle de VIP
- Gerenciamento de categorias de jogos

#### Painel de Afiliados
- Dashboard personalizado
- Controle de sub-afiliados
- Histórico de comissões
- Solicitação de saques

#### Sistema de Notificações
- Notificações em tempo real via WebSockets
- Notificações de depósitos e saques
- Sistema de eventos (GameWin, SportBet, etc.)

#### Sistema de Jogos
- Favoritos e likes
- Avaliações de jogos
- Jogos em destaque
- Busca avançada
- Controle de RTP (Return to Player)
- Visualizações e estatísticas

#### Sistema de Missões
- Missões personalizáveis
- Sistema de recompensas
- Controle de progresso

#### Sistema VIP
- Níveis VIP configuráveis
- Benefícios por nível
- Controle de usuários VIP

#### Sistema de Roleta (Spin)
- Configurações de roleta
- Controle de execuções
- Sistema de prêmios

#### Customização
- Customização de layout CSS
- Gerenciamento de banners e slides
- Personalização de temas
- Sistema de moedas múltiplas

#### Sistema de GGR (Gross Gaming Revenue)
- Controle de GGR por provedor
- Relatórios detalhados
- Análise de performance

## 🔄 Arquitetura e Desenvolvimento

### 🏗️ Estrutura do Projeto

#### Organização Modular
- **Estrutura de rotas modular** - Sistema organizado em `routes/groups/`
  - Separação clara entre rotas de provedores, gateways, autenticação e layouts
  - Facilita manutenção e escalabilidade
  - Reduz acoplamento entre módulos

#### Sistema de Traits
- **Provedores de jogos** - Implementação através de Traits
  - Cada provedor possui sua própria trait em `app/Traits/Providers/`
  - Código mais limpo e reutilizável
  - Facilita adição de novos provedores
  - Isolamento de lógica específica de cada integração

#### Separação de Responsabilidades
- **Controllers organizados** - Separação clara de responsabilidades
  - Controllers específicos para cada funcionalidade
  - Redução de código duplicado
  - Melhor organização e legibilidade

### 🔐 Segurança

#### Middlewares Personalizados
- **Validação de acesso** - Middlewares específicos para cada painel
  - `CheckAdmin` - Validação exclusiva para painel administrativo
  - `CheckAffiliate` - Validação exclusiva para painel de afiliados
  - Separação completa de permissões entre painéis
  - Prevenção de acesso não autorizado

#### Validação de Tokens
- **Sistema de validação de tokens** implementado
  - Implementação em múltiplos provedores (EverGame, WorldSlot, PlayGaming)
  - Prevenção de fraudes em transações
  - Validação centralizada e reutilizável

### 💳 Gateways de Pagamento

#### Estrutura Unificada
- **Padronização de implementação** para todos os gateways
  - Sistema de serviços para cada gateway
  - Melhor tratamento de erros e exceções
  - Webhooks automatizados e mais confiáveis

### 🎮 Provedores de Jogos

#### Padronização de Integrações
- **Todos os provedores** seguem padrão único
  - Sistema de traits permite fácil manutenção
  - Tratamento de erros padronizado
  - Logs e debugging melhorados

### 🎨 Frontend

#### Vue 3 com Composition API
- **Migração para Vue 3** com Composition API
- Implementação de **Pinia** para gerenciamento de estado
- Componentes reutilizáveis e modulares
- Melhor performance e experiência do usuário

#### Filament 3
- **Painéis administrativos** desenvolvidos com Filament 3
- Interface moderna e responsiva
- Melhor organização de recursos

### 📊 Banco de Dados

#### Otimização de Queries
- **Refatoração de queries N+1**
- Implementação de eager loading onde necessário
- Índices adicionados para melhor performance
- Otimização de relacionamentos entre models

#### Models Otimizados
- Uso de **Attribute Casting** para proteção de dados sensíveis
- Melhor organização de fillable/hidden attributes
- Relacionamentos otimizados
- Accessors e Mutators implementados

### 🚀 Performance

#### Cache e Otimização
- Implementação de cache estratégico
- Otimização de rotas e configurações
- Melhor uso de recursos do Laravel
- Redução de tempo de resposta

#### Build e Assets
- Migração para **Vite** (substituindo Mix)
- Build mais rápido e eficiente
- Melhor organização de assets
- Hot Module Replacement (HMR) para desenvolvimento

### 🧪 Qualidade de Código

#### Padrões e Boas Práticas
- **PSR-12** - Padrão de codificação seguido
- Código mais limpo e legível
- Comentários e documentação melhorados
- Nomes de variáveis e métodos mais descritivos

#### Tratamento de Erros
- Sistema de exceções personalizadas
- Melhor tratamento de erros em APIs
- Logs mais informativos
- Mensagens de erro mais claras para desenvolvedores

## 🔒 Melhorias e Correções de Segurança

Esta plataforma passou por diversas melhorias para prevenir ataques e proteger os usuários contra ações maliciosas.

### 🔐 Segurança de Acesso aos Painéis

#### Problema: Rotas do admin sendo acessadas pelo painel de afiliados
Esse problema ocorria devido à ausência de uma validação separada, permitindo que algumas páginas do 
administrador fossem acessadas pelo painel de afiliado usando a mesma sessão e função.

**Solução Implementada:**
- **Novos middlewares criados** para permitir bloqueios e validações individuais nos painéis:
  - `CheckAdmin` - Validação exclusiva para administradores
  - `CheckAffiliate` - Validação exclusiva para afiliados
- Separação completa de permissões entre painéis
- Validação de roles em todas as rotas sensíveis

### 🎮 Segurança em Provedores de Jogos

#### Validação de Tokens em Provedores
Para evitar que dados de vitória sejam enviados via requisição e o saldo seja fraudado, implementamos um sistema 
de tokens para validar as transações recebidas nos seguintes provedores:

- **EverGame** - Sistema de validação de tokens implementado
- **WorldSlot** - Validação de segurança nas transações
- **PlayGaming** - Proteção contra requisições fraudulentas

### 💳 Melhorias nos Gateways de Pagamento

#### DigitoPay - Melhorias de Segurança

1. **Mudanças na Consulta de Status**
   - Anteriormente: Enviávamos apenas o ID da transação para o front-end
   - Agora: Enviamos tanto o ID da transação quanto o ID de verificação
   - Benefício: Permite realizar a chamada da transação com maior segurança

2. **Verificação Adicional no Webhook**
   - Implementada verificação adicional na confirmação de depósito
   - Garante que o pagamento foi realmente aprovado antes de creditar o saldo
   - Previne fraudes e duplicação de créditos

3. **Webhook Automatizado**
   - Webhook da DigitoPay agora é automaticamente configurado
   - Reduz erros de configuração manual
   - Melhora a confiabilidade do sistema

#### Novos Gateways Implementados
- **Stripe** - Integração completa com suporte a webhooks
- **SuitPay** - Gateway de pagamento brasileiro
- **BSPay** - Integração de pagamentos
- **U Pay Brasil** - Gateway com suporte a PIX e consulta de status

### 🛡️ Outras Melhorias de Segurança

- Sistema de validação de tokens em todas as transações críticas
- Proteção contra CSRF em todas as rotas
- Validação de permissões em nível de middleware
- Sistema de logs para auditoria de ações administrativas
- Proteção de dados sensíveis com atributos ocultos em modo demo

## 📋 Requisitos do Sistema

### Requisitos Mínimos
- **PHP:** 8.1 ou superior
- **Composer:** 2.0 ou superior
- **Node.js:** 16.x ou superior
- **NPM:** 8.x ou superior
- **Banco de Dados:** MySQL 5.7+ ou MariaDB 10.3+
- **Extensões PHP:** curl, intl, libxml, simplexml, zip

## 📸 Screenshots

> **Nota:** As imagens podem levar alguns segundos para carregar devido ao tamanho dos arquivos.

### Interface Principal
<p align="center">
  <img src="screenshots/main.png" alt="Interface Principal" width="800"/>
</p>

### Painel Administrativo

#### Configurações Gerais
<p align="center">
  <img src="screenshots/admin-settings.png" alt="Configurações do Sistema" width="800"/>
</p>

#### Configurações de Gateways
<p align="center">
  <img src="screenshots/admin-settings-gateway.png" alt="Configurações de Gateways" width="800"/>
</p>

#### Gerenciamento de Provedores
<p align="center">
  <img src="screenshots/admin-providers.png" alt="Gerenciamento de Provedores" width="800"/>
</p>

#### Customização
<p align="center">
  <img src="screenshots/admin-customization.png" alt="Customização do Sistema" width="800"/>
</p>

### Interface do Usuário

#### Jogos
<p align="center">
  <img src="screenshots/game.png" alt="Interface de Jogos" width="800"/>
</p>

#### Jogos Mobile
<p align="center">
  <img src="screenshots/game-mobile.png" alt="Interface Mobile" width="400"/>
</p>

#### Depósitos
<p align="center">
  <img src="screenshots/deposits.png" alt="Sistema de Depósitos" width="800"/>
</p>

#### Idiomas
<p align="center">
  <img src="screenshots/languages.png" alt="Seleção de Idiomas" width="800"/>
</p>

## 🛠️ Tecnologias e Ferramentas

### Backend
- Laravel 10
- PHP 8.1+
- MySQL/MariaDB
- Laravel Sanctum
- JWT Auth
- Spatie Permissions

### Frontend
- Vue 3
- Pinia
- Vue Router
- Tailwind CSS
- Flowbite
- Vite

### Admin Panel
- Filament 3
- Laravel Modules

### Integrações
- Laravel Echo
- Pusher
- Guzzle HTTP
- Stripe SDK

## 📝 Notas de Desenvolvimento

### Estrutura de Rotas
O projeto utiliza uma estrutura modular de rotas:
- `routes/groups/provider/` - Rotas dos provedores de jogos
- `routes/groups/gateways/` - Rotas dos gateways de pagamento
- `routes/groups/auth/` - Rotas de autenticação
- `routes/groups/layouts/` - Rotas de layout

### Traits de Provedores
Cada provedor possui sua própria trait em `app/Traits/Providers/`:
- Facilita a manutenção e extensão
- Permite reutilização de código
- Isola a lógica específica de cada provedor

### Sistema de Módulos
O projeto utiliza `nwidart/laravel-modules` para organização modular do código.

## 🎯 Desafios e Soluções

### Desafios Enfrentados

1. **Integração com Múltiplos Provedores**
   - Desafio: Cada provedor possui APIs diferentes e padrões distintos
   - Solução: Criação de sistema de Traits padronizado, facilitando a integração de novos provedores

2. **Segurança em Transações**
   - Desafio: Prevenir fraudes em transações de jogos
   - Solução: Implementação de sistema de validação de tokens em múltiplos provedores

3. **Separação de Painéis**
   - Desafio: Garantir que painéis administrativo e de afiliados sejam completamente separados
   - Solução: Criação de middlewares específicos (CheckAdmin, CheckAffiliate)

4. **Performance e Escalabilidade**
   - Desafio: Otimizar queries e melhorar performance
   - Solução: Refatoração de queries N+1, implementação de eager loading e cache estratégico

## 📌 Status do Projeto

Este projeto está **em produção** e sendo continuamente melhorado com novas funcionalidades e otimizações.

🌐 **Site em Produção:** [https://usealpa.online/](https://usealpa.online/)

## 📧 Contato

Para mais informações sobre o projeto, entre em contato através do GitHub.

---

**Nota:** Este repositório contém apenas a documentação do projeto. O código-fonte é mantido em repositório privado.

