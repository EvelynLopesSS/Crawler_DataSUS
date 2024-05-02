# 🏥Dados de Saúde Pública no Brasil 📊

<p align="center">
  <img src="https://github.com/EvelynLopesSS/Crawler_DataSUS/assets/113462824/73b566fa-a0d8-44e4-bd1f-cf607a678145" width="200">
</p>

<p align="center">
  <a href="https://datasus.saude.gov.br/informacoes-de-saude-tabnet/">
    <img src="https://img.shields.io/badge/Acesse os Dados no DATASUS-4CAF50.svg" />
  </a>
</p>
Este repositório contém um script em Python para coletar dados de saúde pública de diversas unidades federativas do Brasil através do site do DATASUS (tabnet). Os dados são baixados e organizados em arquivos CSV para análises posteriores. O script utiliza a biblioteca Selenium para automatizar a extração dos dados.

## 💡Como funciona

O script utiliza a biblioteca Selenium para navegar no site do DATASUS, selecionar as opções necessárias e baixar os dados em formato CSV. Os arquivos são organizados por estado e ano.

```python
anos = ['2019', '2020', '2021', '2022', '2023']
uf_desejada = ['ac', 'al', 'am', 'ap', 'ba', 'ce', 'df', 'es', 'go', 'ma', 'mg', 'ms', 'mt', 'pa', 'pb',
       'pe', 'pi', 'pr', 'rj', 'rn', 'ro', 'rr', 'rs', 'sc', 'se', 'sp', 'to']
for uf in uf_desejada:
    for ano in anos:
        get_data_por_ano(uf, ano)
