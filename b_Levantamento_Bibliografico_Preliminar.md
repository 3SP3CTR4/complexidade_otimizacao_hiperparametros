# Etapa (b) — Levantamento Bibliográfico

> **Como preencher:** este documento deve ser preenchido **em conjunto pelo grupo**, mas com registro individualizado da contribuição de cada integrante em cada passo. Substitua os campos entre `[ ]` pelas informações do seu grupo. Não apague as instruções em itálico — elas ajudam na avaliação do orientador.

---

## 1. Identificação do Grupo

| Campo | Informação |
|---|---|
| Curso / Disciplina | Ciência da Computação / Computabilidade e Complexidade de Algoritmos |
| Projeto de Pesquisa / IC | Projeto Integrado (-) |
| Orientador(a) | Profa. Dra. Andréa Ono Sakai |
| Data de entrega desta etapa | 10/09/2026 |
| Integrantes do grupo | Aliana Sthefani, Bruna Alves, Guilherme Zanni, Luis Hardt, Miguel Pereira, Thales Eduardo |
| Tema (da etapa "a") | XGBoost: comparação de complexidade computacional e desempenho entre Grid Search, Random Search e Otimização Bayesiana |

---

## FASE 1 — Planejamento da Busca

### Passo 1 — Pergunta de pesquisa e palavras-chave

**1.1 Problema/pergunta de pesquisa (versão de trabalho)**
*Ainda não precisa ser a versão final (isso vem na etapa "c"), mas deve orientar a busca desta fase.*

> Como a escolha entre métodos exatos (Grid Search), estocásticos (Random Search) e heurísticos (Otimização Bayesiana) impacta a complexidade de tempo, o consumo de espaço e o desempenho preditivo no ajuste de hiperparâmetros do algoritmo XGBoost?

**1.2 Conceitos-chave e sinônimos**
*Liste os conceitos centrais da pergunta e seus sinônimos, em português e inglês.*

| Conceito-chave | Sinônimos / termos relacionados (PT) | Sinônimos / termos relacionados (EN) |
|---|---|---|
| Otimização de Hiperparâmetros | Ajuste de hiperparâmetros | Hyperparameter optimization, hyperparameter tuning |
| Estratégias de Busca | Busca em Grade, Busca Aleatória, Bayesiana | Grid Search, Random Search, Bayesian Optimization |
| Complexidade Computacional | Custo computacional, tempo de execução, tempo de inferência | Algorithmic complexity, computational cost, execution time |
| XGBoost | Gradient Boosting, árvores de decisão | XGBoost, Extreme Gradient Boosting, Gradient Boosting |

*Responsável por este passo: Aliana e Luis*

---

### Passo 2 — Strings de busca

*Combine os termos do passo 1 com operadores booleanos (`AND`, `OR`, `NOT`). Use aspas para termos compostos e truncamento (`*`) quando a base permitir.*

| Nº | String de busca | Base(s) em que será usada | Elaborada por |
|---|---|---|---|
| 1 | ("XGBoost" OR "Extreme Gradient Boosting") AND ("Hyperparameter Optimization" OR "Hyperparameter tuning") AND ("Grid Search" OR "Random Search" OR "Bayesian Optimization") | IEEE Xplore, ACM Digital Library | Aliana |
| 2 | "Hyperparameter Optimization" AND ("Computational Cost" OR "Time Complexity" OR "Algorithmic Complexity") | Scopus / Portal CAPES | Luis |
| 3 | ("Grid Search" OR "Random Search" OR "Bayesian Optimization") AND "XGBoost" AND "Performance" | Google Scholar / IEEE | Aliana |

---

### Passo 3 — Bases de dados escolhidas

*Selecione de 2 a 4 bases relevantes ao tema. Registre a justificativa — isso vai para a seção de metodologia do artigo/relatório de IC.*

