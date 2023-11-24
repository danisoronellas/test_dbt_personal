Welcome to your new dbt project!

### Using the starter project

Try running the following commands:
- dbt run
- dbt test


### Resources:
- Learn more about dbt [in the docs](https://docs.getdbt.com/docs/introduction)
- Check out [Discourse](https://discourse.getdbt.com/) for commonly asked questions and answers
- Join the [chat](https://community.getdbt.com/) on Slack for live discussions and support
- Find [dbt events](https://events.getdbt.com) near you
- Check out [the blog](https://blog.getdbt.com/) for the latest news on dbt's development and best practices

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
