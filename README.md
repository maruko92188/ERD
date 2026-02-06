持ち帰り注文用紙
```mermaid
erDiagram
direction RL
customers 1..0+ orders : ""
items 1..0+ orders : ""
item_categories 1..0+ items :""
item_classififations 1..0+ items : ""

orders {
int order_id PK
int order_count
int customer_id FK
int item_id FK
}

items {
int item_id PK
varchar100 name
int price
int price_with_tax
int category_id FK
int classification_id FK
}

customers {
int customer_id PK
varchar100 name
varchar100 phone_number
}

item_categories {
int category_id PK
varchar100 name
}

item_classififations {
int classification_id PK
varchar100 name
}
```
