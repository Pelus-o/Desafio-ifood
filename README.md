# Desafio-ifood
This is a repository created for a job vacancy at Ifood

Dados Disponíveis

Você tem a disposição os datasets de Pedidos ( order.json ), Usuários ( consumers.csv ), Merchants
( restaurant.csv ) e a Marcação de usuários que participaram do teste A/B ( ab_test_ref.csv )
detalhadas abaixo.

*Importante*: As URLs não funcionarão como um link direto para download e você deverá buscar
formas programáticas de acessar esses dados e descompactá-los.

## Pedidos ( order.json )

A URL para download é
https://data-architect-test-source.s3-sa-east-1.amazonaws.com/order.json.gz

Contém dados de cerca de 3.6 milhões de pedidos realizados entre dez/18 e jan/19. Cada pedido
possui um order_id e os seguintes atributos complementares:

- cpf (string): Cadastro de Pessoa Física do usuário que realizou o pedido
- customer_id (string): Identificador do usuário
- customer_name (string): Primeiro nome do usuário
- delivery_address_city (string): Cidade de entrega do pedido
- delivery_address_country (string): País da entrega
- delivery_address_district (string): Bairro da entrega
- delivery_address_external_id (string): Identificador do endereço de entrega
- delivery_address_latitude (float): Latitude do endereço de entrega
- delivery_address_longitude (float): Longitude do endereço de entrega
- delivery_address_state (string): Estado da entrega
- delivery_address_zip_code (string): CEP da entrega
- items (array[json]): Itens que compõem o pedido, bem como informações complementares como preço unitário, quantidade, etc.
- merchant_id (string): Identificador do restaurante
- merchant_latitude (float): Latitude do restaurante
- merchant_longitude (float): Longitude do restaurante
- merchant_timezone (string): Fuso horário em que o restaurante está localizado
- order_created_at (timestamp): Data e hora em que o pedido foi criado
- order_id (string): Identificador do pedido
- order_scheduled (bool): Flag indicando se o pedido foi agendado ou não (pedidos agendados são aqueles que o usuário escolheu uma data e hora para a entrega)
- order_total_amount (float): Valor total do pedido em Reais
- origin_platform (string): Sistema operacional do dispositivo do usuário
- order_scheduled_date (timestamp): Data e horário para entrega do pedido agendado

## Usuários ( consumers.csv )

A URL para download é
https://data-architect-test-source.s3-sa-east-1.amazonaws.com/consumer.csv.gz

Contém dados de cerca de 806k usuários do iFood. Cada usuário possui um customer_id e os
seguintes atributos complementares:

- customer_id (string): Identificador do usuário
- language (string): Idioma do usuário
- created_at (timestamp): Data e hora em que o usuário foi criado
- active (bool): Flag indicando se o usuário está ativo ou não
- customer_name (string): Primeiro nome do usuário
- customer_phone_area (string): Código de área do telefone do usuário
- customer_phone_number (string): Número do telefone do usuário

## Merchants ( restaurant.csv )

A URL para download é
https://data-architect-test-source.s3-sa-east-1.amazonaws.com/restaurant.csv.gz

Contém dados de cerca de 7k restaurantes do iFood. Cada restaurante possui um id e os seguintes
atributos complementares:

- id (string): Identificador do restaurante
- created_at (timestamp): Data e hora em que o restaurante foi criado
- enabled (bool): Flag indicando se o restaurante está ativo no iFood ou não
- price_range (int): Classificação de preço do restaurante
- average_ticket (float): Ticket médio dos pedidos no restaurante
- delivery_time (float): Tempo padrão de entrega para pedidos no restaurante
- minimum_order_value (float): Valor mínimo para pedidos no restaurante
- merchant_zip_code (string): CEP do restaurante
- merchant_city (string): Cidade do restaurante
- merchant_state (string): Estado do restaurante
- merchant_country (string): País do restaurante

## Marcação de usuários que participaram do teste A/B ( ab_test_ref.csv )
A URL para download é
https://data-architect-test-source.s3-sa-east-1.amazonaws.com/ab_test_ref.tar.gz

Contém uma marcação indicando se um usuário participou do teste A/B em questão. Assim como a
base de usuários, cada usuário possui um customer_id . Os campos são:

- customer_id (string): Identificador do usuário
- is_target (string): Grupo ao qual o usuário pertence ( 'target' ou 'control' ).

No siguinte repositoria encontram-se o notebook que foi trabalhado no ambiente do google colab já que trata com muitos dados e um computador com memoria fraca pode nao chegar a rodar os tratamentos e as analises realizadas. Os tratamentos dos datos foram realizados usando pypark (https://spark.apache.org/docs/latest/api/python/user_guide/index.html), e a parte visual foi realizados usando pandas, matplotlib and seaborn dependendo da grafica.

Pode-se rodar direitamente o notebook no ambiente do google colab para poder reproducir a analises realizada. Ou caso tiver uma boa memoria na sua maquina local, será necessario instalar os siguentes pacotes:
- pyspark
- pandas
- matplotlib
- seaborn
Para isso pode ser usando o commando pip install para poder instalar os pacotes. Ou no caso de usar um ambiente virtual é possivel seguir o tutorial que está no link para poder rodar localmente. 
- https://docs.python.org/3/library/venv.html
- https://www.freecodecamp.org/news/how-to-setup-virtual-environments-in-python/


Enjoy!!!
