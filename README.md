# 🍃 Caracterização Físico-Química de Genótipos de Umbu-Cajazeira (Spondias sp.)

**Projeto de Ciência de Dados**  
*Análise estatística e visualização de dados experimentais para a seleção de genótipos promissores na agroindústria da Paraíba.*

---

## 📋 Descrição do Projeto

A umbu-cajazeira é uma frutífera de grande relevância para a agricultura familiar nordestina, porém seu potencial ainda é subutilizado devido ao conhecimento limitado sobre as propriedades dos frutos. Este projeto aplica técnicas de análise exploratória e inferência estatística a um conjunto de dados físico-químicos de diferentes genótipos coletados em três municípios paraibanos, com o objetivo de identificar materiais genéticos superiores para a indústria de polpa de fruta.

---

## 🎯 Objetivos

- Analisar as características físicas (peso, comprimento, diâmetro, rendimento de polpa) de quatro genótipos de umbu-cajazeira.
- Quantificar compostos bioativos (vitamina C, polifenóis, carotenoides, flavonoides) e parâmetros de qualidade (sólidos solúveis, acidez titulável, ratio SS/AT).
- Comparar estatisticamente os genótipos por meio de ANOVA e teste de Tukey (α = 5%).
- Recomendar os genótipos mais adequados ao processamento industrial com base em evidências quantitativas.

---

## 💾 Dados

Os dados brutos estão armazenados no arquivo `afq.csv` (análise físico-química). Cada linha representa uma repetição de medição, com variáveis organizadas em colunas.

### 📌 Dicionário de Variáveis (parcial)

| Variável | Descrição | Unidade |
|----------|-----------|---------|
| `peso_fresco` | Peso fresco do fruto | g |
| `comprimento` | Comprimento do fruto | mm |
| `diametro` | Diâmetro do fruto | mm |
| `rendimento_polpa` | Rendimento de polpa | % |
| `umidade` | Teor de umidade | % |
| `cinzas` | Cinzas | % |
| `acucares_red` | Açúcares redutores | % |
| `acidez_titulavel` | Acidez titulável | % ác. cítrico |
| `ph` | Potencial hidrogeniônico | – |
| `solidos_soluveis` | Sólidos solúveis (°Brix) | % |
| `ratio_SS_AT` | Relação sólidos solúveis / acidez titulável | – |
| `acido_ascorbico_nat` | Vitamina C (polpa *in natura*) | mg·100g⁻¹ |
| `acido_ascorbico_liof` | Vitamina C (polpa liofilizada) | mg·100g⁻¹ |
| `polifenois_nat` | Polifenóis extraíveis totais (*in natura*) | mg·100g⁻¹ |
| `polifenois_liof` | Polifenóis extraíveis totais (liofilizada) | mg·100g⁻¹ |
| … | Clorofila, carotenoides, flavonoides amarelos | – |

### 🧪 Amostras e Agrupamento por Genótipo

| Código no CSV | Local de Coleta | Genótipo (estudo) |
|---------------|-----------------|-------------------|
| P1 | Lucena – Seu Dedé | Genótipo 1  |
| P2 | Lucena – Seu Misso | Genótipo 2  |
| P3 | EMEPA (João Pessoa) | Genótipo 3 |
| P4 | Gurinhém | Genótipo 4 |
| P5 | Fazenda Humaitá – longe do rio | Genótipo 5 |
| P6 | Fazenda Humaitá – perto do rio | Genótipo 6 |

O delineamento experimental considerou 6 genótipos, com coletas realizadas no estádio de maturação comercial (coloração amarela da casca).

---

## 🔬 Metodologia

O tratamento dos dados foi realizado em Python, utilizando as bibliotecas **pandas**, **NumPy**, **SciPy** e **matplotlib**. As etapas principais incluíram:

1. **Limpeza e padronização** do arquivo `afq.csv`.
2. **Agrupamento** das amostras P1–P6 nos 4 genótipos definidos.
3. **Estatística descritiva** (média e desvio padrão) para todas as variáveis.
4. **ANOVA de um fator** para comparar os genótipos.
5. **Teste post-hoc de Tukey** para identificar diferenças significativas (α = 0,05).
6. **Visualizações** (boxplots, barras de erro) para comunicar os achados.
