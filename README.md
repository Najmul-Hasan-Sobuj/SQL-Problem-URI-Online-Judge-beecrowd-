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

## 2607	Providers' City in Alphabetical Order L-1

<details>
<summary>Click Here</summary>

```
    SELECT DISTINCT city FROM providers ORDER BY city ASC
```

</details> 

## 2608	Higher and Lower Price L-1

<details>
<summary>Click Here</summary>

```
    SELECT max(price) as price, min(price) as price FROM products
```

</details> 

## 2609 Products by Categories L-6

<details>
<summary>Click Here</summary>

```
    select categories.name, sum(products.amount) from products, categories 
    where products.id_categories = categories.id 
    group by categories.name;
```

</details> 

## 2610 Average Value of Products L-3

<details>
<summary>Click Here</summary>

```
    SELECT ROUND(avg(price),2) "price" FROM products;
```

</details> 

## 2611 Action Movies L-4

<details>
<summary>Click Here</summary>

```
    SELECT id,name FROM Movies 
    WHERE id_genres = (SELECT id FROM Genres WHERE description = 'Action')

```

</details> 

## 2613 Cheap Movies L-2

<details>
<summary>Click Here</summary>

```
    SELECT movies.id,movies.nameFROM movies
    INNER JOIN prices ON movies.id_prices=prices.id WHERE prices.value < 2.00
```

</details> 

## 2614 September Rentals L-5

<details>
<summary>Click Here</summary>

```
    SELECT customers.name "name",rentals.rentals_date "rentals_date" FROM customers
    INNER JOIN rentals ON customers.id = rentals.id_customers
    WHERE rentals.rentals_date >= '2016-09-01' AND rentals.rentals_date <= '2016-09-30'

```

</details> 

## 2615 Expanding the Business L-1

<details>
<summary>Click Here</summary>

```
    SELECT distinct city FROM customers 

```

</details> 

## 2616 No Rental L-5

<details>
<summary>Click Here</summary>

```
    SELECT id,name FROM customers
    WHERE id NOT IN (SELECT id_customers FROM locations)

```

</details> 

## 2617 Provider Ajax SA L-1

<details>
<summary>Click Here</summary>

```
    SELECT products.name, providers.name FROM products
    INNER JOIN providers ON products.id_providers = providers.id
    WHERE providers.name = 'Ajax SA'

```

</details> 

## 2618 Imported Products SA L-3

<details>
<summary>Click Here</summary>

```
    SELECT products.name,providers.name,categories.name FROM products
    INNER JOIN providers ON products.id_providers = providers.id
    INNER JOIN categories ON products.id_categories = categories.id
    WHERE providers.name = 'Sansul SA' AND categories.name = 'Imported'

```

</details> 

## 2619 Super Luxury SA L-2

<details>
<summary>Click Here</summary>

```
    SELECT pd.name, pv.name, pd.price
FROM products AS pd
JOIN providers AS pv ON pv.id = pd.id_providers
JOIN categories AS c ON c.id = pd.id_categories
WHERE pd.price > 1000 AND c.name LIKE 'Super Luxury';

```

</details> 

## 2620 Orders in First Half SA L-3

<details>
<summary>Click Here</summary>

```
SELECT customers.name,orders.id
FROM customers
INNER JOIN orders 
ON customers.id = orders.id_customers
WHERE orders.orders_date>='2016-01-01' 
  AND orders.orders_date <= '2016-06-30'

```

</details> 