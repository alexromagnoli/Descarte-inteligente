# FoodTracks

Sistema inteligente para identificação, pesagem e monitoramento do desperdício de alimentos em restaurantes.

O FoodTracks é um projeto acadêmico desenvolvido no curso de Análise e Desenvolvimento de Sistemas da FATEC Araraquara. A proposta combina inteligência artificial, visão computacional, pesagem eletrônica e uma aplicação web para transformar o descarte de alimentos em dados úteis para a gestão.

## Sobre o projeto

O sistema busca identificar os alimentos descartados, registrar seu peso e o momento do descarte e disponibilizar essas informações para acompanhamento.

A partir dos dados coletados, o FoodTracks permite analisar o desperdício de alimentos, identificar itens não reconhecidos pela inteligência artificial e acompanhar informações relacionadas ao estoque.

## Como funciona

O funcionamento do sistema é baseado em quatro etapas principais:

1. A câmera captura o alimento descartado.
2. O modelo de inteligência artificial realiza a identificação.
3. O sistema de pesagem registra o peso do descarte.
4. Os dados são armazenados e disponibilizados na aplicação web.

Quando um alimento não puder ser identificado, o evento poderá ser registrado para análise posterior.

## Protótipo

O protótipo da aplicação web foi desenvolvido no Figma e apresenta a proposta inicial da interface e do dashboard do FoodTracks.

[Acessar protótipo no Figma](https://www.figma.com/make/BISTgMS8WHvVgGteUsSIJb/Lixeira-Inteligente-Dashboard?t=WdE8vtCaLESAH3Qt-1)

## Infraestrutura Técnica

### Aplicação Web

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=plastic&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=plastic&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=plastic&logo=javascript&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=plastic&logo=tailwindcss&logoColor=white)

### Inteligência Artificial

![Python](https://img.shields.io/badge/Python-3776AB?style=plastic&logo=python&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLOv8-111F68?style=plastic)

### Banco de Dados

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=plastic&logo=mysql&logoColor=white)

## Hardware

O protótipo utiliza os seguintes componentes:

* Arduino
* Raspberry Pi
* Câmera
* Módulo HX711
* 4 células de carga de 50 kg
* Iluminação auxiliar
* Estrutura física produzida por impressão 3D

## Sistema Web

A aplicação permitirá acompanhar informações relacionadas aos descartes realizados pelo estabelecimento, incluindo:

* quantidade de desperdício;
* peso dos alimentos descartados;
* desperdício por alimento;
* evolução dos descartes ao longo do tempo;
* alimentos não identificados;
* relatórios e gráficos;
* informações relacionadas ao estoque.

## Inteligência Artificial

A identificação dos alimentos será realizada utilizando visão computacional.

O modelo será desenvolvido em Python e utilizará **YOLOv8** para reconhecer os alimentos durante o descarte.

## Documentação

A documentação técnica do projeto está disponível na pasta `docs`.

Atualmente, o projeto contempla:

* Protótipo da aplicação web
* Diagrama de Casos de Uso
* Modelagem do Banco de Dados
* Documentação do sistema

Novos diagramas e documentos serão adicionados durante o desenvolvimento.

## Equipe

Projeto desenvolvido por estudantes de Análise e Desenvolvimento de Sistemas da FATEC Araraquara.

| Integrante | GitHub |
| --- | --- |
| Alex Gabriel Romagnoli | alexromagnoli |
| André Capella| ancapella |
| Deivison Miranda Gomes | odeivison |
| João | |
| Nafitaly Vitória | hellooviic |
| Thiago Gotardo | thiagogosantos57-ops |

## Contexto Acadêmico

Projeto Integrador desenvolvido no curso de Análise e Desenvolvimento de Sistemas da FATEC Araraquara.

O projeto integra conhecimentos de desenvolvimento web, banco de dados, inteligência artificial, visão computacional, Internet das Coisas e sistemas embarcados.

## Status

Em desenvolvimento.
