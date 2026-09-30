# Diagrama de Componentes

## Descrição

Este diagrama apresenta os principais componentes de software e hardware do sistema Food Trek.

A Lixeira Inteligente utiliza câmera para captura das imagens, células de carga para medição do peso, Arduino com HX711 para leitura das células e Raspberry Pi para processamento e comunicação com o sistema.

## Diagrama

```mermaid
flowchart TB

    subgraph Hardware["Lixeira Inteligente"]
        Camera["Câmera"]
        Arduino["Arduino"]
        HX711["Módulo HX711"]
        LoadCells["4 Células de Carga"]
        Raspberry["Raspberry Pi"]
    end

    subgraph Software["Sistema Food Trek"]
        Frontend["Front-end"]
        Backend["Back-end"]
        IA["Módulo de Inteligência Artificial"]
        Database["Banco de Dados"]
        Dashboard["Dashboard"]
    end

    LoadCells --> HX711
    HX711 --> Arduino
    Arduino --> Raspberry
    Camera --> Raspberry

    Raspberry --> IA
    IA --> Backend
    Raspberry --> Backend

    Frontend --> Backend
    Backend --> Database
    Backend --> Dashboard
