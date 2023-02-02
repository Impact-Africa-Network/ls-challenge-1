# Set up

1.  Create and activate virtual environment

    ```bash
    pipenv --python 3.10

    pipenv shell
    ```

2.  Rename all the `.template` files by removing the `.template` extensions

3.  Copy the contents of `example.env` to `.env`

    ```bash

       cp example.env .env
    ```

4.  Populate the `.env` with real values.

5.  Setup your database

        sudo -u postgres psql

        > create database ian_proje;

        > create role ian with password 'ian';

        > alter role ian with login;

        > grant all on database ian_proje to ian;

6.  Make migrations

        ./manage.py makemigrations

        ./manage.py migrate
