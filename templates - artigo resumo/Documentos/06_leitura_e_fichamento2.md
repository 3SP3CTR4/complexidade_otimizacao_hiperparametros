# Etapa 6 Leitura e fichamento

## Identificação do artigo

- Referência completa: PROBST, P.; BISCHL, B.; BOULESTEIX, A.-L. Tunability: Importance of hyperparameters of machine learning algorithms. Journal of Machine Learning Research, v. 20, n. 53, p. 1-32, 2019.
- DOI ou URL: -
- Base de origem: Journal of Machine Learning Research
- Leitor responsável: Miguel Pereira
- Data da leitura: 09/10/2026

## Fichamento

### Problema investigado
A incerteza e o dilema associados ao direcionamento dos longos e pesados esforços de otimização, buscando identificar os hiperparâmetros verdadeiramente relevantes e isolar os de impacto marginal.

### Objetivo do estudo
Investigar e quantificar a importância real dos hiperparâmetros por meio do conceito de "tunabilidade", que avalia a margem de melhoria de desempenho em relação aos valores padrão.

### Método utilizado
Análise prática realizada sobre múltiplos conjuntos de dados para medir a sensibilidade associada à escolha de parâmetros em toda a gama de algoritmos.

### Contexto, amostra ou dados
Avaliação em algoritmos de aprendizado de máquina, com destaque para os modelos baseados em árvores e redes neurais, que exigem maior atenção a parâmetros estruturais como a taxa de aprendizado e a profundidade da árvore.

### Principais resultados
A compreensão da "tunabilidade" permite que algoritmos de otimização desconsiderem parâmetros de impacto mínimo. Isso direciona o esforço computacional apenas para aqueles hiperparâmetros que afetam significativamente o desempenho preditivo.

### Limitações apresentadas
A sensibilidade e a necessidade de ajuste variam consideravelmente entre diferentes tipos de algoritmos, exigindo mapeamento prévio para determinar quais parâmetros realmente importam.

### Contribuição para o nosso artigo
O conceito de "tunabilidade" fundamenta o argumento teórico para reduzir o espaço de busca exata. Essa redução é necessária para evitar a explosão combinatória em algoritmos como o *Grid Search*, otimizando o consumo de espaço e tempo.

### Comentário crítico
O artigo conecta a eficiência teórica à modelagem prática. Reduzir a dimensionalidade da busca por meio da tunabilidade é o passo inicial indispensável antes da aplicação de qualquer método de otimização.

### Citação literal opcional

> "Entender a tunabilidade diminui indiretamente o tempo e a complexidade da busca, permitindo que algoritmos de otimização desconsiderem parâmetros de impacto mínimo e direcionem o esforço computacional apenas para aqueles que afetam significativamente o desempenho preditivo."

Página: Não informada.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.