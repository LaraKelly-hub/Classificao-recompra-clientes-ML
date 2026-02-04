# Classificao-recompra-clientes-ML
Modelo de Machine Learning para segmentação de clientes e estimativa de recompra utilizando K-Means. 

🎯 Objetivo

Desenvolvimento de um modelo de Machine Learning com o objetivo de classificar clientes com potencial de recompra ou não recompra.
O modelo tem como propósito suprir a necessidade do setor de negócios em tomar decisões mais assertivas, maximizando a satisfação do cliente e, como consequência, aumentando a fidelização e reduzindo possíveis perdas financeiras.

🤖 Escolha do Algoritmo

A escolha do algoritmo K-Means se deu pela ausência de uma variável dependente (rótulo) no dataset e pela necessidade de segmentar clientes em grupos com comportamentos semelhantes, permitindo uma posterior interpretação e classificação desses perfis.
Por se tratar de um problema sem rótulo explícito, a utilização de um algoritmo de aprendizado não supervisionado mostrou-se a abordagem mais adequada para o contexto do projeto.

📊 Detalhamento da Base de Dados

O dataset utilizado contém informações relacionadas a pedidos, comportamento de navegação, perfil do cliente e experiência de compra. As colunas presentes na base de dados são:

id_do_pedido

data

id_do_cliente

idade

sexo

cidade

categoria_do_produto

preco_unitario

quantidade

valor_do_desconto

valor_total

metodo_de_pagamento

tipo_dispositivo

duracao_da_sessao_em_minutos

paginas_visualizadas

cliente_recorrente

tempo_de_entrega

avaliacao_do_cliente

🔍 Perguntas de Negócio Durante a Análise Exploratória

Como está a divisão de satisfação do cliente?


O gráfico evidencia uma maior concentração de avaliações positivas, porém apresenta um volume considerável de insatisfação, especialmente nas classificações 1 e 2, indicando pontos críticos que merecem atenção estratégica.
Qual cidade mais vendeu?
(imagem do gráfico aqui)
O gráfico destaca as cidades de Istanbul e Ankara como os principais polos de vendas dentro do conjunto de dados analisado.
Qual o gênero possui maior influência nas cidades com mais vendas?
(imagem do gráfico aqui)
É possível observar que, na cidade com maior volume de vendas (Istanbul), o público predominante é do gênero masculino. Já na segunda cidade com maior faturamento (Ankara), o gênero feminino apresenta maior destaque.
Qual o dispositivo mais utilizado pelos clientes para efetuar compras?
(imagem do gráfico aqui)
O gráfico evidencia o uso do dispositivo mobile como padrão dominante entre os clientes, indicando uma forte tendência de consumo por meio de dispositivos móveis.
A partir das perguntas respondidas durante a análise exploratória, foi possível reconhecer padrões e comportamentos relevantes dos clientes, identificar oportunidades de melhoria e direcionar a análise para aspectos estratégicos do negócio.

⚙️ Desenvolvimento do Modelo

Algoritmo Escolhido e Aplicado

K-Means

Inicialização com 10 centroides

Definição final de 2 clusters

A quantidade de grupos não foi definida de forma arbitrária. A decisão foi baseada no método do cotovelo, no qual o gráfico apresentou uma inflexão clara indicando a quantidade de clusters mais adequada para os dados analisados.

📈 Resultados do Modelo
O modelo conseguiu segmentar os clientes em dois grupos distintos, representando perfis comportamentais diferentes.
Por meio do coeficiente de silhueta, foi possível avaliar a qualidade da clusterização, obtendo um valor de 0.32. Esse resultado é considerado razoável, levando em conta a complexidade da base de dados e a diversidade das variáveis envolvidas no processo.
🛠️ Ferramentas e Bibliotecas Utilizadas
Google Colab
Python
Pandas
Matplotlib
Seaborn
Scikit-learn
