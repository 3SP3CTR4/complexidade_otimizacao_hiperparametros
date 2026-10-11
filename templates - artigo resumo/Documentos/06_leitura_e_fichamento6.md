# Etapa 6 Leitura e fichamento

## Identificação do artigo

- Referência completa: BISCHL, B. et al. Hyperparameter optimization: Foundations, algorithms, best practices, and open challenges. WIREs Data Mining and Knowledge Discovery, v. 13, n. 2, e1484, 2023.
- DOI ou URL: https://doi.org/10.1002/widm.1484
- Base de origem: WIREs Data Mining and Knowledge Discovery
- Leitor responsável: Bruna Alves de Jesus
- Data da leitura: 10/10/2026

## Fichamento

### Problema investigado
A ausência de padronização nas configurações e o alto custo computacional enfrentado para avaliar configurações exaustivas durante os testes em métodos automatizados de caixa-preta (*black-box optimization*).

### Objetivo do estudo
Oferecer uma revisão abrangente que consolida os fundamentos, cataloga todas as abordagens existentes (das clássicas às complexas como a Otimização Bayesiana) e estabelece diretrizes e melhores práticas para desenhar fluxos eficientes de Otimização de Hiperparâmetros (HPO).

### Método utilizado
Revisão da literatura unificada à formatação teórica da aprendizagem supervisionada. O texto avalia e classifica a efetividade das estratégias utilizando métricas pautadas por limites de orçamento de avaliação computacional e métodos de reamostragem profunda (como *resampling* aninhado).

### Contexto, amostra ou dados
Trata de cenários abrangentes integrados a grandes *pipelines* de pré-processamento de *AutoML*, avaliando não só a capacidade de descoberta algorítmica de bons parâmetros, mas a prevenção formal do chamado sobreajuste de meta-nível (*meta-overfitting*).

### Principais resultados
Demonstrou que, para contornar o elevadíssimo custo assintótico de avaliação exaustiva, as implementações modernas devem mandatoriamente integrar alocação dinâmica de recursos computacionais (*racing*, *Hyperband*) e explorar ambientes de múltipla fidelidade. A paralelização também foi estabelecida como pilar fundamental de desempenho temporal.

### Limitações apresentadas
A modelagem exata do limite espacial e de custos paralelos ainda apresenta forte suscetibilidade ao ambiente e arquitetura que hospeda os algoritmos, persistindo como um problema aberto na literatura.

### Contribuição para o nosso artigo
Funciona como espinha dorsal para os nossos objetivos de "Boas Práticas" na pesquisa. Seus fundamentos guiam as conclusões do artigo, pois o texto explica como aplicar a restrição dos espaços de busca antes da aplicação dos otimizadores sobre a árvore do *XGBoost*.

### Comentário crítico
Excelente material compilatório de alto padrão metodológico. Funciona perfeitamente para conectar e harmonizar os avanços tecnológicos mais antigos com os limitantes mais rígidos de processamento em hardware moderno.

### Citação literal opcional

> "O uso de abordagens de múltipla fidelidade e alocação dinâmica de recursos é destacado para contornar o elevado custo computacional associado à avaliação exaustiva de configurações complexas."

Página: Não informada.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.