# Etapa 8 Redação do artigo

## Solicitação

Escreva a primeira versão completa do artigo seguindo a estrutura abaixo.

# Título

ANÁLISE DA COMPLEXIDADE COMPUTACIONAL DAS ESTRATÉGIAS DE OTIMIZAÇÃO DE HIPERPARÂMETROS NO XGBOOST

## Palavras-chave

Otimização de Hiperparâmetros; Complexidade Computacional; XGBoost.

## Introdução

Os algoritmos de aprendizado de máquina baseados no impulsionamento de gradiente em árvores marcam o atual estado da arte para predições estruturadas. O *XGBoost*, apresentado por Chen e Guestrin (2016), consolidou-se pela sua extrema precisão e escalabilidade em dados tabulares. Contudo, o alcance do pico de desempenho preditivo é invariavelmente condicionado ao ajuste fino de seus hiperparâmetros. Esse processo formal de Otimização de Hiperparâmetros (HPO) exige uma carga massiva de processamento, configurando um severo gargalo prático em ambientes restritos, um desafio amplamente mapeado na literatura de automação por Bischl et al. (2023). 

O problema central desta pesquisa reside no fato de que, frequentemente, a alta complexidade assintótica das técnicas de busca é negligenciada em prol de ganhos puramente preditivos, ocasionando interrupções por falta de memória (RAM) e tempos de execução computacionalmente impraticáveis. A justificativa para este estudo ancora-se na necessidade de aliar o poder estatístico dos modelos à viabilidade arquitetural das máquinas, evitando o colapso do *hardware* durante as fases de treinamento. O objetivo deste artigo é analisar a complexidade de tempo (Notação *Big-O*) e o consumo de espaço dinâmico das três principais formas de HPO: Busca em Grade (*Grid Search*), Busca Aleatória (*Random Search*) e Otimização Bayesiana, aplicadas sob a estrutura do XGBoost.

## Metodologia

Realizou-se uma revisão bibliográfica sistemática de viés qualitativo, avaliando provas matemáticas e experimentos empíricos. As bases de dados consultadas foram IEEE Xplore, ACM Digital Library e Scopus/CAPES. A estratégia de busca utilizou os descritores "Hyperparameter Optimization" AND "Computational Complexity" AND "XGBoost". O período de análise priorizou a literatura contemporânea (2019 a 2026), resgatando os artigos seminais e basilares a partir de 2012. Como critérios de inclusão, selecionaram-se estudos de alto impacto com foco na notação assintótica matemática de *hardware*. Excluíram-se taxativamente artigos cujo foco estivesse na aplicação de redes neurais profundas (*Deep Learning*). A triagem resultou em 8 estudos definitivos, e a análise deu-se mediante o cruzamento das matrizes de custo e tempo computacional.

## Revisão da literatura

### Eixo 1: A Maldição da Dimensionalidade e a Eficiência Estocástica (Grid vs. Random Search)

A Busca em Grade, embora seja o método de implementação mais trivial, sofre de forma letal com a chamada "maldição da dimensionalidade". A literatura demonstra que a técnica eleva o tempo de processamento de modo exponencial, crescendo assintoticamente em $O(k^d)$, esgotando rapidamente os recursos do *hardware* ao avaliar exaustivamente variáveis que possuem impacto irrelevante no modelo. Para mitigar esse custo irracional de processamento iterativo, Probst, Bischl e Boulesteix (2019) propõem focar na métrica de "tunabilidade", forçando a restrição do espaço de busca exclusivamente aos parâmetros de estrutura de árvore que realmente alteram a função de perda.

Em franco contraste a este modelo arcaico, Bergstra e Bengio (2012) provaram a tese da "baixa dimensão efetiva". Eles demonstraram matematicamente que apenas uma pequena fração do vetor de parâmetros altera significativamente o erro base. A Busca Aleatória se aproveita desse fenômeno: operando de forma autônoma, atinge convergência em um tempo quase linear ($O(n)$) e permite extrema facilidade de paralelização, superando o modelo de Grade sem o risco do travamento de memória.

### Eixo 2: O Custo Algébrico da Otimização Bayesiana

Ao invés de contar com a força bruta ou a aleatoriedade estocástica, a Otimização Bayesiana constrói um modelo probabilístico substituto, guiado via Processos Gaussianos. Snoek, Larochelle e Adams (2012) validaram que este método prevê com extrema exatidão as coordenadas mais promissoras da função, quebrando radicalmente a necessidade de longas avaliações cegas e melhorando drasticamente as métricas do modelo treinado. 

Entretanto, esse poder analítico cobra um altíssimo preço em *hardware*. Shahriari et al. (2016) atestam que a técnica Bayesiana embute um motor algébrico que requer, invariavelmente, a inversão analítica da matriz de covariância a cada novo passo da busca. Isso confere ao algoritmo uma duríssima complexidade de tempo cúbica ($O(n^3)$). Consequentemente, para espaços hiperparamétricos largos e numerosas interações, o próprio agente otimizador consome mais memória ram e *threads* do que o treinamento da árvore do XGBoost em si.

### Síntese crítica

