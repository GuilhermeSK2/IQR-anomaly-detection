# Detecção de Anomalias com o Método IQR (Intervalo Interquartil)

Este projeto Python demonstra a aplicação do método do Intervalo Interquartil (IQR) para identificar anomalias (outliers) em um conjunto de dados numéricos. O método IQR é uma técnica robusta, menos sensível a outliers extremos em comparação com o Z-score, e é particularmente útil para dados que não seguem uma distribuição normal.

## Visão Geral

O método IQR para detecção de anomalias baseia-se na distribuição dos quartis dos dados:
1.  **Quartil 1 (Q1):** O valor abaixo do qual 25% dos dados se encontram.
2.  **Quartil 3 (Q3):** O valor abaixo do qual 75% dos dados se encontram.
3.  **Intervalo Interquartil (IQR):** Calculado como `Q3 - Q1`. Representa a amplitude dos 50% centrais dos dados.
4.  **Limites de Anomalia:**
    * **Limite Inferior:** `Q1 - 1.5 * IQR`
    * **Limite Superior:** `Q3 + 1.5 * IQR`
    Pontos de dados que caem abaixo do limite inferior ou acima do limite superior são considerados anomalias.

Neste projeto, o processo é o seguinte:
1.  Um conjunto de dados numéricos é definido.
2.  Os quartis Q1 e Q3 são calculados.
3.  O IQR é calculado.
4.  Os limites inferior e superior para a identificação de anomalias são determinados.
5.  Os pontos de dados que excedem esses limites são listados como anomalias.

## Estrutura do Projeto

* `IQR.ipynb`: O notebook Jupyter que contém todo o código para definir os dados, calcular IQR e identificar anomalias.

## Tecnologias Utilizadas

* **Python 3**
* **NumPy**: Para cálculo eficiente de percentis.
* **Jupyter Notebook**: Para execução e demonstração interativa do código.

## Exemplo de Detecção

No notebook, um `dataset` de exemplo é fornecido com valores que são claramente outliers:

```python
dataset = [-100, 1, 2, 3, 4, 5, 6, 7, 8, 9, 100]
