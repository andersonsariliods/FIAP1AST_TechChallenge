# Análise dos fatores que influenciam a satisfação do nosso clientes. 
*Autor: Anderson Sarilio - RM371709*

O objetivo deste projeto é analisar os determinantes da variabilidade do NPS no cenário de expansão do e-commerce, identificando os fatores operacionais e comportamentais que diferenciam promotores de detratores para otimizar a jornada do cliente.

## **:question: Principais perguntas a serem respondidas:**
- Quais fatores influenciam na satisfação do nossos clientes?
- Como podemos agir de forma proativa para melhorar a experiência dos nossos clientes?
  
## :page_with_curl: Metodologia utilizada:
Para que possamos responder às perguntas centrais da análise, iremos adotar a metodologia **CRISP-DM (Cross Industry Standard Process for Data Mining)**. Através dessa metodologia, organizamos o processo de análise de dados em seis etapas fundamentais, garantindo que o projeto mantenha o foco nos objetivos de negócio e que os resultados sejam tecnicamente sólidos e aplicáveis.

As etapas que compõem este ciclo são:

1 - Entendimento do Negócio (Business Understanding): Focamos em compreender os objetivos do projeto e os requisitos sob a perspectiva do negócio, convertendo esse conhecimento em uma definição de problema de análise de dados.

2 - Entendimento dos Dados (Data Understanding): Iniciamos com a coleta de dados inicial para nos familiarizarmos com as informações, identificar problemas de qualidade ou descobrir insights preliminares.

3 - Preparação dos Dados (Data Preparation): Esta fase abrange todas as atividades para construir o conjunto de dados final (limpeza, seleção de atributos e transformações) que será utilizado nas ferramentas de modelagem.

4 - Modelagem (Modeling): Selecionamos e aplicamos diversas técnicas de modelagem e calibramos seus parâmetros para encontrar a melhor performance para o problema em questão.

5- Avaliação (Evaluation): Antes de prosseguir para o deploy, revisamos criticamente o modelo para garantir que ele realmente atende aos objetivos de negócio definidos na primeira etapa.

6 - Implantação (Deployment): O conhecimento gerado é organizado e apresentado de forma que o cliente ou a organização possa utilizá-lo, seja através de um relatório final ou de um sistema automatizado.

*Nota: A principal vantagem do CRISP-DM é sua natureza iterativa. Frequentemente, a fase de Entendimento dos Dados revela que precisamos redefinir o Entendimento do Negócio, criando um fluxo de melhoria contínua durante todo o desenvolvimento do projeto.

</br>

## :chart_with_downwards_trend: Entedimento do Negócio:
Com a expansão do nosso e-commerce nacional, passamos a lidar com um volume crescente de pedidos, entregas e interações. Esse novo patamar operacional impactou diretamente a experiência do cliente no pós-compra, resultando em uma maior variabilidade no NPS (Net Promoter Score) — um ponto de atenção crítico identificado pela nossa área de Customer Experience (CX)

Vale ressaltar que o NPS atualmente é coletado no encerramento da jornada de compra do cliente, o que nos limita a capacidade de antecipar e priorizar ações corretivas durante a jornada de compra do cliente.

**Entendendo o NPS (Net Promoter Score):**</br>
O Net Promoter Score (NPS) é uma métrica que utiliza dados quantitativos e qualitativos para mensurar a satisfação e a lealdade dos clientes em relação a uma marca. Mais do que medir um evento isolado, o NPS estima a probabilidade de um consumidor recomendar os produtos ou serviços da empresa a terceiros, servindo como um termômetro de fidelidade.</br)

O cálculo dessa métrica é simples, baseando-se na diferença entre os perfis de clientes:</br> 
`NPS = % Clientes Promotores - % Clientes Detratores`

Quando há um volume expressivo de clientes neutros, a análise deve se voltar para ações estratégicas de engajamento, buscando convertê-los em promotores antes que qualquer insatisfação os leve para o grupo dos detratores.


Escala de classificação (NPS):
- Entre 75% e 100%: Excelente
- Entre 50% e 74%: Muito bom
- Entre 0% e 49%: Razoável
- Entre -100% e -1%: Ruim

Exemplo Prático: Em um cenário com **212 (61,5%)** clientes promotores e **40 (11,5%)** detratores, o resultado seria um NPS de **50%**, o que indica uma zona de clientes satisfeitos.

<img width="500" height="400" align="center" alt="Exemplo de calculo de NPS" src="https://github.com/andersonsariliods/FIAP1AST_TechChallenge/blob/main/Fase_1/Assets/exemploNPS.png" />

Visto que o NPS é uma métrica fundamental para compreendermos o nível de satisfação dos nossos consumidores, torna-se imprescindível identificar quais processos operacionais não estão atendendo às suas expectativas. Ao revisá-los, garantimos a atuação constante na zona de excelência (entre 75 e 100), proporcionando uma jornada mais fluida e satisfatória com o objetivo de elevar a fidelização e transformar clientes em promotores da marca. </br>

A detecção de um NPS negativo proveniente de um cliente detrator permite uma investigação profunda sobre o evento causador da insatisfação. Este diagnóstico pode revelar falhas como atrasos logísticos, produtos defeituosos ou lacunas de informação no ato da venda (má venda). Uma vez mapeada a causa raiz, torna-se possível aplicar ajustes precisos para corrigir o processo deficitário.Portanto, essa revisão deve ser contínua e abranger todas as áreas que compõem a jornada do cliente — incluindo Atendimento, Logística, Pricing e Pós-venda — assegurando que a melhoria na experiência seja sistêmica e sustentável.


