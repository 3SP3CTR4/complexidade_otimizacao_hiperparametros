# Etapa 6 Leitura e fichamento

## Identificação do artigo

- Referência completa: YANG, L.; SHAMI, A. On hyperparameter optimization of machine learning algorithms: Theory and practice. Neurocomputing, v. 415, p. 295-316, 2020.
- DOI ou URL: https://doi.org/10.1016/j.neucom.2020.07.061
- Base de origem: Neurocomputing
- Leitor responsável: Bruna Alves de Jesus
- Data da leitura: 10/10/2026

## Fichamento

### Problema investigado
A dificuldade em adaptar e calibrar algoritmos de predição genéricos a problemas práticos, uma vez que o espaço de hiperparâmetros possui impacto direto no resultado, e o mapeamento dos limites computacionais das técnicas modernas estava demasiadamente fragmentado.

### Objetivo do estudo
Oferecer um roteiro técnico definitivo sobre algoritmos aplicados na otimização de hiperparâmetros, estruturando tanto as abordagens baseadas em gradiente e livres de modelo (como o *Grid* e *Random*) quanto estratégias bayesianas e metaheurísticas complexas baseadas em *bandit* (BOHB).

### Método utilizado
Classificação formal, revisão abrangente da teoria computacional das bibliotecas e, de forma fundamental, uma condução direta de benchmarks e experimentos empíricos com ambientes de alto custo.

### Contexto, amostra ou dados
Trabalhou-se em instâncias contínuas sobre bases de referência abertas para regressão e classificação, testando os limites assintóticos de *hardware* impostos pelo tempo computacional de execução versus precisão obtida.

### Principais resultados
Verificou-se que o tempo computacional das diferentes técnicas diverge agressivamente conforme a estrutura de cada metodologia. A escolha correta da técnica se torna o elemento determinante que viabiliza a solução analítica contra o alto custo das funções objetivo inseridas em espaços de busca com altíssima dimensionalidade.

### Limitações apresentadas
Entre os obstáculos operacionais persistentes, o risco da incapacidade de mitigar perfeitamente o *overfitting* de validação, os curtos orçamentos na avaliação algorítmica da função e o desafio de escalar as bibliotecas abertas para sistemas dinâmicos.

### Contribuição para o nosso artigo
Serve como o laboratório definitivo para as nossas conclusões de pesquisa. As avaliações de tempo computacional entre o Bayes e o *Random Search* executadas pelos autores sustentam o nosso desenvolvimento teórico no contexto de eficiência e complexidade em *hardware*.

### Comentário crítico
Excelente equilíbrio entre o formalismo matemático exigido pela academia e a aplicação prática necessária para cientistas e analistas, alinhando de maneira perfeita as três correntes metodológicas avaliadas em nosso projeto (*Grid*, *Random* e *Bayesiana*).

### Citação literal opcional

> "O estudo também cataloga diversas bibliotecas e frameworks de código aberto em Python para uso prático e conduz experimentos empíricos com conjuntos de dados de referência para comparar a eficácia e o tempo computacional das diferentes técnicas."

Página: Não informada.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.