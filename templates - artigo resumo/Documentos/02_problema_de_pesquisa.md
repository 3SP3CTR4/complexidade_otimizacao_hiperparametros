# Etapa 2: Problema de pesquisa

## Tema aprovado

Análise da complexidade computacional (tempo e espaço) das estratégias de otimização de hiperparâmetros (*Grid Search*, *Random Search*, Otimização Bayesiana) no algoritmo *XGBoost*.

## Pergunta de pesquisa

Qual é o impacto da escolha entre métodos exatos (*Grid Search*), estocásticos (*Random Search*) e heurísticos (Otimização Bayesiana) na complexidade de tempo, no consumo de espaço e no desempenho preditivo no ajuste de hiperparâmetros do algoritmo *XGBoost*?

## Verificação

- **O que se deseja descobrir ou compreender?** O compromisso (*trade-off*) técnico e matemático entre o custo de processamento exigido por diferentes métodos de busca e o ganho preditivo gerado no modelo.
- **Qual é o objeto da pergunta?** A otimização de hiperparâmetros (HPO).
- **Qual é o contexto ou recorte?** A aplicação estrita no algoritmo estruturado em árvores *XGBoost*, sob a ótica da complexidade de algoritmos.
- **A pergunta pode ser respondida por artigos científicos?** Sim. Os artigos de fundamentação algorítmica fornecem as provas matemáticas (Notação *Big-O*) do custo computacional de cada técnica.
- **Por que essa pergunta é relevante?** Porque foca na otimização de recursos de *hardware* (evitando explosão de RAM e tempo de CPU) que muitas vezes são negligenciados em prol de ganhos marginais de acurácia.

## Produto da etapa

Pergunta de pesquisa aprovada.

## Checklist

- [x] Está escrita em forma de pergunta.
- [x] É clara e objetiva.
- [x] Está alinhada ao tema.
- [x] Pode ser respondida por revisão bibliográfica.
- [x] Não exige experimento que não será realizado.

## Contribuições

| Integrante | Atividade realizada | Contribuição |
| :--- | :--- | :---: |
| Luis Hardt | Estruturação da problemática central focada em teoria da computação. | 40% |
| Aliana Sthefani  | Avaliação da viabilidade técnica da pergunta frente à literatura. | 40% |
| Bruna Alves de Jesus | Leitura passiva da formulação da pergunta. | 5% |
| Guilherme Zanni | Validação da sintaxe da pergunta. | 5% |
| Miguel Pereira | Acompanhamento do fechamento do problema. | 5% |
| Thales Eduardo | Revisão gramatical do arquivo. | 5% |