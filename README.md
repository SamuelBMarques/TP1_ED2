# 🔎 Estruturas de Dados II — TP1

Implementação e comparação de diferentes **métodos de pesquisa em arquivos** utilizando estruturas de dados e índices, desenvolvida em **C** para a disciplina de **Estruturas de Dados II (ED2)**.

O projeto analisa o desempenho de diferentes estratégias de busca considerando arquivos com registros ordenados e aleatórios.

---

## 🎯 Objetivo

O objetivo é comparar diferentes métodos de pesquisa sobre grandes conjuntos de registros, analisando:

* Número de comparações
* Número de transferências
* Tempo de criação do índice
* Tempo de pesquisa
* Tempo total de execução

Os testes são realizados com diferentes quantidades de registros e diferentes organizações dos arquivos.

---

## 🔎 Métodos de pesquisa

O projeto implementa quatro métodos:

| Método | Estrutura        |
| ------ | ---------------- |
| `1`    | Busca Sequencial |
| `2`    | Árvore Binária   |
| `3`    | Árvore B         |
| `4`    | Árvore B*        |

As árvores B e B* são construídas a partir dos registros armazenados em arquivos binários.

---

## 📊 Testes

Os experimentos consideram diferentes tamanhos de entrada:

```text
100
1.000
10.000
100.000
1.000.000
```

Os arquivos utilizados podem estar organizados em:

* Ordem crescente
* Ordem decrescente
* Ordem aleatória

Os resultados dos testes são armazenados em `resultados_teste.csv`. O script `testador.py` automatiza a execução dos experimentos e coleta as métricas de desempenho.

---

## 🛠️ Tecnologias e conceitos

* **C**
* Estruturas de dados
* Arquivos binários
* Ponteiros
* Alocação dinâmica
* Busca sequencial
* Árvore Binária de Busca
* Árvore B
* Árvore B*
* Análise de desempenho
* Python para automação dos testes

---

## 📁 Estrutura do projeto

```text
TP1_ED2/
│
├── include/
│   ├── b_tree.h
│   ├── b_star_tree.h
│   ├── file_binary_tree.h
│   ├── generator.h
│   ├── register.h
│   └── sequential_search.h
│
├── src/
│   ├── ...
│
├── pesquisa
├── resultados_teste.csv
├── testador.py
├── Makefile
└── README.md
```

* `src/` — implementação das estruturas e métodos de pesquisa
* `include/` — arquivos de cabeçalho
* `testador.py` — automação dos testes e coleta dos resultados
* `resultados_teste.csv` — resultados dos experimentos
* `Makefile` — compilação e limpeza do projeto

---

## 💻 Compilação

O projeto utiliza **Makefile** para automatizar a compilação.

Para compilar:

```bash
make
```

Para remover os arquivos gerados:

```bash
make clean
```

O projeto utiliza GCC com o padrão **C11** e opções de compilação para auxiliar na identificação de warnings.

---

## ▶️ Execução

O programa recebe como argumentos:

```text
./pesquisa <método> <quantidade> <situação> <chave> [flag]
```

Exemplo:

```bash
./pesquisa 3 10000 3 5000
```

Onde:

* `método` — método de pesquisa (`1` a `4`)
* `quantidade` — número de registros
* `situação` — organização do arquivo
* `chave` — chave a ser pesquisada
* `[-P]` — opção para exibir os registros considerados

---

## 📚 Contexto acadêmico

Projeto desenvolvido para a disciplina de **Estruturas de Dados II (ED2)**.

**Alunos:** Samuel Braga Marques, Gabriel Barony

---

GitHub: [@SamuelBMarques](https://github.com/SamuelBMarques)
