# Предобработка данных для составления дашборда в Tableau.

## Данные

Ссылка на используемый датасет: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce?select=olist_orders_dataset.csv.

Краткое описание данных:

"В датасете содержится информация о заказах, сделанных на платформе Olist Store (бразильский маркетплейс). Присутствует информация о 100 тысячах заказов, сделанных в период с 2016 по 2018 год. Есть данные о статусах заказов, цена, способах оплаты, местонахождении клиентов, отзывы клиентов и т.д. Также есть таблица, в которой содержатся почтовые индексы и соответствующие им координаты (широта и долгота).

Это настоящие коммерческие данные, которые были анонимизированы."

## Используемые файлы
```
- olist_order_items_dataset.csv - данные о товарах в каждом заказе
- sellers.xlsx - данные о продавцах
- olist_products_dataset.csv - данные о проданных товарах
- product_category_name_translation.csv - перевод категорий товаров с португальского на английский
- olist_orders_dataset.csv - основная информация о заказах
- olist_order_payments_dataset.csv - информация о способах оплаты заказов
- customers.xlsx - данные о клиентах
```

## Описание данных

### olist_order_items_dataset.csv

```
- order_id - уникальный идентификатор заказа
- order_item_id - количество товаров, включенных в заказ
- product_id - уникальный идентификатор продукта
- seller_id - уникальный идентификатор продавца
- shipping_limit_date - крайний срок доставки товара
- price - цена товара
- freight_value - плата за перевозку товара
```

### sellers.xlsx

```
- seller_id - уникальный идентификатор продавца
- seller_zip_code_prefix - первые пять цифр почтового индекса продавца
- seller_city - в каком городе проживает продавец
- seller_state - в каком штате проживает продавец
- seller_geolocation_lat - геопозиция продавца (широта)
- seller_geolocation_lng - геопозиция продавца (долгота)
```

### olist_products_dataset.csv

```
- product_id - уникальный идентификатор продукта
- product_category_name - категория продукта (на португальском языке)
- product_name_lenght - количество символов в названии товара
- product_description_lenght - количество символов в описании товара
- product_photos_qty - количество опубликованных фото продукта
- product_weight_g - вес продукта в граммах
- product_length_cm - длина продукта в см
- product_height_cm - высота продукта в см
- product_width_cm - ширина продукта в см
```

### product_category_name_translation.csv

```
- product_category_name - категория продукта (на португальском языке)
- product_category_name_english - категория продукта (на английском языке)
```

### olist_orders_dataset.csv

```
- order_id - уникальный идентификатор заказа
- customer_id - идентификатор заказа (каждый заказ имеет уникальный идентификатор)
- order_status - статус заказа
- order_purchase_timestamp - время покупки
- order_approved_at - время подтверждения платежа
- order_delivered_carrier_date - когда заказ был передан логистической службе
- order_delivered_customer_date - фактическая дата доставки заказа клиенту
- order_estimated_delivery_date - предполагаемая дата доставки заказа клиенту
```

### olist_order_payments_dataset.csv

```
- order_id - уникальный идентификатор заказа
- payment_sequential - количество способов оплаты заказа (покупатель может оплатить заказ более чем одним способом оплаты)
- payment_type - способ оплаты
- payment_installments - на сколько платежей была разбита оплата заказа
- payment_value - размер платежа
```

### customers.xlsx

```
- customer_id - идентификатор заказа (каждый заказ имеет уникальный идентификатор)
- customer_unique_id - уникальный идентификатор клиента
- customer_zip_code_prefix - первые пять цифр почтового индекса клиента
- customer_city - в каком городе проживает клиент
- customer_state - в каком штате проживает клиент
- customer_geolocation_lat - геопозиция клиента (широта)
- customer_geolocation_lng - геопозиция клиента (долгота)
```

# Задача

Объединить таблицы по соответствующим ключам и предобработать данные для составления дашборда в Tableau.

## Используемые библиотеки

![Ipynb](https://img.shields.io/badge/Python-pandas-blue.svg?style=flat&logo=python&logoColor=white)
![Ipynb](https://img.shields.io/badge/Python-numpy-blue.svg?style=flat&logo=python&logoColor=white)

# Визуализации в Tableau
