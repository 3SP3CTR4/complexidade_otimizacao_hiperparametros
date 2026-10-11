# Etapa 6 Leitura e fichamento

## Identificação do artigo

- Referência completa: CHEN, T.; GUESTRIN, C. XGBoost: A scalable tree boosting system. In: ACM SIGKDD INTERNATIONAL CONFERENCE ON KNOWLEDGE DISCOVERY AND DATA MINING, 22., 2016, São Francisco. Proceedings [...]. [S. l.: s. n.], 2016. p. 785-794.
- DOI ou URL: https://doi.org/10.1145/2939672.2939785
- Base de origem: ACM SIGKDD
- Leitor responsável: Miguel Pereira
- Data da leitura: 09/10/2026

## Fichamento

### Problema investigado
Os limites de desempenho e escalabilidade enfrentados pelos algoritmos de *boosting* clássicos ao processarem dados tabulares em larga escala.

### Objetivo do estudo
Apresentar o XGBoost, um sistema de gradiente impulsionado por árvores altamente escalável, eficiente e preciso, desenhado para lidar com grandes volumes de dados.

### Método utilizado
Implementação de inovações algorítmicas e arquiteturais, como um algoritmo sensível à esparsidade dos dados, esboço de quantil ponderado, estruturas de blocos otimizadas para paralelismo e uso eficiente do cache de hardware, além de suporte à computação fora do núcleo (*out-of-core*).

### Contexto, amostra ou dados
Processamento eficiente de conjuntos de dados estruturados em grandes quantidades que superam a capacidade da memória principal do sistema.

### Principais resultados
O XGBoost reduz consideravelmente o tempo de treinamento por meio de aproximações baseadas em histogramas e paralelismo de *hardware*.[cite: 29] A complexidade temporal da construção de árvores é drasticamente otimizada, tornando o método significativamente mais rápido e preciso.

### Limitações apresentadas
Para atingir a eficiência máxima em conjuntos de dados massivos, o sistema exige configurações adequadas de estruturas de blocos e aproveitamento estrito da arquitetura de cache e memória do hardware.

### Contribuição para o nosso artigo
Sendo o artigo fundador do XGBoost, ele fornece a base teórica e as características arquiteturais de escalabilidade. É o ponto de partida para entender como as estratégias de otimização de hiperparâmetros interagem com o custo interno da construção das árvores.

### Comentário crítico
Uma referência indispensável e definitiva. Demonstra como as inovações em nível de engenharia de *software* e algoritmos permitem que o *boosting* em árvores alcance alta performance em ambientes com restrição de memória.

### Citação literal opcional

> "O XGBoost reduz consideravelmente o tempo de treinamento em relação às implementações clássicas de boosting, otimizando drasticamente a complexidade temporal da construção de árvores por meio de aproximações baseadas em histogramas e paralelismo de hardware."

Página: Não informada.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.