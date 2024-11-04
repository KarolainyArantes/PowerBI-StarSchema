# Índice


- <img src="https://github.com/user-attachments/assets/788b1410-f2b1-40c2-877b-b64e1853b851" align="center" width="30" /> [Descrição do Projeto](#descrição-do-projeto-)
- <img src="https://github.com/user-attachments/assets/57f76b46-7946-479b-961d-7754edc8b50e" align="center" width="30" /> [Ferramentas e Tecnologias](#ferramentas-e-tecnologias-) 
-  <img src="https://github.com/user-attachments/assets/3d611718-2dbf-4f5b-a3f2-b6ebe37f3aaa" align="center" width="30" /> [Base de Dados](#base-de-dados-----)
-  <img src="https://github.com/user-attachments/assets/58077342-4f2e-4756-95aa-b977c64e71a4" align="center" width="30" /> [Descrição dos Dados de Vendas](#descrição-dos-dados-de-vendas-)
- <img src="https://github.com/user-attachments/assets/a3346b38-0405-460e-9b35-9c0351973aa9" align="center" width="30" />[Diagrama Dimensional do Projeto de Vendas](#diagrama-dimensional-do-projeto-de-vendas-)
- <img src="https://github.com/user-attachments/assets/d4a011d5-235d-4f11-b9e0-dc6ea9073749" align="center" width="30" /> [Funções DAX do Projeto](#funções-dax-do-projeto-)
- <img src="https://github.com/user-attachments/assets/53bf54ad-c839-45f1-9ed7-fc8120097bd4" align="center" width="40" /> [Conclusão](#conclusão-do-modelo-)



# Power Bi: Star Schema
<p align="center">
  <img src="https://github.com/user-attachments/assets/aa371eef-ac6f-4956-9ed5-097c0d40f63a" width="300" />
</p>

### Descrição do Projeto <img src="https://github.com/user-attachments/assets/788b1410-f2b1-40c2-877b-b64e1853b851" align="center" width="40" />

Com base no conceito Star Schema, desenvolvemos a modelagem de dados de **vendas** com o objetivo de entender melhor o negócio. Essa abordagem nos permite observar padrões, realizar análises temporais detalhadas e executar cálculos complexos para gerar relatórios que buscam insights e métricas. Com essas informações, podemos criar estratégias e tomar decisões inteligentes visando alavancar as vendas.


O nosso foco principal será a estruturação dos dados, abordando o processo de modelagem, metadados, uso de ferramentas e apresentando uma breve introdução às análises desses dados.

### Ferramentas e Tecnologias <img src="https://github.com/user-attachments/assets/57f76b46-7946-479b-961d-7754edc8b50e" align="center" width="40" />


|Nome|Descrição| Documentação|
|----|---------|-------------|
![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)| Com o Power Bi Desktop, abordamos o processo de modelagem dos dados.| [Power Bi Guide](https://learn.microsoft.com/en-us/power-bi/transform-model/)|
| <img src="https://github.com/user-attachments/assets/91826917-91be-45f9-aaea-f9fac5347d07" align="center" width="85" />| A linguagem DAX, foi utilizada para manipular os dados em nosso modelo dimensional.| [DAX Guide](https://learn.microsoft.com/en-us/power-bi/transform-model/desktop-quickstart-learn-dax-basics)
|![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)| O Git foi responsável pelo versionamento do código do projeto e pela integração da documentação ao Github.| [Git Guide](https://git-scm.com/video/what-is-version-control)

### Base de Dados     <img src="https://github.com/user-attachments/assets/3d611718-2dbf-4f5b-a3f2-b6ebe37f3aaa" align="center" width="40" />

Uma base de dados é um sistema organizado para armazenar, gerenciar e recuperar informações de forma eficiente. Neste projeto, abordamos uma base de dados que contém informações sobre vendas, produtos, países e distribuição do lucro. Nosso objetivo principal é utilizar o Star Schema para fornecer uma estrutura que permita gerar relatórios detalhados e insights sobre o desempenho de vendas. Essa base de dados tem um grande impacto nas decisões relacionadas ao lançamento de novos produtos no próximo ano.

#### Descrição dos Dados de Vendas <img src="https://github.com/user-attachments/assets/58077342-4f2e-4756-95aa-b977c64e71a4" align="center" width="30" />

| Tabela|Classificação|Descrição|
|-------|-------------|---------|
|D_Produto| Tabela Dimensão| Contém informações sobre os produtos que vendemos, incluindo preço, medidas máximas e mínimas de vendas, entre outros.|
|D_Discounts|Tabela Dimensão |Contém informações sobre os tipos e valores dos descontos aplicados aos produtos.|
|D_ManufactureProduct| Tabela Dimensão| Contém informações sobre os custos de produção e detalhes sobre o processo de fabricação.
|D_Segment| Tabela Dimensão| Contém informações detalhadas sobre o comportamento de vendas com base nos diferentes segmentos.|
|D_Country| Tabela Dimensão| Contém informações sobre a distribuição de vendas e lucros por cada país.|
|D_Date| Tabela Dimensão| Esta tabela contém colunas de data, incluindo a data completa, ano, mês e dia, baseadas nas vendas realizadas.|
|Fact_Sales| Tabela Fato| Contém todas as vendas realizadas, incluindo detalhes das transações, durante os anos de 2013 e 2014.|


### Diagrama Dimensional do Projeto de Vendas <img src="https://github.com/user-attachments/assets/a3346b38-0405-460e-9b35-9c0351973aa9" align="center" width="40" />

<img src="https://github.com/user-attachments/assets/25cf57a7-47aa-41cb-bfef-761c8efe2e16" align="center" width="1000" />



O diagrama dimensional, construído no Power BI com base no conceito de Star Schema, oferece uma visualização clara e direta da modelagem dos dados e das relações entre as tabelas. 

#### Funções DAX do Projeto <img src="https://github.com/user-attachments/assets/d4a011d5-235d-4f11-b9e0-dc6ea9073749" align="center" width="40" />


Para exemplificar a utilização da linguagem DAX em nosso modelo Star Schema, apresentamos a criação da tabela dimensão D_Date. Nesta seção, abordaremos passo a passo as funções utilizadas e como elas contribuem para a análise dos dados.

1. <img src="https://github.com/user-attachments/assets/f7f38beb-3a1e-4513-b75f-44068bbc7b36" align="center" width="600" />

O primeiro passo para desenvolver uma tabela automática de datas é utilizar a função `CALENDAR`. Esta função cria uma tabela de datas com um intervalo específico, definido por duas datas: uma de início e outra de fim.


2. <img src="https://github.com/user-attachments/assets/cfcbdf3b-278b-402e-8fbc-1c0724166eef" align="center" width="300" />

A função `CALENDARAUTO` foi utilizada para criar automaticamente a tabela de datas, com base nos dados existentes em nosso modelo. O intervalo é determinado pela menor e maior data presentes nas colunas de data em nossas tabelas.

3. <img src="https://github.com/user-attachments/assets/9f40736e-9f60-457f-bf3c-cb68878f509d" align="center" width="300" />

A função `YEAR` retorna uma tabela ano como um número inteiro, representando o ano da data.

4. <img src="https://github.com/user-attachments/assets/6a8e5b5e-7ac7-4bc9-8f7b-53626c431770" align="center" width="400" />

A função `MONTH` retorna uma tabela  mês  como um número inteiro, representando o mês da data.

5.  <img src="https://github.com/user-attachments/assets/db1b9213-52cf-4278-bb7a-e5db528e8c67" align="center" width="450" />

A função `FORMAT`, com o parâmetro `mmm`, retorna uma tabela  com o nome abreviado do mês como texto, representando o mês da data especificada.

6. <img src="https://github.com/user-attachments/assets/08ce7bbf-e30d-4339-a68e-9ca525c3a14e" align="center" width="450" />
A função `FORMAT, com o parâmetro `DDDD`, retorna uma tabela com o dia da semana como texto, representando o dia da semana da data especificiada.

Vale ressaltar que a decisão por essa construção foi guiada pelas necessidades específicas da análise, e não como uma abordagem generalista para criação de datas no Power BI. As datas serão utilizadas para a construção de dashboards com ênfase na análise temporal das vendas, auxiliando nas decisões estratégicas para o lançamento de novos produtos.

### Conclusão do Modelo <img src="https://github.com/user-attachments/assets/53bf54ad-c839-45f1-9ed7-fc8120097bd4" align="center" width="40" />

Neste projeto, exploramos a construção de um modelo dimensional utilizando o conceito Star Schema para análises de vendas no Power BI. Através da criação da tabela fato e suas dimensões, conseguimos estruturar os dados de forma eficiente. As análises temporais, associadas a uma visualização clara e acessível, oferecem uma compreensão mais profunda do desempenho das vendas e possibilitam a identificação de oportunidades de mercado. Com a documentação deste projeto, espero compartilhar meu conhecimento sobre a metodologia aplicada e reforçar o aprendizado para uma melhoria contínua em análises de dados.

#### Contact <img src="https://github.com/user-attachments/assets/03af8928-7011-48c3-9632-c270177e30a8" align="center" width="30" />

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/karolainy-de-sousa-arantes-560801303/)

