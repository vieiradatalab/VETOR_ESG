# Quais países são mais semelhantes ao Brasil em indicadores ESG?

Um estudo em ciência de dados para comparar países a partir de indicadores ESG usando vetores, padronização, distância euclidiana e visualizações analíticas.

![Mapa de similaridade ESG em relação ao Brasil](images/esg_distance_brazil_worldmap.png)

## Visão geral

Este projeto investiga a similaridade entre países com base no conjunto de indicadores ESG, tomando o Brasil como referência.
A proposta foi representar cada país como um vetor de características e comparar sua posição com outros países de forma multivariada.
Em vez de observar um único indicador por vez, o estudo considera o comportamento conjunto das variáveis.

## Pergunta central

Quais países são mais semelhantes ao Brasil quando analisamos o conjunto de indicadores ESG como um vetor?

## Método

- Coleta e organização de indicadores ESG por país
- Limpeza e padronização dos dados
- Representação vetorial dos países
- Cálculo de distâncias para medir similaridade
- Visualização com mapa, gráficos e PCA

## Destaque visual

O mapa acima apresenta uma visão sintética da proximidade entre países em relação ao Brasil a partir dos indicadores ESG analisados.

## Principais achados

- A comparação multivariada oferece uma leitura mais consistente do que análises isoladas
- Indicadores individuais ajudam, mas não explicam o posicionamento completo dos países
- A abordagem vetorial permite identificar padrões de proximidade de forma mais robusta
- O estudo amplia a qualidade da comparação internacional em ESG

## Estrutura do repositório

- `notebooks/` → notebook principal do estudo
- `data/` → dados utilizados
- `images/` → gráficos exportados
- `README.md` → apresentação do projeto

## Como reproduzir
```bash
git clone https://github.com/vieiradatalab/VETOR_ESG.git
cd VETOR_ESG
pip install -r requirements.txt