| Base de dados | Por que foi escolhida | Responsável pela busca nesta base |
|---|---|---|
| IEEE Xplore | Principal repositório para artigos com foco em engenharia de software e análise rigorosa de custo de hardware e processamento. | Luis |
| ACM Digital Library | Acervo essencial em Ciência da Computação pura para algoritmos de aprendizado de máquina. | Aliana |
| Portal CAPES / Scopus | Necessário para capturar revisões amplas de literatura (estado da arte) e cobrir revistas de impacto em Inteligência Artificial. | Aliana |

---

### Passo 4 — Critérios de inclusão e exclusão

**Critérios de inclusão:**
- Artigos publicados entre 2012 e 2026.
- Foco em comparação direta de algoritmos de busca, complexidade computacional ou consumo de memória em modelos baseados em árvores e *boosting*.
- Revisados por pares (revistas científicas ou anais de conferências de alto impacto).

**Critérios de exclusão:**
- Artigos focados exclusivamente em redes neurais profundas (*Deep Learning*) ou arquiteturas específicas de outros domínios (como SVM).
- Trabalhos acadêmicos que não abordem o custo ou a mecânica de otimização de hiperparâmetros.

*Definidos em conjunto por: Aliana e Luis*

---

## FASE 2 — Execução da Busca e Triagem

### Passo 5 — Execução das buscas e registro dos resultados

*Anote quantos resultados cada string trouxe em cada base (útil para o fluxograma tipo PRISMA, se o projeto exigir). Exporte as referências (BibTeX, RIS, CSV) para um gerenciador de referências.*

| Base | String usada (nº) | Data da busca | Nº de resultados | Executada por |
|---|---|---|---|---|
| IEEE Xplore | 1 e 2 | 10/09/2026 | 28 | Luis |
| ACM Digital Library | 1 | 10/09/2026 | 14 | Aliana |
| Portal CAPES/Scopus | 2 e 3 | 10/09/2026 | 18 | Aliana e Luis |

**Total de resultados brutos (soma de todas as buscas):** 60

**Gerenciador de referências utilizado:** Mendeley / Zotero
**Formato de exportação:** RIS / BibTeX

---

### Passo 6 — Triagem por título e resumo (1ª filtragem)

*Leia apenas título e resumo de cada resultado. Classifique: incluir / excluir / dúvida. Remova duplicatas entre bases.*

| Item de controle | Quantidade |
|---|---|
| Total de resultados antes da triagem | 60 |
| Duplicatas removidas | 8 |
| Classificados como "Incluir" | 22 |
| Classificados como "Excluir" | 25 |
| Classificados como "Dúvida" | 5 |

*A triagem detalhada, artigo por artigo, deve ser registrada na planilha de controle do projeto (aba "Triagem de Artigos"). Aqui, registre apenas o resumo quantitativo.*

**Como as dúvidas foram resolvidas?** 
Realizamos uma leitura dinâmica da introdução dos 5 artigos em dúvida. Avaliamos se o texto mencionava custos de hardware ou tempo de execução (Tempo e Espaço) atrelados às buscas. Artigos focados puramente em acurácia clínica ou financeira, sem análise de complexidade, foram excluídos.

*Responsável(is) por esta triagem: Aliana e Luis*

---

### Passo 7 — Triagem por leitura completa (2ª filtragem)

*Para os artigos que passaram na primeira filtragem, leia introdução e conclusão. Aplique os critérios de inclusão/exclusão (passo 4) de forma mais rigorosa.*

| Item de controle | Quantidade |
|---|---|
| Total de artigos que entraram nesta filtragem | 27 (22 Incluídos + 5 Dúvidas resolvidos) |
| Aprovados (conjunto definitivo para fichamento) | 14 |
| Excluídos nesta etapa | 13 |

**Principais motivos de exclusão nesta filtragem:**
- Otimização superficial: Os artigos mencionavam a otimização de hiperparâmetros, mas não comparavam métodos (ex: usavam apenas Grid Search de forma arbitrária).
- Fuga do escopo algorítmico: Muitos textos eram de áreas médicas/financeiras focados nos dados, negligenciando a avaliação analítica da escalabilidade do XGBoost.

