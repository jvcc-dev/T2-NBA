# T2-NBA — Análise Probabilística NBA

**Disciplina:** Métodos Quantitativos para Computação  
**Professor:** Prof. Me. Ricardo Carubbi  
**Instituição:** UNIFOR  

---

## Integrantes

- João Victor Cunha de Castro
- Heitor Cunha Damasceno

---

link1: https://drive.google.com/file/d/1h-S7D-yBWH27PC_KeuwEtC0ojbGH9lj8/view?usp=drivesdk
João victor cunha de castro

## Pergunta de Pesquisa

> **A não permanência observada no mesmo time é mais frequente entre casos jogador-temporada classificados como baixo desempenho?**

---

## Descrição dos Eventos

| Evento | Descrição |
|--------|-----------|
| **S** | Caso jogador-temporada em que o jogador **não é observado no mesmo time na temporada seguinte** (`nao_permanencia = True`). Casos da última temporada disponível foram excluídos da análise por não possuírem temporada seguinte observável. |
| **B** | Caso jogador-temporada classificado como **baixo desempenho**, definido por `X ≥ 2` — ou seja, pelo menos dois dos três indicadores de baixo desempenho presentes simultaneamente: pontos, minutos totais e jogos disputados abaixo do quartil inferior do dataset. |

---

## Variável de Contagem — Análise de Poisson

A variável de contagem utilizada é **X**, definida como o número de indicadores de baixo desempenho observados por caso jogador-temporada, com `X ∈ {0, 1, 2, 3}`.

A **unidade de exposição** é uma temporada por jogador (caso jogador-temporada). O parâmetro **λ** foi estimado pela média empírica de X no subconjunto de análise.

---

## Estrutura do Repositório

```
T2-NBA/
├── dataset/
│   └── nba_stats_preprocessed.csv   # dataset tratado utilizado na análise
├── T2_NBA_MIL.ipynb                 # notebook documentado e executável
└── README.md
```

---

## Vídeo Explicativo

> 🔗 **[Inserir link do vídeo aqui]**

---

## Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/T2-NBA
   cd T2-NBA
   ```
2. Instale as dependências:
   ```bash
   pip install pandas numpy matplotlib seaborn scipy
   ```
3. Abra o notebook e execute todas as células em ordem:
   ```bash
   jupyter notebook T2_NBA_MIL.ipynb
   ```
