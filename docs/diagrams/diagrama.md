# Diagrama de Casos de Uso

## Descrição

Este diagrama apresenta as principais interações entre os usuários e o sistema da Lixeira Inteligente.

O sistema permite o gerenciamento de usuários, monitoramento dos resíduos orgânicos, identificação dos alimentos por inteligência artificial, controle de estoque e geração de relatórios.

## Diagrama

```mermaid
flowchart LR
    Admin((Administrador))
    Usuario((Usuário do Sistema))
    Lixeira((Lixeira Inteligente))

    subgraph Sistema["Sistema Food Trek"]
        Login["Realizar login"]
        Dashboard["Visualizar dashboard"]
        Usuarios["Gerenciar usuários"]
        Estoque["Gerenciar estoque"]
        Residuos["Monitorar resíduos"]
        Relatorios["Visualizar relatórios"]
        IA["Identificar alimento"]
        Peso["Registrar peso"]
        Desconhecido["Registrar alimento não identificado"]
    end

    Admin --> Login
    Admin --> Dashboard
    Admin --> Usuarios
    Admin --> Estoque
    Admin --> Relatorios

    Usuario --> Login
    Usuario --> Dashboard
    Usuario --> Residuos
    Usuario --> Estoque
    Usuario --> Relatorios

    Lixeira --> IA
    Lixeira --> Peso
    Lixeira --> Desconhecido

    IA --> Residuos
    Peso --> Residuos
    Desconhecido --> Residuos
