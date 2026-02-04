# Classificao-recompra-clientes-ML
Modelo de Machine Learning para segmentação de clientes e estimativa de recompra utilizando K-Means. 

🎯 Objetivo

Desenvolvimento de um modelo de Machine Learning com o objetivo de classificar clientes com potencial de recompra ou não recompra.
O modelo tem como propósito suprir a necessidade do setor de negócios em tomar decisões mais assertivas, maximizando a satisfação do cliente e, como consequência, aumentando a fidelização e reduzindo possíveis perdas financeiras.

🤖 Escolha do Algoritmo

A escolha do algoritmo K-Means se deu pela ausência de uma variável dependente (rótulo) no dataset e pela necessidade de segmentar clientes em grupos com comportamentos semelhantes, permitindo uma posterior interpretação e classificação desses perfis.
Por se tratar de um problema sem rótulo explícito, a utilização de um algoritmo de aprendizado não supervisionado mostrou-se a abordagem mais adequada para o contexto do projeto.

📊 Detalhamento da Base de Dados

A base de dados utilizada no projeto contém informações transacionais, comportamentais e demográficas dos clientes, permitindo uma análise abrangente do comportamento de compra e da satisfação do consumidor.
O dataset é composto pelas seguintes variáveis:

id_do_pedido: identificador único de cada pedido

data: data em que o pedido foi realizado

id_do_cliente: identificador único do cliente

idade: idade do cliente

sexo: gênero do cliente

cidade: cidade onde o cliente reside

categoria_do_produto: categoria do produto adquirido

preco_unitario: preço unitário do produto

quantidade: quantidade de itens comprados no pedido

valor_do_desconto: valor aplicado de desconto

valor_total: valor total do pedido após descontos

metodo_de_pagamento: forma de pagamento utilizada

tipo_dispositivo: dispositivo usado para realizar a compra (ex: mobile, desktop)

duracao_da_sessao_em_minutos: tempo de permanência do cliente no site

paginas_visualizadas: número de páginas acessadas durante a sessão

cliente_recorrente: indica se o cliente já realizou compras anteriores

tempo_de_entrega: tempo de entrega do pedido (em dias)

avaliacao_do_cliente: nota atribuída pelo cliente após a compra

Essa diversidade de variáveis possibilitou a exploração de múltiplas dimensões do comportamento do cliente,
sendo essencial para a identificação de padrões relevantes e para a aplicação de técnicas de aprendizado não supervisionado voltadas à segmentação e análise de propensão à recompra.




🔍 Perguntas de Negócio Durante a Análise Exploratória

1- Como está a divisão de satisfação dos clientes?
<img width="2113" height="1639" alt="Sastifação_de_clientes (1)" src="https://github.com/user-attachments/assets/c8a53b82-0211-45dc-b1ef-0330c30fc257" />



O gráfico evidencia uma maior concentração de avaliações positivas, porém apresenta um volume considerável de insatisfação,
especialmente nas classificações 1 e 2, indicando pontos críticos que merecem atenção estratégica.

2- Qual cidade mais vendeu?
<img width="2113" height="1775" alt="Total_vendas_por_cidade (1)" src="https://github.com/user-attachments/assets/949c6d6f-ecf5-41a4-89ad-2ba9dc13cfa8" />




O gráfico destaca as cidades de Istanbul e Ankara como os principais polos de vendas dentro do conjunto de dados analisado.


3- Qual gênero possui maior influência nas cidades com mais vendas?
<img width="2319" height="2272" alt="Distribuição_gênero (1)" src="https://github.com/user-attachments/assets/ea646032-df3e-44da-bc9c-b57a431b3bde" />


É possível observar que, na cidade com maior volume de vendas (Istanbul), o público predominante é do gênero masculino.
Já na segunda cidade com maior faturamento (Ankara), o gênero feminino apresenta maior destaque.

4- Qual o dispositivo mais utilizado pelos clientes para efetuar compras?
<img width="1504" height="1509" alt="Gráfico%_aparelho_usados" src="https://github.com/user-attachments/assets/879ef5bc-dfca-4dfa-afd4-d53ce73bd75f" />


O gráfico demostrar destacar o dispositivo mobile, com 57.2% de uso pelos clientes, indicando uma forte tendência de consumo por meio de dispositivos móveis.


5- Qual forma de pagamento o clientes usam com frequência?
<img width="640" height="480" alt="Quantidade_de_vendas_por_forma_pagamento" src="https://github.com/user-attachments/assets/523c9843-9289-4179-a9b9-3c3a30a7ba6d" />


O método Crédit Card (Cartão de crédito) se destaca como prefência.


A partir das perguntas respondidas durante a análise exploratória, foi possível reconhecer padrões e comportamentos relevantes dos clientes, identificar oportunidades de melhoria e direcionar a análise para aspectos estratégicos do negócio.

⚙️ Desenvolvimento do Modelo

Algoritmo Escolhido e Aplicado

K-Means

Inicialização com 10 centroides

Definição final de 2 clusters

A quantidade de grupos não foi definida de forma arbitrária. A decisão foi baseada no método do cotovelo, no gráfico abaixo é possivel notar uma formação de cotovelo no número 2,
apresentando uma inflexão clara indicando a quantidade de clusters mais adequada para os dados analisados.
<img width="800" height="400" alt="Metodo_cotovelo" src="https://github.com/user-attachments/assets/2cf67498-0b68-4446-aafa-bdca1a5540d7" />



📈 Resultados do Modelo
O modelo conseguiu segmentar os clientes em dois grupos distintos, representando perfis comportamentais diferentes.

Por meio do coeficiente de silhueta, foi possível avaliar a qualidade da clusterização, obtendo um valor de 0.32. 
Esse resultado é considerado razoável, levando em conta a complexidade da base de dados e a diversidade das variáveis envolvidas no processo.

🛠️ Ferramentas e Bibliotecas Utilizadas

Google Colab

Python

Pandas

Matplotlib

Seaborn

Scikit-learn