*Responsável(is) por esta triagem: Aliana e Luis*

---

## 3. Lista Final de Artigos Selecionados (Conjunto Definitivo)


1. BERGSTRA, J.; BENGIO, Y. Random search for hyper-parameter optimization. **Journal of Machine Learning Research**, v. 13, p. 281-305, 2012. Disponível em: https://jmlr.csail.mit.edu/papers/v13/bergstra12a.html. Acesso em: 5 set. 2026.
2. CHEN, T.; GUESTRIN, C. XGBoost: A scalable tree boosting system. *In*: ACM SIGKDD INTERNATIONAL CONFERENCE ON KNOWLEDGE DISCOVERY AND DATA MINING, 22., 2016, São Francisco. **Proceedings** [...]. [S. l.: s. n.], 2016. p. 785-794. DOI: https://doi.org/10.1145/2939672.2939785. Acesso em: 5 set. 2026.
3. YANG, L.; SHAMI, A. On hyperparameter optimization of machine learning algorithms: Theory and practice. **Neurocomputing**, v. 415, p. 295-316, 2020. DOI: https://doi.org/10.1016/j.neucom.2020.07.061. Acesso em: 5 set. 2026.
4. BENTÉJAC, C.; CSÖRGŐ, A.; MARTÍNEZ-MUÑOZ, G. A comparative analysis of gradient boosting algorithms. **Artificial Intelligence Review**, v. 54, n. 3, p. 1937-1967, 2021. DOI: https://doi.org/10.1007/s10462-020-09896-5. Acesso em: 21 ago. 2026[cite: 3].
5. VICTORIA, A. H.; MARAGATHAM, G. Automatic tuning of hyperparameters using Bayesian optimization. **Evolving Systems**, v. 12, n. 1, p. 217-223, 2021. DOI: https://doi.org/10.1007/s12530-020-09345-2. Acesso em: 6 set. 2026[cite: 3].
6. BISCHL, B. *et al*. Hyperparameter optimization: Foundations, algorithms, best practices, and open challenges. **WIREs Data Mining and Knowledge Discovery**, v. 13, n. 2, p. e1484, 2023. DOI: https://doi.org/10.1002/widm.1484. Acesso em: 6 set. 2026[cite: 3].
7. BORISOV, V. *et al*. Deep Neural Networks and Tabular Data: A Survey. **IEEE Transactions on Neural Networks and Learning Systems**, v. 34, n. 11, p. 8171-8185, 2023. DOI: https://doi.org/10.1109/TNNLS.2022.3229161. Acesso em: 5 set. 2026.
8. FEURER, M.; HUTTER, F. Hyperparameter optimization. *In*: Automated Machine Learning: Methods, Systems, Challenges. Springer, Cham, p. 3-33, 2019. DOI: https://doi.org/10.1007/978-3-030-05318-5_1. Acesso em: 21 ago. 2026[cite: 3].
9. WU, J. *et al*. Hyperparameter optimization for machine learning models based on Bayesian optimization. **Journal of Electronic Science and Technology**, v. 17, n. 1, p. 26-40, 2019. DOI: https://www.sciencedirect.com/science/article/pii/S1674862X19300047. Acesso em: 21 ago. 2026[cite: 3].
10. SHAHRIARI, B. *et al*. Taking the human out of the loop: A review of Bayesian optimization. **Proceedings of the IEEE**, v. 104, n. 1, p. 148-175, 2016. DOI: https://doi.org/10.1109/JPROC.2015.2494218. Acesso em: 22 ago. 2026[cite: 3].
11. SCHRATZ, P. *et al*. Hyperparameter tuning and performance assessment of tree and tree-based machine learning algorithms. **Ecological Modelling**, v. 406, p. 109-120, 2019. DOI: https://doi.org/10.1016/j.ecolmodel.2019.06.002. Acesso em: 22 ago. 2026[cite: 3].
12. PROBST, P.; BISCHL, B.; BOULESTEIX, A.-L. Tunability: Importance of hyperparameters of machine learning algorithms. **Journal of Machine Learning Research**, v. 20, n. 53, p. 1-32, 2019. Acesso em: 6 set. 2026.
13. LI, L. *et al*. Hyperband: A novel bandit-based approach to hyperparameter optimization. **Journal of Machine Learning Research**, v. 18, n. 185, p. 1-52, 2018. Acesso em: 6 set. 2026.
14. SNOEK, J.; LAROCHELLE, H.; ADAMS, R. P. Practical Bayesian optimization of machine learning algorithms. **Advances in Neural Information Processing Systems**, v. 25, p. 2951-2959, 2012. Acesso em: 6 set. 2026.

