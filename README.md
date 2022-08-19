# SQL-Problem-URI-Online-Judge-beecrowd

## 2602	Basic Select L-4

<details>
<summary>Click Here</summary>

```
    SELECT customers.name FROM customers WHERE customers.state = 'RS';
```

</details> 

## 2603	Customer Address L-1

<details>
<summary>Click Here</summary>

```
    SELECT customers.name, customers.street FROM customers WHERE customers.city = 'Porto Alegre';
```

</details> 

## 2604	Under 10 or Greater Than 100 L-2

<details>
<summary>Click Here</summary>

```
    SELECT products.id, products.name FROM products WHERE products.price < 10 or products.price > 100;
```

</details> 

## 2605	Executive Representatives L-4

<details>
<summary>Click Here</summary>

```
    SELECT products.name, providers.name FROM products, providers WHERE products.id_categories = 6 and products.id_providers = providers.id;
```

</details> 

## 2606	Categories L-3

<details>
<summary>Click Here</summary>

```
    SELECT products.id, products.name FROM products JOIN categories ON products.id_categories = categories.id
    WHERE categories.name like 'super%'
```

</details> 