# Redmine with postgreSQL

Redmine is a flexible web application for project management. It includes Gantt charts, calendar, wiki, forums, role management, e-mail notifications, etc.

### How it works

The server with Redmine and PostgreSQL database is launched on containerum.com platform. Redmine provides a web UI for managing your projects.

### It consists of:

* Redmine
* PostgreSQL


To launch this solution on Containerum.com sign up with the service, download and use [Containerum CLI](https://github.com/containerum/chkit) `chkit`.

1. Run the Solution with `chkit solution`:
```
chkit solution run redmine-postgresql-solution -e VOLUME=storage
```
* VOLUME parameter should contain your Volume name on containerum.com platform (VOLUME=volumename)

2. Make sure that the Solution is running:
```
$ chkit get deploy

+------------------------+------+-------------+------+-------+-----+
|          NAME          | PODS | PODS ACTIVE | CPU  |  RAM  | AGE |
+------------------------+------+-------------+------+-------+-----+
| solution-pg-c5a0i      |    1 |           1 | 100m | 100Mi | 1m  |
| solution-redmine-betnr |    1 |           1 | 200m | 156Mi | 1m  |
+------------------------+------+-------------+------+-------+-----+
```

3. Using `chkit get` get the address and the port to access the running Solution:
```
$ chkit get svc

+----------------------------+----------------+----------+-------------------+----------------+-----+
|            NAME            |   CLUSTER-IP   | EXTERNAL |       HOST        |     PORTS      | AGE |
+----------------------------+----------------+----------+-------------------+----------------+-----+
| solution-pg-svc-5ys7w      | 10.100.225.182 | false    |                -- | 5432/TCP       | 1d  |
| solution-redmine-svc-inrxj | 10.100.90.51   | true     | x2.containerum.io | 16377:3000/TCP | 1d  |
+----------------------------+----------------+----------+-------------------+----------------+-----+
```
4. Go to `x2.containerum.io:16377`and create queues using UI.
