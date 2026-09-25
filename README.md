# Checkpoint 2 — Machine Learning & Modelling / Statistical Computing with R & Python

**Curso:** Tecnólogo em Inteligência Artificial — FIAP
**Disciplinas:** Machine Learning & Modelling e Statistical Computing with R & Python
**Integrantes:** Gustavo Correia · Fabricio Cantuário
**Dataset:** [IRIS](https://archive.ics.uci.edu/dataset/53/iris) (via `scikit-learn`)

## Sobre o projeto

Este repositório contém o notebook do Checkpoint 2, que integra as duas disciplinas
utilizando o dataset IRIS:

- **Parte 1 — Statistical Computing with R and Python:** coleta, exploração,
  tratamento e validação dos dados. O dataset original do `scikit-learn` é limpo,
  então injetamos artificialmente (com semente fixa, para reprodutibilidade)
  problemas de qualidade comuns em coletas reais — valores ausentes, linhas
  duplicadas e inconsistências de rótulo — para então identificá-los e tratá-los.
- **Parte 2 — Machine Learning & Modelling:** separação treino/teste (70/30,
  estratificada), treinamento do modelo **KNN** para k = 1, 3, 5, 7 e 9, e
  comparação da acurácia de cada configuração.

## Resultado principal

| k | Acurácia |
|---|----------|
| 1 | 91,30% |
| 3 | 89,13% |
| 5 | 86,96% |
| 7 | 89,13% |
| 9 | 91,30% |

k = 1 e k = 9 empatam com a melhor acurácia. Optamos por **k = 9** como o ponto de
equilíbrio do modelo: mesma performance de k = 1, porém mais robusto a ruído, já que
considera 9 vizinhos na votação em vez de apenas 1.

## Como executar

1. Clone o repositório:
   ```bash
   git clone <link-deste-repositorio>
   cd <pasta-do-repositorio>
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Abra o notebook `checkpoint2_iris.ipynb` no Jupyter ou no Google Colab e execute
   todas as células (`Run All`).

## Estrutura do repositório

```
.
├── checkpoint2_iris.ipynb   # Notebook principal (Parte 1 + Parte 2)
├── requirements.txt         # Dependências do projeto
└── README.md                # Este arquivo
```

## Referências

- FISHER, Ronald A. *The use of multiple measurements in taxonomic problems.*
  Annals of Eugenics, v. 7, n. 2, p. 179-188, 1936.
- PEDREGOSA, F. et al. *Scikit-learn: Machine Learning in Python.* Journal of
  Machine Learning Research, v. 12, p. 2825-2830, 2011.
- UCI Machine Learning Repository. *Iris Data Set.*
  Disponível em: https://archive.ics.uci.edu/dataset/53/iris.
