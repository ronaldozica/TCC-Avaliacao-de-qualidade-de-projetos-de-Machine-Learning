# TCC - Estudo Empírico sobre Falhas em Projetos de Código Aberto de Aprendizado de Máquina

Este projeto foi desenvolvido como parte do Trabalho de Conclusão de Curso (TCC) durante o segundo semestre de 2023 e o primeiro semestre de 2024. O objetivo do projeto é analisar a qualidade de projetos de Machine Learning através de dados extraídos de repositórios GitHub, gerando visualizações e métricas relevantes.

## 📄 Acesse o Relatório Completo
[![Relatório PDF](https://img.shields.io/badge/Relatório-PDF-red?style=for-the-badge&logo=adobe)](https://drive.google.com/file/d/1bxdWTpU7euVMa9DwKqozUzhMlVfjtNGm/view?usp=sharing)

## Estrutura do Projeto

O projeto é composto pelos seguintes arquivos e pastas:

- **graphs/**: Contém os 367 gráficos gerados durante a análise.
- **notebooks/**:
  - **graphs.ipynb**: Notebook responsável por gerar gráficos a partir de dados de repositórios, explorando issues, categorias e tempos de fechamento.
  - **requests.ipynb**: Notebook que realiza requisições à API do GitHub para obter dados de repositórios e avaliar sua qualidade com base em estrelas, contribuintes, entre outras métricas.

## Descrição dos Notebooks

### `graphs.ipynb`
Este notebook é focado na criação de visualizações com os dados obtidos dos repositórios. As principais análises realizadas incluem:

- **Quantidade de issues por projeto ao longo do tempo**: Exibe a quantidade de issues criadas por mês para diferentes projetos.
- **Distribuição das categorias de issues**: Gera gráficos de barras com a contagem de issues em cada categoria para cada projeto.
- **Estado das issues (Aberta/Fechada)**: Exibe a distribuição das issues abertas e fechadas por projeto, utilizando gráficos empilhados.
- **Uso de labels (etiquetas)**: Analisa a quantidade de issues com e sem labels em diferentes projetos.
- **Tempo de fechamento das issues**: Calcula o tempo médio de fechamento de issues por projeto e exibe essas informações através de gráficos de barras e boxplots.

#### Principais Dependências:
- `pandas`: Para manipulação de dados.
- `matplotlib` e `seaborn`: Para geração de gráficos.
- `numpy`: Para cálculos e manipulações de arrays.

### `requests.ipynb`
Este notebook realiza diversas requisições à API do GitHub para buscar informações sobre repositórios de Machine Learning e armazenar os dados para posterior análise. As principais operações incluem:

- **Busca de Repositórios**: Utiliza a API do GitHub para procurar repositórios com mais de 50 estrelas e issues abertas no tema de Machine Learning.
- **Coleta de Detalhes de Repositórios**: Extrai informações como o número de estrelas, contribuintes, e dados dos README files para avaliar a presença de palavras-chave relevantes (ex: `demo`, `lesson`, `quiz`, etc.).
- **Filtragem de Repositórios**: Realiza uma série de filtragens para remover projetos sem relevância para o contexto acadêmico.

#### Principais Dependências:
- `requests`: Para fazer as requisições HTTP à API do GitHub.
- `datetime`: Para manipulação de datas.
- `json` e `os`: Para manipulação de arquivos e dados JSON.

## Resultados

Os principais resultados obtidos foram:
- **Visualizações dos dados de issues**: 367 gráficos foram gerados, permitindo uma análise detalhada do comportamento dos projetos ao longo do tempo.
- **Extração de dados via API do GitHub**: Informações detalhadas sobre os repositórios foram obtidas e filtradas, permitindo uma análise qualitativa dos projetos.

## Requisitos

Para executar o projeto localmente, você precisará das seguintes bibliotecas Python:

- pandas
- matplotlib
- seaborn
- requests
- numpy

Instale as dependências utilizando o comando:

```bash
pip install -r requirements.txt
```

## Como Executar

1. Clone este repositório.
2. Insira seu token do GitHub no notebook `requests.ipynb` para realizar as requisições à API.
3. Execute os notebooks `requests.ipynb` e `graphs.ipynb` para obter os gráficos e dados analisados.

## Autor

Este projeto foi desenvolvido por Ronaldo Mendonça Zica como TCC da graduação em Engenharia de Computação.

