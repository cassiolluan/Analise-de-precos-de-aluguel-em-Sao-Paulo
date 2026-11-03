# README

# Desafio SYNAPTA

# Análise de preços de aluguel em São Paulo

**Autor**: Cássio Luan de Oliveira Santos 

***2º Período Ciência da Computação***

Projeto desenvolvido para a etapa de desafio da **SYNAPTA 2026 – UNINASSAU Maceió**.

A ideia deste projeto foi analisar uma base de imóveis para entender melhor os preços de aluguel em São Paulo e verificar se algumas características dos imóveis, como área, quantidade de quartos e garagens, têm relação com o valor anunciado.

## Sobre os dados

A base utilizada contém informações de imóveis para aluguel em São Paulo.

Algumas das informações disponíveis são:

- área do imóvel;
- quantidade de quartos;
- quantidade de garagens;
- valor do aluguel;
- valor total;
- distrito/localização.

O arquivo utilizado na análise é o `dataframe.csv`.

**Fonte dos dados:**

[https://www.kaggle.com/datasets/renatosn/sao-paulo-housing-prices](https://www.kaggle.com/datasets/renatosn/sao-paulo-housing-prices)

## O que foi analisado

Primeiro, fiz uma verificação geral da base para entender como os dados estavam organizados.

Foram verificadas:

- quantidade de linhas e colunas;
- nomes das colunas;
- tipos dos dados;
- valores ausentes;
- registros duplicados;
- valores mínimos e máximos;
- quantidade de registros por distrito;
- possíveis valores inconsistentes.

Durante essa etapa, encontrei **2 imóveis com área igual a zero**. Como esse valor não faz sentido para uma análise que utiliza a área do imóvel, esses registros foram mantidos na base original, mas não foram utilizados nos cálculos relacionados à área.

## Média e mediana

O valor médio dos aluguéis encontrados foi de aproximadamente **R$ 3.250,81**.

Já a mediana foi de **R$ 2.415,00**.

A diferença acontece principalmente porque existem imóveis com valores de aluguel bem mais altos. Esses valores acabam aumentando a média. A mediana sofre menos influência desses valores extremos e, por isso, ajuda a ter uma ideia melhor do valor que está mais próximo do centro da distribuição.

## Comparação entre os distritos

Para evitar que distritos com poucos anúncios distorcessem a comparação, foram considerados apenas aqueles que possuíam **pelo menos 30 registros**.

Os cinco distritos com maiores médias de aluguel foram:

1. Jardim Leonor
2. Tamboré
3. Cerqueira César
4. Jardim Paulista
5. Paraíso

Entre os distritos analisados, **Jardim Leonor apresentou a maior média**.

Entre os menores valores médios apareceram:

- Taboão;
- Sé;
- Campos Elíseos;
- Santa Efigênia;
- Vila Ema.

## Relação com as características dos imóveis

Também comparei o preço do aluguel com algumas características dos imóveis.

Os valores de correlação encontrados foram:

| Característica | Correlação com o aluguel |
| --- | --- |
| Área | 0,67 |
| Garagem | 0,62 |
| Quartos | 0,53 |

A área apresentou a maior correlação entre as características analisadas. Isso indica que, nesta base, imóveis maiores tendem a apresentar aluguéis maiores.

A quantidade de garagens também apresentou uma relação positiva com o aluguel, assim como a quantidade de quartos.

Esses valores mostram uma relação entre as variáveis, mas não significam que uma característica sozinha seja responsável pelo preço do imóvel.

## Gráficos

Foram utilizados três gráficos principais:

- relação entre área e preço do aluguel;
- relação entre quantidade de quartos e preço do aluguel;
- distritos com maiores preços médios.

Os gráficos estão disponíveis no notebook principal do projeto.

## Principais conclusões

Com a análise realizada, foi possível observar que:

1. O valor médio dos aluguéis foi maior que a mediana, indicando influência de imóveis com preços mais altos.
2. A área foi a característica que apresentou maior correlação com o preço do aluguel entre as analisadas.
3. A quantidade de garagens também apresentou uma relação positiva com o valor do aluguel.
4. Imóveis com mais quartos tendem a apresentar valores maiores, embora existam diferenças entre os imóveis.
5. Existem diferenças consideráveis entre as médias de aluguel dos distritos analisados.
6. Jardim Leonor apresentou a maior média de aluguel entre os distritos com pelo menos 30 registros.
7. A relação observada entre as características e o preço não permite afirmar que uma delas seja, sozinha, a causa do aumento do aluguel.

## Limitações

Alguns pontos precisam ser considerados ao interpretar os resultados.

Os valores presentes na base são **preços anunciados**, então não é possível afirmar que sejam exatamente os valores que foram negociados entre proprietário e locatário.

Também existe uma diferença grande na quantidade de anúncios entre os distritos. Por isso, foi utilizado o mínimo de 30 registros para fazer a comparação das médias.

Além disso, a base possui apenas algumas características dos imóveis. Outros fatores que podem influenciar o preço do aluguel não estão disponíveis nos dados analisados.

Também foram encontrados dois registros com área igual a zero, que não foram utilizados nas análises envolvendo essa variável.

Por fim, correlação não significa causalidade. Os resultados mostram relações entre as variáveis, mas não permitem afirmar que uma determinada característica seja a causa direta de um aluguel mais caro ou mais barato.

## Como executar

Para reproduzir a análise, é necessário ter o Python instalado e as bibliotecas utilizadas no projeto.

Depois de baixar o projeto, deixe o arquivo `dataframe.csv` na mesma pasta do notebook e abra o arquivo principal no Jupyter Notebook ou no VS Code.

As bibliotecas utilizadas foram:

- Pandas
- NumPy
- Matplotlib

Caso seja necessário instalar as bibliotecas:

```bash
pip install pandas numpy matplotlib
```

## Arquivos do projeto

```
projeto-synapta/
│
├── dataframe.csv
├── projeto_synapta.ipynb
├── README.md
└── requirements.txt
```

## Uso de inteligência artificial

Durante a criação do projeto, utilizei inteligência artificial para tirar dúvidas sobre a linguagem utilizada (Python), organização da análise e interpretação de alguns conceitos.

As respostas e os códigos utilizados foram conferidos e adaptados de acordo com os resultados obtidos diretamente na base de dados.

A análise, os resultados apresentados e as conclusões foram revisados antes da entrega.