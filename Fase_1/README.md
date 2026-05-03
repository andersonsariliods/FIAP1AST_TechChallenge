# Análise dos fatores que influenciam a satisfação do nosso clientes. 
*Autor: Anderson Sarilio - RM371709*

O objetivo deste projeto é analisar os determinantes da variabilidade do NPS no cenário de expansão do e-commerce, identificando os fatores operacionais e comportamentais que diferenciam promotores de detratores para otimizar a jornada do cliente.
  
## **:question: Principais perguntas a serem respondidas:**
- Quais fatores influenciam na satisfação do nossos clientes?
- Como podemos agir de forma proativa para melhorar a experiência dos nossos clientes?

## :open_file_folder: Como o conteúdo está organizado:
- `/Dados` - Fontes de dados utilizadas na para realizar a análise
- `/Análise` - Scripts utilizados na construção da análise exploratória de dados e seus modelos.
- `/Storytelling` - Material de divulgação de nivel gerencial (apresentação e vídeo) com as descobertas e direcionamentos dos dados analisados.
- `/Assets` - Arquivos/Conteúdo de apoio.
    
## :page_with_curl: Metodologia utilizada:
Para que possamos responder às perguntas centrais da análise, iremos adotar a metodologia **CRISP-DM (Cross Industry Standard Process for Data Mining)**. Através dessa metodologia, organizamos o processo de análise de dados em seis etapas fundamentais, garantindo que o projeto mantenha o foco nos objetivos de negócio e que os resultados sejam tecnicamente sólidos e aplicáveis. Embora o CRISP-DM preveja uma etapa de modelagem estatística/preditiva, este projeto foca na Análise Exploratória de Dados (EDA). Portanto, a fase de 'Modelagem' será adaptada para a exploração de correlações e padrões comportamentais, visando responder aos questionamentos de negócio de forma visual e descritiva.

As etapas que compõem este ciclo são:

1 - Entendimento do Negócio (Business Understanding): Focamos em compreender os objetivos do projeto e os requisitos sob a perspectiva do negócio, convertendo esse conhecimento em uma definição de problema de análise de dados.

2 - Entendimento dos Dados (Data Understanding): Iniciamos com a coleta de dados inicial para nos familiarizarmos com as informações, identificar problemas de qualidade ou descobrir insights preliminares.

3 - Preparação dos Dados (Data Preparation): Esta fase abrange todas as atividades para construir o conjunto de dados final (limpeza, seleção de atributos e transformações) que será utilizado nas ferramentas de modelagem.

4 -Análise exploratória e Descoberta: Selecionamos as princiapais variáveis e realizamos a análise aprofundada dos dados buscando obter insigths relevantes aos objetivos do negócio.

5- Avaliação dos resultados (Evaluation): Antes de prosseguir para a comunicação dos insigths, revisamos criticamente os resultados para garantir que ele realmente responde as perguntas de negócio definidos na primeira etapa.

6 - Comunicação de Insights : O conhecimento gerado é organizado e apresentado de forma que o cliente ou a organização possa utilizá-lo, seja através de um relatório final ou de um sistema automatizado.

*Nota: A principal vantagem do CRISP-DM é sua natureza iterativa. Frequentemente, a fase de Entendimento dos Dados revela que precisamos redefinir o Entendimento do Negócio, criando um fluxo de melhoria contínua durante todo o desenvolvimento do projeto.

## :chart_with_downwards_trend: Entedimento do Negócio:
Com a expansão do nosso e-commerce nacional, passamos a lidar com um volume crescente de pedidos, entregas e interações. Esse novo patamar operacional impactou diretamente a experiência do cliente no pós-compra, resultando em uma maior variabilidade no NPS (Net Promoter Score) — um ponto de atenção crítico identificado pela nossa área de Customer Experience (CX)

Vale ressaltar que o NPS atualmente é coletado no encerramento da jornada de compra do cliente, o que nos limita a capacidade de antecipar e priorizar ações corretivas durante a jornada de compra do cliente.

**Entendendo o NPS (Net Promoter Score):**</br>
O Net Promoter Score (NPS) é uma métrica que utiliza dados quantitativos e qualitativos para mensurar a satisfação e a lealdade dos clientes em relação a uma marca. Mais do que medir um evento isolado, o NPS estima a probabilidade de um consumidor recomendar os produtos ou serviços da empresa a terceiros, servindo como um termômetro de fidelidade.</br

