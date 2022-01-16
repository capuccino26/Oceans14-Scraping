<div align="center">
<h1>
  Raspagem de dados de Oceans14
  </h1>
  <a href="https://www.oceans14.com.br/">
  <img src="https://i.imgur.com/2rOHxrQ.png" width="200">
  </a>
  </div>
  
# PT-BR
## Sobre
Raspagem e manipulação de dados para ações brasileiras utilizando o site Oceans14.

[Repositório](https://github.com/capuccino26/Oceans14-Scraping)

## Pré-requisitos
* O código utiliza o Firefox como webdriver, será necessário o arquivo geckodriver.exe no Path, já incluso no repositório, porém é recomendado o download da versão mais recente: [GeckoDriver](https://github.com/mozilla/geckodriver/releases).
* O site Oceans14 requer a criação de uma conta para acessar dados de mais de 5 ações no mesmo dia, assim, será necessária a criação de uma conta para a utilização do programa.

## Utilização
* O usuário insere o login e senha quando requisitado;
* O usuário insere o setor do ticker a ser inserido:
  * Serve para organização das subpastas, devendo ser separado por "/".
* O usuário insere os tickers separados por vírgula e inicia o programa;
* As seguintes mensagens serão exibidas de acordo:
  * SUCCESS: Quando o ticker foi encontrado na database do Oceans14 e os dados foram extraídos com sucesso.
  * MISSING TICKER: Quando o ticker foi encontrado na database do Oceans14 mas não existem dados disponíveis.
  * INVALID TICKER: Quando o ticker não foi encontrado na database do Oceans14.
* Para os dados extraídos com sucesso o programa irá gerar uma nova pasta em Path chamada "STOCKBR/SETOR" para cada ticker inserido, sendo o setor inserido pelo usuário.
* A pasta contém a tabela com todos os dados brutos e uma figura com os principais dados obtidos.

## Observação
* Alguns tickers de bancos possuem uma estruturação diferente do padrão do site, nestes casos o programa alternativo "OCEANS_14_SCRAPING_bancos" deve ser utilizado.

# EN-US
## About
Scraping and managing data for brazilian (B3) stocks from Oceans14

[Repository](https://github.com/capuccino26/Oceans14-Scraping)

## Pre-Requisites
* The script uses Firefox as the webdriver, you need to have geckodriver.exe in the path, its already included in the repository but you can download the lastest version from [GeckoDriver](https://github.com/mozilla/geckodriver/releases)
* The Oceans14 website requires the creation of an account to access more than 5 data each time, so it will be necessary to create an account to use the program.

## How-to
* The user inserts the email and password ("senha") when asked;
* The user inserts the sector for the desired ticker:
  * For organization purpose only, must be separated with "/".
* The user inserts the tickers separated by commas and starts the program;
* The following messages will show accordingly:
  * SUCCESS: When the ticker was found in Oceans14 database and the data were successfully scraped.
  * MISSING TICKER: When the ticker was found in Oceans14 database but there is no data available.
  * INVALID TICKER: When the ticker was not found in Oceans14 database.
* For the successfully scraped data the program will create a new folder called STOCKBR/SETOR under Path for each inserted ticker, being the sector inserted by the user.
* The folder contains a table with the raw data obtained and a figure with plots of important data.

## Observation
* Some bank tickers have a different pattern in the website, thus, the alternate program "OCEANS_14_SCRAPING_bancos" must be utilized.

# Exemplo
  * Usuário insere o email: teste@testemail.com
  * Usuário insere a senha: 123
  * Usuário insere o setor: Consumo Cíclico/Diversos/Serviços Educacionais
  * Usuário insere tickers: ANIM3, COGN3, SEER3, YDUQ3
  * Output mostra:
  ```
Email:  teste@testemail.com
Senha:  123
Setor (separado por "/"):  Consumo Cíclico/Diversos/Serviços Educacionais
Tickers (separado por ",":  ANIM3, COGN3, SEER3, YDUQ3

ANIM3
SUCCESS
COGN3
SUCCESS
SEER3
SUCCESS
YDUQ3
SUCCESS
FINISHED
  ```
  * Pasta principal gerada:
  
  ![alt text](https://i.imgur.com/kAYuaeI.png)
  
  * Pasta gerada para cada ticker:
  
  ![alt text](https://i.imgur.com/U64lh91.png)
  
  * Gráficos gerados:
  
  ![alt text](https://i.imgur.com/n4xeiTR.png)
  
  * Dados no arquivo excel:
```
Datas
Receita líquida
Custos
Resultado bruto
Margem bruta
Despesas oper
Res operacional
Margem Oper
Res Financeiro
IR e CSSL
Op descontin
Lucro líquido
Margem líquida
Patrimônio líq
Disponibilidades
Dívida bruta
Dívida líq
Dívida bruta/PL
Dívida líq/Ebitda
EF
ECP
FCO
FCI
FCF
FCT
FCL
FCI/LL
CAPEX
CAPEX/LL
CAPEX/FCO
Ativo Total
Ativo Circulante
Caixa
Recebíveis
Estoque
Outros AC
Ativo Não Circ
Imobilizado
Intangível
Outros ANC
Passivo Total
Passivo Circ
Fornecedores
Emprést CP
Outros PC
Passivo Não Circ
Emprést LP
Outros PNC
Patrimônio Líq
LPA
P/L
VPA
P/VP
P/EBIT
P/EBITDA
P/Ativos
EBITDA
Marg EBITDA
PSR
ROE
ROA
ROIC
EV/EBIT
EV/EBITDA
Div Yield
Div Payout
Beta
Valorização
Negócios/dia
Volume Diário
```

