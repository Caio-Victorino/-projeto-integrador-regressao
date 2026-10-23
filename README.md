# 🛠️ Projeto Integrador: Previsão de Força em Prensa Hidráulica (Manutenção Preditiva)

## 📌 Visão Geral do Projeto
Projeto prático focado na aplicação de Machine Learning (Regressão Linear vs. Polinomial) para prever o desgaste e a força de pressionamento exigida por uma prensa hidráulica industrial com base nas horas de operação contínua.

O objetivo foi construir um pipeline completo de Data Science, tratando ruídos de sensores e otimizando a precisão do modelo para o chão de fábrica.

---

## 🛠️ Etapas do Pipeline
1. **Tratamento e Limpeza de Dados:** Identificação e remoção de *outliers* (leituras falsas por falha de sensor).
2. **Divisão de Dados:** Separação entre Treino (80%) e Teste (20%) com validação cega.
3. **Engenharia de Recursos:** Transformação polinomial dos dados de entrada (Grau 2) para capturar o comportamento não-linear do fluido hidráulico.
4. **Avaliação de Desempenho:** Aplicação de métricas industriais ($R^2$, MAE e RMSE).

---

## 📊 Comparativo de Modelos (Resultados na Base de Teste)

| Modelo | $R^2$ Score (Precisão) | MAE (Erro Médio) | RMSE (Penalizador) | Conclusão Técnica |
| :--- | :--- | :--- | :--- | :--- |
| **Regressão Linear (Reta)** | $86{,}78\%$ | $51{,}28\text{ Ton}$ | $56{,}53\text{ Ton}$ | Inadequada para o processo; não captura a aceleração do desgaste. |
| **Regressão Polinomial (Curva)** | **$99{,}63\%$** | **$6{,}41\text{ Ton}$** | **$9{,}51\text{ Ton}$** | **Modelo Homologado.** Erro reduzido em $87,5\%$ com aderência quase perfeita. |

---

## 💻 Tecnologias Utilizadas
* **Linguagem:** Python
* **Bibliotecas:** Pandas, NumPy, Scikit-Learn
* **Ambiente:** Google Colab