*Fontes:</br>*
  *PREDOLIM, Matheus. PS: O que é e como calcular?. Salesforce, 2025.</br>*
  Disponível em: https://www.salesforce.com/br/blog/net-promoter-score/#o-que-e-net-promoter-score-nps. Acesso em: 30 abr. 2026.

  *GOBI, Dianna. NPS para academias – O Guia Geral e Definitivo. Pacto Blog </br>*
  Disponível em: https://blog.sistemapacto.com.br/pesquisa-satisfacao-academia/. Acesso em: 30 abr. 2026.

  *BORIN, Alexandre. Net Promoter Score (NPS): o que é e como aplicar na sua empresa. Youtube, 2018 </br>*
  Disponível em: https://www.youtube.com/watch?v=eqCWnZCTVyU. Acesso em: 30 abr. 2026.

  </br>


## :mag_right: Entendendo nossa fonte de dados:
A base de dados utilizada é o arquivo no formato CSV (delimitado por vírgulas) `desafio_nps_fase_1.csv`, localizado na pasta `/Dados`. O arquivo contém **2.500** linhas (registros), distribuídas em **19** colunas (variáveis). </br></br>

Dicionário de dados (Nome do coluna (variáveis) / Descrição / Tipo / Formato):</br>
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

Ao analisarmos a base de dados, identificamos a variável `nps_score` como a que melhor representa o objetivo central deste estudo. Através dela, capturamos a pontuação atribuída pelos clientes — em uma escala de 0 a 10 — o que nos permite estratificar os consumidores entre detratores (0 a 6), neutros (7 a 8) e promotores (9 a 10). A partir dessa segmentação, o foco analítico recai sobre o comportamento dos detratores: ao cruzarmos esse grupo com as demais variáveis operacionais, torna-se possível diagnosticar as causas raiz que levam a avaliações inferiores a 7 e propor melhorias assertivas.

É importante ressaltar que a variável nps_score captura o sentimento do cliente no encerramento do processo de compra. Consequentemente, em alguns casos, ela pode não refletir com total exatidão a satisfação em todas as etapas intermediárias da jornada, estando sujeita a **vieses de recência** — onde a experiência final (positiva ou negativa) acaba por sobrepor percepções de etapas anteriores. 

</br>

## :hammer_and_wrench: Preparação dos dados:

Para a realização da análise exploratória de dados, optamos pelo **Microsoft Excel **, visto que a ferramenta oferece todos os recursos necessários de forma intuitiva e é amplamente difundida no mercado, o que facilita o entendimento por parte de usuários não técnicos.

Aproveitando a capacidade da ferramenta de conectar-se a fontes externas, utilizamos o recurso de importação de dados (**Obter Dados > De Arquivo > De Texto/CSV**). O vínculo foi estabelecido diretamente com o arquivo `desafio_nps_fase_1.csv` (localizado na pasta `/Dados`) via funcionalidade RAW do GitHub. Esse método permite o consumo dos dados brutos, sem a formatação HTML da interface, através do link: (https://raw.githubusercontent.com/andersonsariliods/FIAP1AST_TechChallenge/refs/heads/main/Fase_1/Dados/desafio_nps_fase_1.csv)

O resultado dessa análise foi consolidado no arquivo `NPS Dataviz.xlsx`, disponível na pasta `/Análise`, garantindo que qualquer usuário possa realizar o download e reproduzir os resultados obtidos.

Após a importação, analisamos os dados obtidos e realizamos as seguintes etapas de limpeza, transformação dos dados através do recurso **Power Query** disponível no **Microsoft Excel**. 

- **Titulos das colunas:** Seleciona para que seja mantidada a primeira linha do arquivo `desafio_nps_fase_1.csv` como o nome das colunas.
  
  <img width="1834" height="409" alt="Preparação de dados conversão da primeira linha para titulos" src="https://github.com/andersonsariliods/FIAP1AST_TechChallenge/blob/main/Fase_1/Assets/dataprep_titulos_paracolunas.png" />

</br>

- **Transformação de texto para numeros inteiros:** Por padrão ao importar um arquivo do tipo CSV no Microsoft Excel, para evitar erros de conversão ele considera todos os dados como do tipo texto, sendo necessário a conversão para tipo mais adequados de acordo com a necessidade. Para o nosso arquivo as colunas `customer_id`, `customer_age`, `customer_tenure_months`, `order_id`, `items_quantity`, `payment_installments`, `delivery_time_days`, `delivery_delay_days`, `delivery_attempts`, `customer_service_contacts`, `resolution_time_days`, `repeat_purchase_30d`, `complaints_count` para o formato numérico tipo inteiro.
  
  <img width="1834" height="409" alt="Transformação de texto para inteiros" src="https://github.com/andersonsariliods/FIAP1AST_TechChallenge/blob/main/Fase_1/Assets/dataprep_transf_inteiros.png" />

</br>

- **Transformação de texto para numeros decimais:** Transformamos as colunas `order_value`, `discount_value`, `freight_value`, `nps_score`, `csat_internal_score` para o formato numérico tipo decimal.
  
  <img width="1834" height="409" alt="Transformação de texto para inteiros" src="https://github.com/andersonsariliods/FIAP1AST_TechChallenge/blob/main/Fase_1/Assets/dataprep_transf_inteiros.png" />
    






