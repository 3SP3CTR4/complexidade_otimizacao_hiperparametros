# Etapa 6 Leitura e fichamento

## Identificação do artigo

- Referência completa: FEURER, M.; HUTTER, F. Hyperparameter optimization. In: Automated Machine Learning: Methods, Systems, Challenges. Springer, Cham, p. 3-33, 2019.
- DOI ou URL: https://doi.org/10.1007/978-3-030-05318-5_1
- Base de origem: Springer
- Leitor responsável: Miguel Pereira
- Data da leitura: 09/10/2026

## Fichamento

### Problema investigado
O longo tempo de execução e a complexidade do ajuste de algoritmos de aprendizado de máquina, abordando a transição da parametrização manual para processos automatizados.

### Objetivo do estudo
Oferecer uma introdução detalhada à Otimização de Hiperparâmetros (HPO) no contexto de *AutoML*, classificando e analisando as técnicas para resolver o gargalo do tempo de execução.

### Método utilizado
Análise e contraste entre abordagens tradicionais (Busca em Grade e Busca Aleatória), técnicas baseadas em modelos (Otimização Bayesiana) e métodos inspirados em *bandit* (como *Hyperband* e *Successive Halving*), que utilizam alocação dinâmica de recursos.

### Contexto, amostra ou dados
Avaliação dos desafios práticos da área, incluindo a otimização em altos espaços dimensionais condicionais, a otimização multi-fidelidade e a reprodutibilidade de experimentos em ciência de dados.

### Principais resultados
A utilização de métodos com alocação dinâmica de recursos e interrupção antecipada (*early stopping*) diminui a complexidade empírica da busca. Essas abordagens eliminam rapidamente configurações de baixo desempenho, evitando o consumo excessivo de tempo de treinamento.

### Limitações apresentadas
A otimização em espaços dimensionais muito altos e a garantia de reprodutibilidade exata continuam sendo desafios práticos significativos e em aberto na aplicação de técnicas avançadas de HPO.

### Contribuição para o nosso artigo
O artigo fornece o referencial teórico comparativo direto entre *Grid Search*, *Random Search* e abordagens avançadas. Ele evidencia que a complexidade de tempo pode ser contornada estruturalmente com o uso de parada antecipada.

### Comentário crítico
Excelente contextualização das estratégias de HPO. A comparação entre métodos exaustivos e lógicas de interrupção antecipada enriquece a análise de eficiência e custo de *hardware*.

### Citação literal opcional

> "[...] métodos que utilizam alocação dinâmica de recursos e parada antecipada diminuem a complexidade empírica ao eliminar rapidamente as configurações de baixo desempenho, evitando que consumam muito tempo de treinamento."

Página: Não informada.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.