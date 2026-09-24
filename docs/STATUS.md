# Status de implementação — Vittae

Este documento resume o estado público do projeto sem expor o código-fonte privado.

## Implementado

### Frontend

- SPA em React/Vite;
- rotas públicas e dashboard;
- páginas de home, descoberta, perfil, agendamento, voucher e autenticação;
- busca, filtros e ordenação sobre catálogo demonstrativo;
- tratamento de estados vazios e rotas inválidas;
- cuidados básicos de acessibilidade e responsividade;
- integração real do frontend com os endpoints de autenticação.

### Backend

- API Express independente;
- configuração validada por ambiente;
- health e readiness;
- CORS, Helmet e rate limiting;
- logging estruturado;
- contrato consistente de sucesso/erro;
- Prisma e PostgreSQL em ambiente de desenvolvimento;
- migrations e validações de integridade;
- suíte de testes sem exigir banco externo para os casos principais.

### Autenticação

- cadastro;
- login;
- refresh de sessão;
- logout;
- logout global;
- endpoint de sessão atual;
- senha com Argon2id;
- access token JWT;
- refresh opaco em cookie HttpOnly;
- rotação e revogação;
- dashboard protegido no frontend;
- restauração de sessão.

## Parcial / demonstrativo

As áreas abaixo possuem interface e/ou modelagem, mas ainda não representam uma operação completa de produção:

- perfis e serviços;
- favoritos;
- agenda;
- clientes;
- financeiro;
- planos;
- avaliações;
- voucher;
- páginas institucionais e contatos.

## Planejado

- recuperação de senha;
- verificação de e-mail;
- CRUDs e APIs de negócio;
- persistência real do agendamento;
- regras de concorrência e disponibilidade;
- cancelamento e reagendamento;
- pagamentos e assinaturas;
- emissão e resgate transacional de vouchers;
- notificações;
- uploads;
- observabilidade de produção;
- CI e ampliação dos testes E2E;
- hospedagem pública do produto.

## Princípio de documentação

O projeto diferencia explicitamente:

- **interface existente**;
- **modelagem de banco existente**;
- **backend implementado**;
- **integração efetivamente operacional**.

Uma tabela no banco ou uma tela no frontend não é apresentada como funcionalidade concluída se o fluxo completo ainda não existe.
