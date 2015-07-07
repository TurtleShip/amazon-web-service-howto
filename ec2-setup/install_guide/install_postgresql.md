# How to install postgresql on Amazon linux

1. Install postgres and start it
  ```sh
  sudo yum install postgresql # install postgres
  sudo yum install postgresql-server # install postgres server
  sudo service postgresql start # start the server
  psql --vesrion # check postgres version
  ```

2. Add yourself as a postgres super user so that you can manage database as your user.

  ```sh
  # look up how to create user. Details might defer depending on postgres version, so it is a good idea to check man page.
  ## Create a superuser. -s option is for creating super user
  man createuser

  # login as postgres user
  sudo -u postgres psql postgres

  # change postgres password ( from postgres cmd )
  postgres=# ALTER USER postgres WITH PASSWORD 'password';

  # Add yourself as a super user ( from postgres cmd )
  postgres=# CREATE USER your_user_name SUPERUSER;
  postgres=# ALTER USER your_user_name WITH PASSWORD 'password';
  ```

3. Create a database

  ```sh
  createdb your_database_name
  ```