O cruzamento bibliográfico revela uma forte convergência metodológica: a rejeição absoluta da Busca em Grade para cenários complexos (YANG; SHAMI, 2020). Há, todavia, um abismo no emprego das técnicas substitutas. O método Bayesiano consolida-se como superior na minimização do erro e na otimização da predição, mas diverge gravemente no consumo de recursos internos, limitando-se a espaços contínuos e amostragens curtas. Como lacuna central e tendência futura, evidencia-se a urgência apontada por Feurer e Hutter (2019) de que qualquer técnica adotada deve possuir métodos estritos de "parada antecipada" (*early stopping*) e alocação dinâmica de recursos computacionais para sobreviver na nuvem.

## Considerações finais

Em resposta ao problema proposto, a escolha de uma estratégia de otimização de hiperparâmetros no XGBoost transcende a mera necessidade de maximizar a acurácia de predição; ela é ditada fundamentalmente pela arquitetura do *hardware* disponível. Os achados confirmam que a Busca Aleatória é o mecanismo ideal para conjuntos maciços e de alta dimensionalidade em virtude do seu tempo linear e de sua capacidade ilimitada de paralelismo em rede. 

Por sua vez, a Otimização Bayesiana detém o estado da arte na resolução da função objetivo, mas está estritamente limitada ao gargalo de sua complexidade matricial cúbica. Recomenda-se que cientistas de dados não adotem abordagens cegas, equilibrando matematicamente os limites de sua memória RAM e CPU ao orçamento de tempo viável para o treinamento de rotinas analíticas estruturadas.

## Resumo

Os algoritmos de aprendizado baseados em árvores, como o XGBoost, são fundamentais em dados tabulares, mas o ajuste de hiperparâmetros gera um alto gargalo em hardware limitado (CHEN; GUESTRIN, 2016; BISCHL et al., 2023). O objetivo foi analisar a complexidade de tempo e espaço da Busca em Grade, Aleatória e Otimização Bayesiana. Realizou-se uma revisão sistemática focada no custo assintótico (*Big-O*), triando 8 artigos essenciais. Os resultados indicam que a Busca em Grade sofre com o tempo exponencial incomputável, a Busca Aleatória opera eficientemente de forma linear explorando a baixa dimensão efetiva (BERGSTRA; BENGIO, 2012), enquanto a Bayesiana reduz avaliações do modelo, mas embute um peso cúbico restritivo via inversão de matrizes (SHAHRIARI et al., 2016). Conclui-se que o rigor de *hardware* dita a escolha do método analítico ideal.

## Referências

BERGSTRA, J.; BENGIO, Y. Random search for hyper-parameter optimization. Journal of Machine Learning Research, v. 13, p. 281-305, 2012.

BISCHL, B. et al. Hyperparameter optimization: Foundations, algorithms, best practices, and open challenges. WIREs Data Mining and Knowledge Discovery, v. 13, n. 2, e1484, 2023.

CHEN, T.; GUESTRIN, C. XGBoost: A scalable tree boosting system. In: ACM SIGKDD INTERNATIONAL CONFERENCE ON KNOWLEDGE DISCOVERY AND DATA MINING, 22., 2016, São Francisco. Proceedings [...]. [S. l.: s. n.], 2016. p. 785-794.

FEURER, M.; HUTTER, F. Hyperparameter optimization. In: Automated Machine Learning: Methods, Systems, Challenges. Springer, Cham, p. 3-33, 2019.

PROBST, P.; BISCHL, B.; BOULESTEIX, A.-L. Tunability: Importance of hyperparameters of machine learning algorithms. Journal of Machine Learning Research, v. 20, n. 53, p. 1-32, 2019.

SHAHRIARI, B. et al. Taking the human out of the loop: A review of Bayesian optimization. Proceedings of the IEEE, v. 104, n. 1, p. 148-175, 2016.

SNOEK, J.; LAROCHELLE, H.; ADAMS, R. P. Practical Bayesian optimization of machine learning algorithms. In: ADVANCES IN NEURAL INFORMATION PROCESSING SYSTEMS, 25., 2012. Proceedings [...]. [S. l.: s. n.], 2012.

YANG, L.; SHAMI, A. On hyperparameter optimization of machine learning algorithms: Theory and practice. Neurocomputing, v. 415, p. 295-316, 2020.

## Checklist

- [x] A introdução termina com o objetivo.
- [x] A metodologia descreve o processo realmente realizado.
- [x] A revisão compara os artigos.
- [x] A conclusão responde ao problema.
- [x] O resumo representa o texto completo.

## Contribuições

| Integrante | Atividade realizada no projeto | Contribuição |
| :--- | :--- | :---: |
| Aliana Sthefani | Redação do documento final, síntese teórica e formatação geral. | 25% |
| Luis Hardt | Estruturação da matriz assintótica e redação metodológica. | 25% |
| Bruna Alves de Jesus | Leitura, triagem e redação de 4 fichamentos bibliográficos estruturais. | 20% |
| Miguel Pereira | Leitura, triagem e redação de 4 fichamentos bibliográficos estruturais. | 20% |
| Guilherme Zanni | Revisão ortográfica, gramatical e padronização da equipa. | 5% |
| Thales Eduardo | Formatação de tabelas, cabeçalhos e referências em ordem alfabética. | 5% |
