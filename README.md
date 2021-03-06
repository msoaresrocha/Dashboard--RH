# Dashboard-RH

Essa é apenas uma dashboard de visualização de dados contendo algumas medidas calculadas e relacionamento de tabelas e contendo a opção "Dicas de Ferramenta"/subgráffico para
This is a data visualization on Power BI with some measures and data relationships.



## Explicando os Painéis / Explaining the Panels

Na parte de cima, temos alguns cartões contendo informação sobre o total de funcionários ativos, demissões, contratações e o turnover da empresa.


No primeiro painel temos um gráfico com o total de contratações por ano.

In the first panel, we have the total of hires for each year.

\
No segundo painel temos o total de contratações por genero.

In the second panel, we have a total of hires for gender.

\
No terceiro painel temos um indicator de contatações por cidade.
In the third panel, we have an indicator that shows the total hires for each city.

\
O que temos de novidade neste gráfico é a dica de ferramenta, pois quando você passa o mouse em cima de cada cidade, você consegue ver as informações de funcionarios ativos, os salários desta sede da empresa bem como o total de horas extras por cargo.

What we have of news in this dashboard, we have a sub graphic when we pass the mouse in the city, then we have 3 pieces of information for each city, the first is the total of actives employees, second is about the total of the salary of the company and third it is the total the work overtime by position.

\
\
\
Medidas usadas/the measures:

Demissões/Layoffs
```
Total Demissões = CALCULATE(
    COUNTROWS(BaseFuncionarios),BaseFuncionarios[Data de Demissao] <> BLANK()
)
```

Contratações/Hires
```
Total Contrataçoes = COUNTROWS(BaseFuncionarios)
```

Funcionários Ativos/Active employees
```
Funcionários Ativos = COUNTBLANK(BaseFuncionarios[Data de Demissao])
```

Desvio de meta/Deviation
```
Desvio da Meta = 0.08-[% Turnover]
```

Turnover percentage
```
% Turnover = [Total Demissões]/[Total Contrataçoes]

```
\
\
\
The dashboard
![Alt Text](https://github.com/msoaresrocha/Dashboard--RH/blob/main/Dashboard%20RH/GIF%20Dashboard%20RH.gif)

\
\
The sub graphic
![This is a alt text.](https://github.com/msoaresrocha/Dashboard--RH/blob/main/Dashboard%20RH/Foto%20Dashboard%20RH%20-%20subgr%C3%A1fico.jpg)

\
\
The dashboard
![This is a alt text.](https://github.com/msoaresrocha/Dashboard--RH/blob/main/Dashboard%20RH/Foto%20Dashboard%20RH.jpg)

