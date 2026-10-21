# Etapa 7: Matriz de Síntese e Cruzamento Bibliográfico

## Identificação
- **Grupo:** 6
- **Data da síntese:** 11/10/2026

## Matriz de Convergências e Divergências Assintóticas

Esta matriz consolida as métricas de complexidade computacional (Notação Big-O) e o comportamento empírico do *XGBoost* e dos métodos de busca, cruzando as evidências dos 8 artigos fichados.

| Artigo (Autor, Ano) | Foco Tecnológico | Complexidade de Tempo (Big-O) | Vantagem Identificada | Limitação Computacional / Espaço |
| :--- | :--- | :--- | :--- | :--- |
| **CHEN; GUESTRIN (2016)** | Arquitetura XGBoost | Otimizada via histogramas | Suporte *out-of-core* e paralelismo de hardware nativo. | Exige alto controle de cache para evitar gargalo de memória. |
| **BERGSTRA; BENGIO (2012)** | Random Search | Tempo linear $O(n)$ | Explora a baixa dimensão efetiva; não drena RAM excessiva. | Falta de heurística (sem memória de iterações passadas). |
| **SNOEK et al. (2012)** | Otimização Bayesiana | Tempo cúbico $O(n^3)$ | Reduz drasticamente as avaliações empíricas e o erro final. | Inversão analítica da matriz exige processamento multicore. |
| **SHAHRIARI et al. (2016)** | Otimização Bayesiana | Tempo cúbico $O(n^3)$ | Equilíbrio exato entre exploração e aproveitamento. | Peso algébrico inviabiliza iterações demasiadamente longas. |
| **PROBST et al. (2019)** | Tunabilidade | Redução de dimensão $d$ | Foca recursos apenas em parâmetros estruturais (ex: profundidade). | A sensibilidade precisa ser mapeada antes de iniciar a busca. |
| **FEURER; HUTTER (2019)** | HPO (AutoML) | Redução via heurística | Interrupção antecipada barra tempo inútil de processamento. | Complexidade para garantir reprodutibilidade exata do hardware. |
| **YANG; SHAMI (2020)** | Teoria vs. Prática | Dependente do método | Valida Bayes para espaços contínuos curtos e Random para massivos. | Explosão de RAM ao utilizar validação cruzada (K-Fold) pesada. |
| **BISCHL et al. (2023)** | Boas Práticas HPO | Gestão de orçamento | Formaliza regras de alocação dinâmica e fidelidade múltipla. | Modelar o custo oculto de latência em sistemas dinâmicos. |

## Síntese Crítica
O cruzamento revela o consenso literário de que o *Grid Search* possui custo exponencial inviável. A literatura converge para o uso do *Random Search* devido ao seu comportamento assintótico linear $O(n)$, enquanto a *Otimização Bayesiana*, apesar de reduzir o erro de predição do XGBoost, insere um gargalo cúbico $O(n^3)$ na álgebra do Processo Gaussiano.

## Contribuições

| Integrante | Atividade realizada | Contribuição |
| :--- | :--- | :---: |
| Aliana Sthefani | Cruzamento assintótico (Big-O) e elaboração da síntese crítica. | 35% |
| Luis Hardt | Estruturação comparativa dos métodos e identificação dos limites de espaço. | 35% |
| Bruna Alves de Jesus | Revisão cruzada entre matriz e fichamentos individuais. | 10% |
| Miguel Pereira | Validação da precisão das anotações de tempo ($O(n)$ e $O(n^3)$). | 10% |
| Guilherme Zanni | Conferência das autoriais e padronização dos anos de publicação. | 5% |
| Thales Eduardo | Formatação estética da tabela Markdown. | 5% |
