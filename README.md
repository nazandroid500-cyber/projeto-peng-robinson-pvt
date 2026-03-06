#  Modelagem PVT: Equação Peng-Robinson para Petróleo

**Implementação da equação de estado Peng-Robinson** para calcular fator de compressibilidade Z e volume molar de hidrocarbonetos (C1-C8).

[![Z vs P](img/grafico_z.png)](notebook.ipynb)
[![Volume PR vs Ideal](img/volume_comparison.png)](notebook.ipynb)

##  O que faz
- Calcula **Z** e **Vm** para qualquer hidrocarboneto
- **Compara** gás ideal vs real (erro até 25%)
- **Visualizações** interativas (Plotly + Matplotlib)
- **Tabela fixa metano** (referência gás natural)

##  Resultados principais
| Fluido | Tc(K) | Z@Tc,100bar |
|--------|-------|-------------|
| Metano | 191   | 0.750      |
| n-Pentano | 470 | 0.820  |

## 🚀 Como usar (sem código!)

1. 1. **[Abrir Notebook interativo](https://mybinder.org/v2/gh/nazandroid500-cyber/projeto-peng-robinson-pvt/main?filepath=peng_robinson_pvt.ipynb)** 👈 **Clique aqui**
2. Mude `fluido_escolhido = "metano"` e rode célula 8
3. Gráficos e tabelas atualizam automaticamente!

##  Tech
- Python 3.9+
- pandas, numpy, plotly, matplotlib

##  Galeria
![Z×P n-Pentano](img/z_pressao.png)
![Volume Comparison](img/volume_pr_ideal.png)

**Feito por Matheus Santana** | [LinkedIn](https://linkedin.com/in/matheussantana) | Mar/2026
