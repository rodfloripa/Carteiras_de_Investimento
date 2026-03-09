

---

<p align="justify"><h1>Carteiras de Ações: O Impacto da Selic a 15,00%</h1></p>

<p align="justify">Este documento apresenta a análise de desempenho de três estratégias de investimento — Risco Baixo, Médio e Alto — processadas através do seu ambiente Python. O foco principal recai sobre a eficiência de cada carteira quando ajustada pela volatilidade do mercado, utilizando o <b>Índice de Sharpe</b> como métrica balizadora para a tomada de decisão.</p>

<p align="justify"><h3>1. Metodologia e Parâmetros Reais</h3></p>

<p align="justify">A análise incorpora a realidade económica vigente, utilizando uma Taxa Livre de Risco de 15,00% ao ano (<b>taxa_livre_risco_anual = 0.15</b>). Este valor reflete o retorno atual do Tesouro Selic e de investimentos de liquidez imediata que acompanham o CDI. Os retornos dos portfólios foram calculados com base numa estratégia de pesos iguais para cada ativo dentro das carteiras, garantindo uma distribuição equilibrada.</p>

<p align="justify"><h3>2. O Conceito: O Índice de Sharpe</h3></p>

<p align="justify">O Índice de Sharpe é uma ferramenta fundamental para medir a qualidade de um investimento. Ele não avalia apenas o retorno final, mas sim quanto risco foi necessário correr para alcançar esse resultado acima do que o investidor ganharia "parado" no Tesouro Direto. Matematicamente, o índice <b>S</b> é calculado pela razão entre o retorno excedente e a volatilidade anualizada:</p>

<p align="center">
<b>S = (R<sub>p</sub> - R<sub>f</sub>) / σ<sub>p</sub></b>
</p>

<p align="justify">Onde <b>R<sub>p</sub></b> é o retorno anualizado do portfólio e <b>R<sub>f</sub></b> é a taxa livre de risco de 15,00%. Se o retorno da sua carteira não superar significativamente os <b>1,17% mensais</b> (equivalentes aos 15% anuais), o numerador da fórmula torna-se próximo de zero ou negativo, indicando que a volatilidade da bolsa não está a ser recompensada.</p>

<p align="justify"><h3>3. Resultados e Análise de Eficiência</h3></p>

<p align="justify">Com base nos dados extraídos do notebook, a comparação com o rendimento de "risco zero" revela os seguintes indicadores de eficiência:</p>

| Carteira | Cenário | Retorno Mensal | Sharpe Ratio (15% a.a.) |
| --- | --- | --- | --- |
| **Risco Baixo** | Original | 1,18% | **-0,04** |
| **Risco Baixo** | Diversificado | 1,31% | **0,04** |
| **Risco Médio** | Original | 1,36% | **0,05** |
| **Risco Médio** | Diversificado | 1,21% | **-0,02** |
| **Risco Alto** | Original | 1,91% | **0,23** |
| **Risco Alto** | Diversificado | 1,87% | **0,20** |

<p align="justify"><h3>4. Conclusão Crítica</h3></p>

<p align="justify">Os resultados confirmam que, com a Selic a 15,00%, a "barra" para o sucesso na renda variável é extremamente elevada. O portfólio de <b>Risco Baixo Original</b> e o <b>Risco Médio Diversificado</b> apresentam índices de Sharpe negativos (-0,04 e -0,02), o que significa que estas estratégias renderam menos que o Tesouro Direto no período, apesar de exporem o investidor ao risco de mercado. Apenas a carteira de <b>Risco Alto</b> consegue entregar um prêmio de risco positivo e consistente (0,23), sendo a única que justifica matematicamente a alocação em ações sob as condições atuais de juros elevados.</p>
