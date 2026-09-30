# Diagrama de Classes

## Descrição

Este diagrama apresenta as principais entidades utilizadas pelo sistema Food Trek e seus relacionamentos.

As classes representam usuários, resíduos, alimentos, registros de pesagem, estoque e relatórios.

## Diagrama

```mermaid
classDiagram

    class Usuario {
        +int id
        +string nome
        +string email
        +string senha
        +string perfil
        +login()
        +logout()
    }

    class Alimento {
        +int id
        +string nome
        +string categoria
        +float pesoMedio
    }

    class Residuo {
        +int id
        +datetime dataHora
        +float peso
        +string status
        +string imagem
    }

    class RegistroPesagem {
        +int id
        +float peso
        +datetime dataHora
        +registrarPeso()
    }

    class Estoque {
        +int id
        +string ingrediente
        +float quantidade
        +float estoqueMinimo
        +atualizarEstoque()
        +verificarEstoque()
    }

    class Relatorio {
        +int id
        +string tipo
        +datetime periodoInicial
        +datetime periodoFinal
        +gerarRelatorio()
    }

    class IdentificacaoIA {
        +int id
        +string classeDetectada
        +float confianca
        +identificarAlimento()
    }

    Usuario "1" --> "0..*" Relatorio : gera
    Usuario "1" --> "0..*" Residuo : consulta

    Residuo "1" --> "1" RegistroPesagem : possui
    Residuo "1" --> "0..1" IdentificacaoIA : possui
    IdentificacaoIA "0..*" --> "1" Alimento : identifica

    Alimento "1" --> "0..*" Estoque : relacionado
    Relatorio "1" --> "0..*" Residuo : utiliza dados
