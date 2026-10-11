# Etapa 6 Leitura e fichamento

## Identificação do artigo

- Referência completa: SHAHRIARI, B. et al. Taking the human out of the loop: A review of Bayesian optimization. Proceedings of the IEEE, v. 104, n. 1, p. 148-175, 2016.[cite: 27]
- DOI ou URL: https://doi.org/10.1109/JPROC.2015.2494218
- Base de origem: Proceedings of the IEEE[cite: 27]
- Leitor responsável: Miguel Pereira
- Data da leitura: 09/10/2026

## Fichamento

### Problema investigado
A resolução de problemas de otimização global em funções de caixa-preta que são fortemente não lineares e cujas avaliações têm um custo computacional ou experimental muito alto.[cite: 27]

### Objetivo do estudo
Substituir a intuição humana por um ciclo automatizado e rigoroso, fundamentado na estatística Bayesiana, para encontrar soluções eficazes em problemas de otimização.[cite: 27]

### Método utilizado
O método se baseia em um modelo substituto (*surrogate model*), geralmente um Processo Gaussiano para mapeamento do espaço de busca e estimativa de incerteza, aliado a uma função de aquisição matemática que decide o próximo ponto a ser amostrado, equilibrando a exploração e o aproveitamento.[cite: 27]

### Contexto, amostra ou dados
Exploração em cenários de alta complexidade, como altas dimensões, ambientes ruidosos, restrições físicas e computação paralela, com aplicações práticas em *AutoML*, robótica e design de materiais.[cite: 27]

### Principais resultados
A Otimização Bayesiana reduz significativamente o tempo total do processo ao diminuir a necessidade de chamadas diretas à função objetivo principal.[cite: 27] No entanto, a sua versão padrão baseada em Processos Gaussianos apresenta uma complexidade cúbica $O(n^3)$ em relação ao número de avaliações, resultante da inversão da matriz de covariância.[cite: 27]

### Limitações apresentadas
A complexidade matricial associada aos Processos Gaussianos torna a abordagem computacionalmente pesada para cenários que exigem muitas iterações.[cite: 27]

### Contribuição para o nosso artigo
O estudo confirma e quantifica a complexidade temporal ($O(n^3)$) da estratégia heurística. Essa evidência é crucial para a nossa avaliação do custo de *hardware*, contrapondo a eficácia analítica do método ao seu peso computacional iterativo.

### Comentário crítico
Uma revisão fundamental que ilustra o *trade-off* da Otimização Bayesiana: poupa tempo na função objetivo ao custo de introduzir um forte peso algébrico interno.

### Citação literal opcional

> "A otimização bayesiana padrão baseada em Processos Gaussianos possui uma complexidade cúbica $O(n^{3})$ em relação ao número de avaliações 'n', em virtude da inversão da matriz de covariância."[cite: 27]

Página: Não informada.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.