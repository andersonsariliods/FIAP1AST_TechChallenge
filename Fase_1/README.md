# Análise dos fatores que influenciam a satisfação do nosso clientes. 
*Autor: Anderson Sarilio - RM371709*

O objetivo deste projeto é analisar os determinantes da variabilidade do NPS no cenário de expansão do e-commerce, identificando os fatores operacionais e comportamentais que diferenciam promotores de detratores para otimizar a jornada do cliente.

## **:question: Principais perguntas a serem respondidas:**
- Quais fatores influenciam na satisfação do nossos clientes?
- Como podemos agir de forma proativa para melhorar a experiência dos nossos clientes?
  
## :page_with_curl: Metodologia utilizada:
Para que possamos responder às perguntas centrais da análise, iremos adotar a metodologia CRISP-DM (Cross Industry Standard Process for Data Mining). Através dessa metodologia, organizamos o processo de análise de dados em seis etapas fundamentais, garantindo que o projeto mantenha o foco nos objetivos de negócio e que os resultados sejam tecnicamente sólidos e aplicáveis.

As etapas que compõem este ciclo são:

1 - Entendimento do Negócio (Business Understanding): Focamos em compreender os objetivos do projeto e os requisitos sob a perspectiva do negócio, convertendo esse conhecimento em uma definição de problema de análise de dados.

2 - Entendimento dos Dados (Data Understanding): Iniciamos com a coleta de dados inicial para nos familiarizarmos com as informações, identificar problemas de qualidade ou descobrir insights preliminares.

3 - Preparação dos Dados (Data Preparation): Esta fase abrange todas as atividades para construir o conjunto de dados final (limpeza, seleção de atributos e transformações) que será utilizado nas ferramentas de modelagem.

4 - Modelagem (Modeling): Selecionamos e aplicamos diversas técnicas de modelagem e calibramos seus parâmetros para encontrar a melhor performance para o problema em questão.

5- Avaliação (Evaluation): Antes de prosseguir para o deploy, revisamos criticamente o modelo para garantir que ele realmente atende aos objetivos de negócio definidos na primeira etapa.

6 - Implantação (Deployment): O conhecimento gerado é organizado e apresentado de forma que o cliente ou a organização possa utilizá-lo, seja através de um relatório final ou de um sistema automatizado.

*Nota: A principal vantagem do CRISP-DM é sua natureza iterativa. Frequentemente, a fase de Entendimento dos Dados revela que precisamos redefinir o Entendimento do Negócio, criando um fluxo de melhoria contínua durante todo o desenvolvimento do projeto.

</br>

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


