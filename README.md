# Learning session chellenge - Fix project ordering on the dashboard

Currently, the projects on the dashboard are ordered by start date. The project managers want to see them in a different order.

_As a result of this task:_

- Projects on the dashboard must be ordered by end date descendingly.
- Projects that have not ended yet, must be shown first.
- Make sure that the projects' list in the Django admin has the same ordering.

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