---

## 4. Contribuição Individual dos Integrantes

### Integrante 1 — Aliana 
- **Passo(s) em que atuou:** Passos 1, 2, 3, 5, 6 e 7.
- **O que fez em cada passo:** Formulei a pergunta de pesquisa central focada na teoria de complexidade e delimitei as bases da ACM e Portal CAPES. Executei buscas com as strings 1 e 3, obtendo resultados preliminares. Conduzi a triagem de 50% dos títulos/resumos do escopo de 60 artigos e liderei a seleção por leitura completa integrando os 7 artigos adicionais do rascunho validado ao conjunto principal.
- **Tempo dedicado (aprox.):** 7h
- **Evidência da contribuição:** Planilha de controle Excel preenchida com as decisões de inclusão e histórico dos DOIs.

### Integrante 2 — Luis
- **Passo(s) em que atuou:** Passos 2, 3, 4, 5, 6 e 7.
- **O que fez em cada passo:** Estruturou os critérios rigorosos de exclusão para barrar artigos fora do escopo algorítmico. Gerenciou a busca primária na base IEEE Xplore com 28 resultados brutos. Executou a remoção das 8 duplicatas entre as bases e auxiliou na triagem dos textos completos para totalizar os 14 artigos do fichamento.
- **Tempo dedicado (aprox.):** 6h
- **Evidência da contribuição:** Registros de filtragem na base IEEE Xplore e remoção cruzada de duplicatas.

### 4.1 Quadro-resumo de participação por passo

| Passo | Responsável(is) | % estimado de participação de cada um |
|---|---|---|
| 1. Pergunta e palavras-chave | Aliana | Aliana 100% |
| 2. Strings de busca | Aliana, Luis | Aliana 50% / Luis 50% |
| 3. Bases de dados | Aliana, Luis | Aliana 50% / Luis 50% |
| 4. Critérios de inclusão/exclusão | Aliana, Luis | Aliana 50% / Luis 50% |
| 5. Execução das buscas | Aliana, Luis | Aliana 50% / Luis 50% |
| 6. Triagem título/resumo | Aliana, Luis | Aliana 50% / Luis 50% |
| 7. Triagem texto completo | Aliana, Luis | Aliana 50% / Luis 50% |

### 4.2 Quadro-resumo geral de participação na etapa

| Integrante | % estimado de participação total nesta etapa |
|---|---|
| Aliana | 50% |
| Luis | 50% |

---

## 5. Checklist Final da Etapa

**Fase 1 — Planejamento**
- [x] Pergunta de pesquisa de trabalho definida
- [x] Conceitos-chave e sinônimos (PT/EN) listados
- [x] Strings de busca elaboradas com operadores booleanos
- [x] Bases de dados escolhidas e justificadas
- [x] Critérios de inclusão e exclusão definidos

**Fase 2 — Execução e triagem**
- [x] Buscas executadas e resultados registrados (60 artigos brutos)
- [x] Referências exportadas para o gerenciador de referências
- [x] Triagem por título/resumo concluída (com 8 duplicatas removidas)
- [x] Triagem por texto completo (introdução/conclusão) concluída
- [x] Conjunto definitivo de 14 artigos compilados

**Documentação**
- [x] Contribuição individual de cada integrante registrada por passo
- [x] Quadro-resumo de participação preenchido (soma = 100%)