# Simulador Termodinâmico PVT: Equações de Estado Cúbicas (RK, SRK, PR)

Este projeto consiste em um simulador interativo desenvolvido em Python para o cálculo e análise do **Fator de Compressibilidade (Z)** de hidrocarbonetos e contaminantes. O foco principal é a comparação de modelos cúbicos e sua aplicabilidade em condições extremas da indústria de Óleo e Gás.

---

##  O Projeto
O simulador permite visualizar como o comportamento de gases reais se desvia da idealidade sob diferentes condições de pressão e temperatura, mapeando desde condições de superfície até reservatórios **HPHT (High Pressure, High Temperature)**, como os encontrados no **Pré-Sal brasileiro**.

### Modelos Implementados:
1. **Redlich-Kwong (RK):** O primeiro modelo a introduzir a dependência da temperatura no termo de atração.
2. **Soave-Redlich-Kwong (SRK):** Evolução que integra o fator acêntrico ($\omega$) para melhorar a predição da pressão de vapor.
3. **Peng-Robinson (PR):** O padrão ouro da indústria para hidrocarbonetos, com refinamentos no co-volume e na predição de densidades de fase líquida.

---

## Diferenciais Técnicos
* **Range Industrial:** O simulador opera até **100 MPa**, permitindo análise de fluidos em condições de ultra-profundidade.
* **Rastreabilidade de Dados:** Banco de dados de propriedades críticas baseado no *Smith, Van Ness & Abbott* e *NIST*.
* **Seleção de Raiz Estável:** Implementação de lógica para filtragem de raízes reais fisicamente consistentes ($Z > B$), garantindo a estabilidade numérica em altas pressões.
* **Interface Interativa:** Uso de `ipywidgets` para manipulação dinâmica das isotermas em tempo real.

---

##  Estrutura do Repositório
* `/Versao 1`: Protótipo inicial focado em Peng-Robinson básico.
* `/Versao 2`: Implementação de carregamento via JSON e interface interativa.
* `/Versao 3`: (Atual) Dashboard comparativo multimodelos com zoneamento industrial (Superfície vs Reservatório).
* `fluidos.json`: Banco de dados com propriedades críticas ($T_c, P_c, \omega$) de 13 componentes essenciais.

---

##  Lições Aprendidas (Engenharia)
Durante o desenvolvimento, observou-se que em ranges de pressão muito elevados (acima de 70 MPa), o **Domínio de Repulsão** torna-se tão dominante que sutilezas como o "mínimo de Z" (Domínio de Atração) podem ser visualmente mascaradas se a escala não for ajustada. Além disso, reforçou-se a compreensão de que modelos cúbicos, embora robustos para hidrocarbonetos, possuem limitações em sistemas polares ou fundo de colunas de destilação de pesados, onde modelos de atividade seriam mais indicados.

---

## Como Executar
1. Clone o repositório.
2. Certifique-se de ter as bibliotecas instaladas: `numpy`, `pandas`, `plotly` e `ipywidgets`.
3. Abra o arquivo `Simulador_PVT_Comparativo_v3.ipynb` em um ambiente que suporte widgets (Jupyter Notebook ou VS Code).