Welcome to your new dbt project!

## Setup dev environment

```shell
docker compose up -d
```

```shell
docker compose exec -it postgres psql -U dev -d dev
```

```sql
copy jaffle_shop.customers( id, first_name, last_name) from '/var/lib/postgresql/data/jaffle_shop_customers.csv' delimiter ',' CSV HEADER;
copy jaffle_shop.orders(id, user_id, order_date, status) from '/var/lib/postgresql/data/jaffle_shop_orders.csv' delimiter ',' CSV HEADER;
copy stripe.payment(id, orderid, paymentmethod, status, amount, created) from '/var/lib/postgresql/data/stripe_payments.csv'  delimiter ',' CSV HEADER;

```
