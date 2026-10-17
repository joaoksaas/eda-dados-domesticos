# Análise de despesas de uma família (dados simulados)

> **Status: em andamento.** Projeto de estudo de análise de dados com Python e pandas.

## Sobre o projeto

Análise exploratória de uma tabela de despesas domésticas de uma família fictícia
(casal, dois filhos e um pet) ao longo de 36 meses (out/2023 a set/2026).

**Os dados são simulados** (gerados com apoio de IA, com padrões como inflação e
sazonalidade embutidos). Os resultados abaixo servem para praticar o método, e não
descrevem nenhuma família real.

## Perguntas que o projeto tenta responder

- Para onde vai o dinheiro da família? (categorias)
- Como o gasto evolui no tempo? (mês, ano, sazonalidade)
- Quanto do orçamento é fixo, variável, essencial ou supérfluo?
- O aumento do gasto é real ou só inflação?
- Qual o peso de cada forma de pagamento, e como ela muda ao longo do tempo?
- Como limpar uma versão "suja" da mesma tabela (duplicatas, formatos misturados, nulos)?

## Estrutura

```
.
├── data/
│   ├── despesas_familia.csv        # tabela limpa
│   └── despesas_familia_suja.csv   # versão com problemas, para a etapa de limpeza
├── analise.ipynb                   # notebook com a análise
├── limpeza.py                      # funções de apoio à limpeza
└── README.md
```

## Etapas

- [x] 1. Conhecer os dados
- [x] 2. Gasto por categoria
- [x] 3. Evolução no tempo
- [x] 4. Fixo vs. variável, essencial vs. supérfluo
- [x] 5. Gráficos
- [x] 6. Perguntas mais profundas (inflação, responsável, forma de pagamento)
- [ ] 7. Limpeza de dados (em andamento)
- [ ] 8. Conclusões e versão final do notebook

## Resultados preliminares

- 1.439 lançamentos em 13 categorias.
- Moradia, Educação e Saúde somam cerca de 59% do gasto total.
- Entre 2024 e 2025, a média mensal de gasto subiu cerca de 8,0% em valores nominais,
  mas só cerca de 3,3% depois de descontar a inflação (taxa fixa de 4,5% ao ano).
- O cartão de crédito fica em torno de 30% do gasto, sem tendência de alta, com
  picos nos meses de viagem (julho).

## Como rodar

```bash
pip install pandas matplotlib ipykernel
```

Abra `analise.ipynb` no VS Code (ou Jupyter) e execute as células em ordem.

## Ferramentas

Python, pandas, matplotlib.