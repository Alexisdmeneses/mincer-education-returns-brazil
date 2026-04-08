# Returns to schooling in Brazil

Econometric study estimating the impact of education on wages in Brazil using PNAD/IBGE panel data across all 27 states from 2012 to 2025.

## Research question

*What is the return to an additional year of schooling on wages in Brazil?*

## Approach

Three model specifications estimated sequentially:

1. **Basic Mincer equation** — OLS with HC3 robust standard errors
2. **Pooled OLS with controls** — state dummies, year dummies, quarter dummies (R²=0.69)
3. **Panel fixed effects** — entity and time effects via PanelOLS (R²_within=0.63)

Extension: wage premiums by education level (dummies replacing continuous years of schooling, R²=0.94)

## Key results

- Each additional year of schooling is associated with ~7.6% higher wages, robust across all three specifications
- Workers with a completed university degree earn on average 344% more than workers with no formal education
- Strong regional wage inequality: São Paulo and Santa Catarina show ~40–45% higher wages than Acre, controlling for education and time
- Macroeconomic shocks (2016–2020) show negative year coefficients, but the education effect remains stable

## Data

- Source: IBGE PNAD Contínua — tabela 5438
- Coverage: 27 Brazilian states · Q1 2012 – Q3 2025 · 7 education levels
- Observations: 8,883 after filtering

## Stack

Python · pandas · numpy · statsmodels · linearmodels · matplotlib

## Structure

```
├── AlexisCanez_Econ_TrabalhoFinal.ipynb   ← main notebook
├── AlexisCanez_Econ_TrabalhoFinal.pdf     ← rendered output
├── data/
│   └── tabela5438_arrumada.xlsx
└── README.md
```

## How to run

```bash
pip install pandas numpy statsmodels linearmodels matplotlib openpyxl
jupyter notebook AlexisCanez_Econ_TrabalhoFinal.ipynb
```
