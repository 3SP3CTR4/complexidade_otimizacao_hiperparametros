# Etapa 6 Leitura e fichamento

## Identificação do artigo

- Referência completa: SNOEK, J.; LAROCHELLE, H.; ADAMS, R. P. Practical Bayesian optimization of machine learning algorithms. In: ADVANCES IN NEURAL INFORMATION PROCESSING SYSTEMS, 25., 2012. Proceedings [...]. [S. l.: s. n.], 2012.
- DOI ou URL: https://proceedings.neurips.cc/paper/2012/hash/05311655a15b75fab86956663e1819cd-Abstract.html
- Base de origem: NIPS
- Leitor responsável: Bruna Alves de Jesus
- Data da leitura: 10/10/2026

## Fichamento

### Problema investigado
A abordagem imprecisa e cega do ajuste de hiperparâmetros, que exigia dependência empírica humana ou buscas por força bruta de custo extremo, diante de funções de desempenho instáveis com custos de tempo de execução variáveis ou totalmente desconhecidos.

### Objetivo do estudo
Demonstrar a viabilidade e a superioridade estatística da Otimização Bayesiana, substituindo tentativas e erros por um modelo substituto robusto que modela o desempenho de generalização através de um Processo Gaussiano.

### Método utilizado
Engenharia de algoritmos com abordagens totalmente bayesianas para a avaliação dos hiperparâmetros (como *slice sampling* e integração do modelo Matérn 5/2 com ARD). Os algoritmos também foram modificados para inferir os custos de tempo ocultos via "melhoria esperada por segundo".

### Contexto, amostra ou dados
Trabalho baseado em experimentos com arquiteturas algorítmicas de alto nível de processamento matricial que exigem limites exaustivos da capacidade de avaliação computacional em grade, como classificadores estruturados.

### Principais resultados
A otimização Bayesiana, ao marginalizar os hiperparâmetros internamente e adaptar-se ao custo da execução computacional por unidade de segundo, obteve melhorias que superaram o estado da arte e a otimização empírica de humanos. Reduziu simultaneamente o tempo necessário para treinar e o número absoluto de avaliações, se comparada ao *Grid Search* tradicional.

### Limitações apresentadas
Apesar de conseguir reduzir o tempo de chamadas primárias via estimativas independentes e paralelismo multicore (via aproximação por Monte Carlo), a estrutura matemática pesada do núcleo ainda impõe restrições ao número excessivo de iterações puras.

### Contribuição para o nosso artigo
O artigo traz os fundamentos analíticos de compensação entre tempo de modelo e tempo de aquisição Bayesiana. É vital para provar como a paralelização por aproximações de Monte Carlo amortece o forte crescimento do *hardware* exigido na formulação bayesiana padrão, tornando-a viável ao cruzar parâmetros difíceis do *XGBoost*.

### Comentário crítico
Trabalho irretocável que mostra como o rigor analítico consegue resolver ambiguidades práticas. As estratégias de cálculo por *threads* simultâneas abrem caminho para a viabilização matemática moderna da otimização Bayesiana sob restrições técnicas.

### Citação literal opcional

> "A otimização bayesiana com marginalização de hiperparâmetros e paralelização reduz significativamente o tempo necessário e o número de avaliações comparativamente às pesquisas em grelha tradicionais."

Página: Não informada.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.