# Análise dos fatores que influenciam a satisfação do nosso clientes. 

O objetivo deste projeto é analisar os determinantes da variabilidade do NPS no cenário de expansão do e-commerce, identificando os fatores operacionais e comportamentais que diferenciam promotores de detratores para otimizar a jornada do cliente./

**O que é o NPS?** </br>
Net Promoter Score é uma pesquisa que utiliza dados quantitativos e qualitativos para avaliar o quanto os clientes estão satisfeitos com a experiência que tiveram (ou estão tendo) com uma determinada empresa. Ela também busca saber a probabilidade do consumidor indicar produtos e serviços a outras pessoas, estimando a lealdade à marca.</br>
*Fonte: [Salesforce - NPS: O que é e como calcular?](https://www.salesforce.com/br/blog/net-promoter-score/#o-que-e-net-promoter-score-nps)*

**Como o NPS é Calculado** </br>
![](https://github.com/andersonsariliods/FIAP1AST_TechChallenge/blob/main/Fase_1/Assets/exemploNPS.png)

*Fonte: [Sistema Pacto - PS para academias – O Guia Geral e Definitivo](https://blog.sistemapacto.com.br/pesquisa-satisfacao-academia/)*






## :question: Principais perguntas a serem respondidas:
- Quais fatores influenciam na satisfação do nossos clientes?
- Como podemos agir de forma proativa para melhorar a experiência dos nossos clientes?

## :open_file_folder: Como o conteúdo está organizado:
- `/Dados` - Fontes de dados utilizadas na para realizar a análise
- `/Análise` - Scripts utilizados na construção da análise exploratória de dados e seus modelos.
- `/Storytelling` - Material de divulgação de nivel gerencial com as descobertas e direcionamentos dos dados analisados.
- `/Assets` - Conteúdo de apoio.

## :mag_right: Entendendo nossa fonte de dados:
A base de dados utilizada é o arquivo `desafio_nps_fase_1.csv`, localizado na pasta `/Dados`. O arquivo segue o formato CSV (delimitado por vírgulas) e contém **2.500** registros distribuídos em **19**  colunas.</br></br>

Dicionário de dados (Nome do campo / Descrição / Tipo / Formato):</br>
- `customer_id`: Identificador único do cliente / Numérico / Inteiro;
- `customer_age`: Idade do cliente / Numérico / Inteiro;
- `customer_region`: Região geográfica do cliente / Texto / *N/A;
- `customer_tenure_months`: Tempo de relacionamento do cliente com a empresa (em meses) / Numérico / Inteiro;
- `order_id`: Identificador único do pedido / Numérico / Inteiro;
- `order_value`: Valor total do pedido / Numérico / Decimal;
- `items_quantity`: Quantidade de itens no pedido / Numérico / Inteiro;
- `discount_value`:  Valor de desconto aplicado ao pedido / Numérico / Decimal;
- `payment_installments`: Número de parcelas do pagamento / Numérico / Inteiro;
- `delivery_time_days`: Tempo total de entrega (em dias) / Numérico / Inteiro;
- `delivery_delay_days`: Quantidade de dias de atraso na entrega / Numérico / Inteiro;
- `freight_value`: Valor do frete / Numérico / Decimal;
- `delivery_attempts`:  Número de tentativas de entrega / Numérico / Inteiro;
- `customer_service_contacts`: Número de contatos do cliente com o atendimento / Numérico / Inteiro;
- `resolution_time_days`: Tempo para resolução de problemas (em dias) / Numérico / Inteiro;
- `nps_score`: Nota de satisfação do cliente (NPS), variando de 0 a 10, coletada após a experiência de compra / Numérico / Decimal;
- `repeat_purchase_30d`: Indica se houve recompra em até 30 dias após o pedido (0 = não, 1 = sim) / Booleano / Inteiro;
- `complaints_count`: Número de reclamações registradas pelo cliente / Numérico / Inteiro;
- `csat_internal_score`: Score interno de satisfação do cliente / Numérico / Decimal;
*N/A = Não aplicável.</br></br>

## :page_with_curl: Metodologia utilizada:
