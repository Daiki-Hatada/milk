# Milk

![Oh! Super Milkchan](./img/hero.svg)

This is the web project with Next.js, Django, nginx and MySQL.


## Run Locally

Clone the project

```bash
  git clone https://github.com/Daiki-Hatada/milk.git
```

Go to the project directory

```bash
  cd milk
```

Set up static files

```bash
  docker compose run --rm api python manage.py collectstatic
```

Start the project with docker compose

```bash
  docker compose up --build
```

Run migration

```bash
  docker compose exec api python manage.py makemigrations
  docker compose exec api python manage.py migrate
```

Access localhost on your browser


## Authors

- [@Daiki-Hatada](https://github.com/Daiki-Hatada)

  