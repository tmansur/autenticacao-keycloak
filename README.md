# Autenticação e Keycloak

## OAuth 2.0

Protocolo padrão que define regras para **autorização** (o que posso acessar?). Possui diferentes fluxos de autorização definidos para atender a diferentes necessidades: sistemas web, acesso entre serviços (sem interface para usuário), etc.

Composto de 4 elementros principias (roles):

- Resource owner (proprietário do recurso): usuário ou aplicativo que possui o recurso protegido que precisa ser acessado. Exemplo: um app precisa acessar seus dados do facebook para fazer autenticação, você é o proprietário do recurso (dados do facebook) e o único que pode conceder acesso.
- Authorization server (servidor de autorização): servidor que autentica o proprietário do recurso e concede permissões de acesso ao aplicativo solicitante ao servidor de recurso (através de tokens de acesso). Exemplo: Servidor do Facebook onde está implementado OAuth 2.0.
- Client (Aplicativo solicitante): aplicativo que solicita acesso ao recurso protegido. Deve possuir credenciais de acesso para autenticar-se junto ao servidor de autorização. Exemplo: aplicativo que precisa das informações do Facebook do usuário.
- Resource server: servidor onde o recurso protegido está hospedado. Retorna os recursos apropriados de acordo como o token que recebe. Exemplo: servidor do Facebook onde estão as informações do usuário.

## Open ID Connect

Principal protocolo de **autenticação** (posso acessar algo?) existente no mercado, é uma camada de autenticação baseada em token sobre o protocolo OAuth 2.0. Permite que usuários se autentiquem em diferentes sites usando identidade única: Single Sign-On (SSO).

