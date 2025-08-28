# Python para Epidemiologistas — IESC (Minicurso em 5 aulas)

Material do minicurso voltado a profissionais de epidemiologia que **já usam R/tidyverse** e desejam aprender **Python** no **Google Colab**.
**Sem instalações locais.** Cada notebook é autossuficiente, com dados sintéticos de fallback, exercícios com soluções colapsadas e uma tabela R↔Python incremental.

---

## Como começar

* **Aula 1 (Fundamentos)** — abra diretamente no Colab/Drive:
  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://tinyurl.com/python-iesc)
  *(Link fornecido pelo curso; abre o arquivo no seu Google Drive.)*

* Alternativamente, acesse a pasta deste repositório:

```
aulas/
└── Python IESC - Aula 1.ipynb
    Exercicios_complementares_Aula1.ipynb
```

**Dica (Colab):**

1. `Runtime > Run all` para executar tudo do zero.
2. `File > Save a copy in Drive` para salvar sua versão.
3. `Runtime > Factory reset runtime` para “limpar” o ambiente.

---

## Público‑alvo e pré‑requisitos

* Público: analistas de vigilância/epidemiologistas.
* Pré‑requisitos: estatística aplicada e **R/tidyverse**; nenhuma experiência prévia em Python é necessária.
* Ferramenta: **Google Colab** (navegador + conta Google).

---

## Estrutura do curso (macro‑cronograma)

1. **Aula 1 — Fundamentos de Python e Programação**
   Tipos/operadores, listas/tuplas/dicionários, condicionais, loops, **funções**, **list comprehensions** e **CSV**.
   Exercícios progressivos + 1 desafio integrador.

2. **Aula 2 — Introdução ao `pandas`**
   Criação e inspeção de DataFrames, seleção/filtragem (`query`/máscaras), `assign`, `groupby().agg()`; mini‑EDA; exemplo **OpenDataSUS** (fallback sintético).

3. **Aula 3 — Datas, joins, reshapes e curva epidêmica**
   `to_datetime`/`.dt`, `resample`, `melt`/`pivot`, `merge`; curva epidêmica e taxas por 100k.

4. **Aula 4 — Visualização para epidemiologia**
   Matplotlib/Seaborn: barras/linhas, facetas, rótulos/temas; widgets simples com `#@title`.

5. **Aula 5 — Modelos básicos e reprodutibilidade**
   GLM Poisson/Logística (`statsmodels`/`scikit-learn`), métricas, organização de projeto, exportação e compartilhamento no Drive.

> **Observação:** apenas a **Aula 1** está publicada neste repositório no momento.

---

## O que cada notebook inclui

* Seção **Setup** (imports, opções de display, semente aleatória).
* **Dados**: preferência por datasets públicos (ex.: OpenDataSUS/OWID/WHO/ECDC) com **fallback sintético reprodutível**.
* **Exercícios** no fluxo + **soluções colapsadas** (`<details>`).
* **Tabela R↔Python** incremental.
* **Checklist** de competências e referências oficiais.

---

## Mapa mental R ↔ Python (amostra)

| R/tidyverse                 | `pandas`                                                                  |                                         
| --------------------------- | ------------------------------------------------------------------------- | 
| `select(x, y)`              | `df[['x','y']]`                                                           |                                         
| `filter(a > 0 & sexo=='F')` | `df[(df['a']>0) & (df['sexo']=='F')]` / `df.query('a>0 and sexo==\"F\"')` |                                         
| `mutate(novo = f(x))`       | `df.assign(novo = f(df['x']))`                                            |                                         
| `group_by(g) > summarise(n=n())` | `df.groupby('g').agg(n=('col','size'))` |                                         
| `arrange(desc(x))`          | `df.sort_values('x', ascending=False)`                                    |                                         
| `rename(novo=antigo)`       | `df.rename(columns={'antigo':'novo'})`                                    |                                         

*(Tabelas completas em cada aula.)*

---

## Dados e privacidade

* Notebooks usam **amostras** e/ou **dados sintéticos** por padrão.
* Ao usar dados públicos (p.ex., **OpenDataSUS – SIVEP‑Gripe**), o notebook normaliza nomes de colunas e mantém **fallback** sintético se o download falhar ou estiver bloqueado.

---

## Contribuindo

* Sugerir melhorias/erros: abra uma *issue* ou envie *pull request* com exemplo mínimo reproduzível.
* Padrões: código comentado em PT‑BR, gráficos com rótulos e unidades, links para documentação oficial.

---

## Roadmap

* [ ] Publicar **Aula 2** (`pandas` básico).
* [ ] Publicar **Aula 3** (datas/reshapes/joins/curva epidêmica).
* [ ] Publicar **Aula 4** (visualização).
* [ ] Publicar **Aula 5** (GLM e reprodutibilidade).

---

## Licença

[GPL v3](https://www.gnu.org/licenses/gpl-3.0)

---

## Contato

* Dúvidas e sugestões: abra uma *issue* neste repositório.


