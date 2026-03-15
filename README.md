# O que significa “parecido” em dados ESG?
Quando alguém pergunta: **“Quais países são mais parecidos com o Brasil em termos de indicadores ESG?”**  
A resposta mais comum costuma vir em forma de **médias**, **rankings** ou **índices agregados**.  
Mas existe uma questão metodológica aqui.
**ESG não é uma variável**. É um **conjunto de variáveis ao mesmo tempo!!**

Indicadores <u>ambientais</u>, <u>sociais</u> e de <u>governança</u> formam um **sistema multidimensional**.  
Quando tentamos comparar países apenas olhando <u>médias</u> ou <u>rankings</u>, estamos simplificando demais um problema que é naturalmente mais complexo.  
Medidas como **média**, **mediana**, **variância** e **desvio padrão** são extremamente úteis mas, elas respondem a perguntas específicas:
 - <u><span style="color:blue">Qual é o valor típico de um indicador?</span></u>
 - <u><span style="color:blue">Quanto os valores variam?</span></u>
 - <u><span style="color:blue">Um país está acima ou abaixo da média?</span></u>

Essas métricas ajudam a entender **cada indicador isoladamente**.
Mas elas não respondem diretamente à pergunta: **Quais países são mais parecidos considerando todos os indicadores ao mesmo tempo?** Aqui surge uma mudança de perspectiva interessante. Em vez de pensar em cada indicador separadamente, podemos representar cada país como um **vetor de indicadores ESG**.

Para o nosso exemplo, vamos considerar o **ano de 2019** e o seguinte conjunto de indicadores para o Brasil:
- CO<sup>2</sup> per capita
- Energia renovável (%)
- Expectativa de vida ao nascer
- Mortalidade infantil
- Controle da corrupção
- Efetividade do governo

> **Nota:** O recorte temporal e os indicadores foram selecionados intencionalmente para ilustrar a abordagem analítica e demonstrar o processo de coleta, tratamento e integração de dados, não devendo ser interpretados como uma avaliação completa do desempenho ESG das nações consideradas.

Esse conjunto de dimensões forma, neste exemplo, um **vetor**. Cada país terá o mesmo conjunto de dimensões, que por sua vez compõe o seu próprio **vetor**. Isso nos leva a uma abordagem distinta: **medir a distância entre esses vetores**. Se dois países possuem vetores muito próximos, eles apresentam **perfis ESG semelhantes**. Quando a distância é maior, isso indica que seus perfis são mais diferentes.

Uma das formas mais simples de fazer isso é usar **distância euclidiana**, uma medida clássica em análise multivariada. Nesse caso, comparar países vira literalmente um problema de **geometria de dados**. Mas existe um detalhe importante: antes de calcular distâncias, os indicadores precisam ser **padronizados**, porque cada variável possui escala diferente (anos, toneladas, índices etc.).
Sem essa etapa, a comparação pode ficar completamente distorcida.

Essa abordagem levanta uma pergunta interessante: Talvez a discussão sobre ESG não devesse se limitar apenas a **quem está melhor no ranking**. Talvez também devêssemos perguntar: **quais países realmente se parecem entre si em termos de estrutura ESG?**



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
