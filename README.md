# Análise comparativa de desempenho de quatro lojas

Projeto de análise exploratória de dados desenvolvido em Python com Pandas, Matplotlib, Seaborn e Folium. O objetivo é comparar indicadores de quatro lojas e apresentar evidências que apoiem uma decisão comercial.

> **Status:** projeto de portfólio em revisão. Os dados utilizados são os arquivos públicos do desafio de Data Science da Alura.

## Pergunta de negócio

Considerando o valor total registrado, a satisfação dos clientes e o custo médio de frete, qual loja apresenta os resultados mais interessantes? A resposta depende do critério de decisão: não existe uma vencedora absoluta em todos os indicadores.

## Fonte dos dados

Os quatro arquivos CSV são disponibilizados no repositório público do desafio:

- [Loja 1](https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_1.csv)
- [Loja 2](https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_2.csv)
- [Loja 3](https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_3.csv)
- [Loja 4](https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_4.csv)

Cada registro contém produto, categoria, preço, frete, data da compra, vendedor, local da compra, avaliação, forma de pagamento, parcelas e coordenadas geográficas.

## Ferramentas

- Python
- Pandas
- Matplotlib
- Seaborn
- Folium
- Jupyter Notebook / Google Colab

## Indicadores apurados

A leitura dos quatro arquivos retornou 9.435 registros no total. Os valores abaixo foram calculados diretamente dos CSVs disponibilizados pela fonte.

| Loja | Registros | Soma dos preços registrados | Avaliação média (0–5) | Frete médio |
|---|---:|---:|---:|---:|
| Loja 1 | 2.359 | R$ 1.534.509,12 | 3,98 | R$ 34,69 |
| Loja 2 | 2.359 | R$ 1.488.459,06 | 4,04 | R$ 33,62 |
| Loja 3 | 2.359 | R$ 1.464.025,03 | 4,05 | R$ 33,07 |
| Loja 4 | 2.358 | R$ 1.384.497,58 | 4,00 | R$ 31,28 |

**Leitura inicial:**
- A Loja 1 tem a maior soma dos preços registrados.
- A Loja 3 apresenta a maior avaliação média.
- A Loja 4 tem o menor frete médio.
- Nenhuma loja lidera simultaneamente os três indicadores.

## Análises realizadas no notebook

1. Comparação da soma dos preços registrados por loja.
2. Distribuição de registros por categoria.
3. Avaliação média dos clientes.
4. Produtos com maior e menor frequência de registros.
5. Comparação do frete médio.
6. Distribuição geográfica dos registros e visualizações exploratórias com latitude e longitude.

## Conclusão responsável

Os indicadores mostram resultados distintos: a Loja 1 lidera na soma dos preços registrados, enquanto a Loja 3 tem a melhor avaliação média e a Loja 4 apresenta o menor frete médio.

Por isso, a recomendação comercial deve considerar qual objetivo tem maior peso — retorno financeiro, satisfação ou custo logístico. Com os indicadores isolados, não é correto afirmar que uma única loja é a melhor em todos os aspectos.

## Limitações da análise

- A base não apresenta uma coluna explícita de quantidade vendida. Assim, a frequência de registros por produto ou categoria não deve ser interpretada como quantidade de unidades vendidas.
- A soma da coluna `Preço` é apresentada como soma dos preços registrados; sua interpretação como faturamento depende da granularidade e das regras da base.
- A análise geográfica descreve a distribuição das coordenadas. Latitude e longitude, isoladamente, não permitem concluir poder aquisitivo regional nem estabelecer causalidade entre localização, avaliação e faturamento.
- Os resultados dependem dos arquivos públicos da fonte e podem mudar caso a base seja atualizada.

## Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/thalissakezia/analise-lojas-vendas.git
   cd analise-lojas-vendas
   ```
2. Abra `AluraStoreBr.ipynb` no Jupyter Notebook ou Google Colab.
3. Execute as células em ordem. O notebook carrega os CSVs diretamente das URLs da fonte.

## Estrutura

- `AluraStoreBr.ipynb`: notebook com carregamento, exploração, visualizações e análise comparativa.

## Próximas melhorias

- Organizar o notebook em etapas reproduzíveis, com funções reutilizáveis.
- Validar dados ausentes, tipos, duplicidades e consistência das colunas.
- Padronizar os indicadores e explicitar suas fórmulas.
- Acrescentar gráficos comparativos consolidados e uma síntese executiva.
- Registrar as versões das bibliotecas e instruções de execução.

---
Projeto de portfólio — análise exploratória de dados.
