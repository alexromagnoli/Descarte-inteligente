
---

### 2. `02-diagrama-sequencia-login.md`

```md
# Diagrama de Sequência — Login

## Descrição

Este diagrama representa o processo de autenticação de um usuário no sistema.

O usuário informa suas credenciais, o sistema realiza a validação e, caso os dados estejam corretos, permite o acesso ao dashboard.

## Diagrama

```mermaid
sequenceDiagram
    actor Usuario as Usuário
    participant Frontend as Front-end
    participant Backend as Back-end
    participant Banco as Banco de Dados

    Usuario->>Frontend: Informa e-mail e senha
    Frontend->>Backend: Envia credenciais
    Backend->>Banco: Consulta usuário
    Banco-->>Backend: Retorna dados do usuário

    alt Credenciais válidas
        Backend-->>Frontend: Autenticação aprovada
        Frontend-->>Usuario: Exibe dashboard
    else Credenciais inválidas
        Backend-->>Frontend: Autenticação recusada
        Frontend-->>Usuario: Exibe mensagem de erro
    end
