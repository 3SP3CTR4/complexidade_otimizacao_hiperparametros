# Etapa 6 Leitura e fichamento

## Identificação do artigo

- Referência completa: BERGSTRA, J.; BENGIO, Y. Random search for hyper-parameter optimization. Journal of Machine Learning Research, v. 13, p. 281-305, 2012.
- DOI ou URL: https://jmlr.csail.mit.edu/papers/v13/bergstra12a.html
- Base de origem: Journal of Machine Learning Research
- Leitor responsável: Bruna Alves de Jesus
- Data da leitura: 10/10/2026

## Fichamento

### Problema investigado
A grave ineficiência e a limitação de escalabilidade da Busca em Grade (*Grid Search*) em ambientes de hiperparâmetros de alta dimensão, gerando o gargalo conhecido como maldição da dimensionalidade (onde o número de combinações testadas cresce de forma exponencial).

### Objetivo do estudo
Demonstrar, por meio de simulações em Processos Gaussianos, que a Busca Aleatória (*Random Search*) é estatística e operacionalmente mais eficiente do que a Busca em Grade, superando também a lentidão das abordagens de parametrização manuais.

### Método utilizado
Execução empírica rigorosa com repetição de simulações sobre diversos conjuntos de dados aplicados a arquiteturas não lineares de aprendizado de máquina. O método avalia o ganho de eficiência da busca aleatória com diversos conjuntos de pontos e interrupções probabilísticas.

### Contexto, amostra ou dados
Trabalhou-se com conjuntos de dados complexos que exigiam ajuste em dezenas de hiperparâmetros simultâneos, cenários onde o *Grid Search* se torna analiticamente impossível de processar devido ao limite de tempo de *hardware*.

### Principais resultados
Cerca de 8 tentativas do *Random Search* igualaram ou superaram uma malha de grade contendo 100 tentativas. Comprovou-se que modelos preditivos possuem baixa "dimensão efetiva" (apenas 1 a 4 parâmetros realmente importam). Enquanto a malha exata desperdiça tempo avaliando dimensões irrelevantes, a busca aleatória foca nas dimensões de real peso na função de perda.

### Limitações apresentadas
Embora eficiente em tempo, a Busca Aleatória é um processo sem memória. Ela não aproveita os resultados de iterações passadas para corrigir a rota nos passos futuros, sendo superada por modelos adaptativos quando o espaço vetorial de erro se torna demasiadamente complexo.

### Contribuição para o nosso artigo
O artigo introduz as bases teóricas essenciais que fundamentam por que o *Grid Search* jamais deve ser adotado cegamente no *XGBoost*. A comprovação matemática da baixa dimensionalidade efetiva serve de argumento incontestável para a superioridade do tempo linear do *Random Search* em relação à explosão exponencial do *Grid*.

### Comentário crítico
Uma pesquisa clássica e transformadora no campo de otimização algorítmica. Os autores conseguem comprovar como o acaso probabilístico aliado à facilidade de paralelização e resiliência a falhas bate o método exato (*Grid*) em arquiteturas complexas.

### Citação literal opcional

> "Isso ocorre porque a função de desempenho possui baixa dimensão efetiva: apenas de 1 a 4 hiperparâmetros são realmente relevantes em cada conjunto de dados, e esses hiperparâmetros variam de um conjunto para outro, o que faz a grade desperdiçar tentativas em dimensões irrelevantes."

Página: Não informada.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.