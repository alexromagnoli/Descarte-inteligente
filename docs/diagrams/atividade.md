# Diagrama de Atividade — Registro de Resíduo

## Descrição

Este diagrama representa o fluxo principal realizado quando um alimento é descartado na Lixeira Inteligente.

A câmera captura a imagem, a inteligência artificial tenta identificar o alimento e o sistema registra o peso do resíduo.

Caso o alimento não seja identificado, o sistema registra o evento como "não identificado", armazenando a imagem e o horário para posterior análise.

## Diagrama

```mermaid
flowchart TD

    A([Início]) --> B["Alimento descartado"]
    B --> C["Câmera captura imagem"]
    C --> D["Sistema realiza detecção"]
    D --> E{"Alimento identificado?"}

    E -->|Sim| F["Identificar alimento"]
    F --> G["Realizar pesagem"]
    G --> H["Registrar resíduo"]
    H --> I["Atualizar informações de estoque"]
    I --> J["Atualizar dashboard"]

    E -->|Não| K["Classificar como não identificado"]
    K --> L["Armazenar imagem e horário"]
    L --> G

    J --> M([Fim])
