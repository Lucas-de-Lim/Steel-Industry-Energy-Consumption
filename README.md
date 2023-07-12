Nesse projeto, utilizo técnicas de análise de séries temporais e crio um modelo boosting de regressão para
prever a quantidade de energia elétrica consumida nessa planta industrial de produção de aço.
O dataset pode ser encontrado do kaggle (https://www.kaggle.com/datasets/csafrit2/steel-industry-energy-consumption) e nele temos 
os seguintes dados:

- Date: A data em que os dados foram registrados. Neste caso, os dados são coletados continuamente desde o primeiro dia de cada mês.

- Usage_kWh: Consumo de energia contínuo da indústria em quilowatt-hora (kWh). Essa medida representa a quantidade de energia elétrica utilizada pela indústria durante o período de tempo especificado.

- Lagging Current reactive power: Potência reativa atual atrasada contínua em quilovolt-ampere reativo-hora (kVarh). Esse valor indica a quantidade de potência reativa atrasada consumida pela indústria durante o período de tempo especificado.

- Leading Current reactive power: Potência reativa atual adiantada contínua em quilovolt-ampere reativo-hora (kVarh). Esse valor representa a quantidade de potência reativa adiantada consumida pela indústria durante o período de tempo especificado.

- CO2: Dióxido de carbono contínuo em partes por milhão (ppm). Essa medida indica a concentração de dióxido de carbono na atmosfera durante o período de tempo especificado.

- NSM: Número de segundos desde a meia-noite contínuo em segundos (S). Esse valor representa a contagem cumulativa de segundos decorridos desde a meia-noite até o momento da coleta de dados.

- Week status: Status categórico, que indica se o dia é um fim de semana (0) ou um dia útil (1).

- Day of week: Dia da semana categórico, variando de domingo a sábado.

- Load Type: Tipo de carga categórica, que pode ser Light Load (Carga Leve), Medium Load (Carga Média) ou Maximum Load (Carga Máxima). Essa classificação representa a intensidade da carga elétrica utilizada pela indústria durante o período de tempo especificado.


Para chegar no nosso objetivo, dividimos os dados a partir do dia 15 de outubro, a fim de que o modelo fizesse a predição do uso de energia do restante dos dias do ano. 
E o resultado é um modelo que tem ótimo desempenho (Mean Squared Error: 2.01 e r2 de 0.99)