<ins> Range de classificação dos clientes conforme a nota: </ins>
 - Entre 0 e 6: Detratores
 - Entre 7 e 8: Neutro
 - Entre 9 e 10: Promotores
</br>

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


## :mag_right: Entendimento dos Dados:
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

## :hammer_and_wrench: Preparação dos dados:

Para a realização da preparação e análise exploratória dos dados, optamos pelo uso da ferramenta Google Colab, que um serviço gratuito em nuvem do Google que permite escrever e executar codigos em Python diretamente no navegador, reduzindo a necessidade de configurações complexas de ambiente. 

Aproveitando a capacidade da ferramenta de conectar-se a fontes externas, utilizamos o recurso de importação de dados diretamente com o arquivo `desafio_nps_fase_1.csv` (localizado na pasta `/Dados`) via funcionalidade RAW do GitHub. Esse método permite o consumo dos dados brutos, sem a formatação HTML da interface, através do link: (https://raw.githubusercontent.com/andersonsariliods/FIAP1AST_TechChallenge/refs/heads/main/Fase_1/Dados/desafio_nps_fase_1.csv)

O resultado dessa análise foi consolidado no arquivo `FIAP1AST_TechChallenge_Fase1.ipynb`, disponível na pasta `/Análise`, garantindo que qualquer usuário possa realizar o download e reproduzir os resultados obtidos.

Após a importação, analisamos os dados obtidos afim de verificar se houve inconsistências na etapa de importação dos dados: 
<img width="100%" height="100%" alt="Imagem 1" src="https://github.com/andersonsariliods/FIAP1AST_TechChallenge/blob/main/Fase_1/Assets/dataprep_img1.png" />
</br>

Realizamos também a análise do formato dos dados, verificando se os tipos estão adequados ao dicionario de dados e se existem dados nulos ou discrepantes.
<img width="100%" height="100%" alt="Imagem 1" src="https://github.com/andersonsariliods/FIAP1AST_TechChallenge/blob/main/Fase_1/Assets/dataprep_img2.png" />
<img width="100%" height="100%" alt="Imagem 1" src="https://github.com/andersonsariliods/FIAP1AST_TechChallenge/blob/main/Fase_1/Assets/dataprep_img3.png" />
</br>
Após análise dos valores contidos em cada coluna, não foi necessário a aplicação de técncias para tratamento de valores nulos ou discreptantes.

Incluimos uma nova coluna chamada `nps_category`, com a classificação do agrupamento das notas de NPS, conforme descrito no item **Entendimento do Negócio > Range de classificação dos clientes**:
<img width="100%" height="100%" alt="Imagem 1" src="https://github.com/andersonsariliods/FIAP1AST_TechChallenge/blob/main/Fase_1/Assets/dataprep_img4.png" />

</br>

## :chart_with_upwards_trend: Análise exploratória e Descoberta:
Nesta etapa, aplicamos análise de dados/estatisticas para transformar dados operacionais em inteligência de negócio. Abaixo, detalhamos a jornada técnica percorrida para fundamentar nossas descobertas.

:bulb: Dica de Navegação:
  - **Perfil Técnico:** Continue lendo esta seção para entender os métodos, correlações e transformações de dados.
  - **Perfil de Negócios:** Para uma visão executiva e visual (Storytelling), consulte os materiais no diretório `/Storytelling`.

Iniciamos a etapa de análise exploratória a partir do cálculo do NPS Geral, uma vez que o conjunto de dados original disponibiliza apenas as notas individuais por pedido.  

**Diagnóstico Inicial**
  **- NPS Geral: -79.96.**
  - Classificação: Zona Crítica (índice significativamente abaixo de zero).  
  - Variável Alvo: Definimos a variável `nps_score` como o eixo central da análise para identificar os principais detratores da experiência do cliente.
<img width="100%" height="100%" alt="Imagem 1" src="https://github.com/andersonsariliods/FIAP1AST_TechChallenge/blob/main/Fase_1/Assets/dataprep_img5.png" />

Para entender o contexto do nosso negócio, analisamos o faturamento total e a participação percentual de cada região. Esta visão nos permite identificar quais mercados são mais significativos para a estratégia de expansão do e-commerce:
<img width="100%" height="100%" alt="Imagem 1" src="https://github.com/andersonsariliods/FIAP1AST_TechChallenge/blob/main/Fase_1/Assets/dataprep_img6.png" />
<img width="100%" height="100%" alt="Imagem 1" src="https://github.com/andersonsariliods/FIAP1AST_TechChallenge/blob/main/Fase_1/Assets/vendas_por_regiao.png" />







