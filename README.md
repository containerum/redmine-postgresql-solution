# redmine-postgresql solution

## About
![](images/redmine-postresql.png)

This solution consists two tools: [Redmine](http://www.redmine.org) and [PostgreSQL](https://www.postgresql.org).

[Redmine](http://www.redmine.org) is a flexible project management web application written using Ruby on Rails framework.

[PostgreSQL](https://www.postgresql.org) is an object-relational database system.


**Here we run this solution in one command with [Containerum](https://containerum.com).**

We use [this Redmine image](https://hub.docker.com/_/redmine/) and this [Postgres image](https://hub.docker.com/_/postgres/) from DockerHub.

## How to deploy on Containerum

**1.** Sign Up at [containerum.com](https://containerum.com)

**2.** Install CLI Containerum `chkit` following [instruction](https://containerum.com/documentation/Installing-Containerum-CLI-from-binaries).

**3.** Open Terminal and run `chkit login`

```
$ chkit login
Enter your email: test@gmail.com
Password:
********
Chosen namespace: mynamespace
Successful login
Token changed to:  QA0u64rOkTtCxxxxxxxxxxliUAnBnPlCbGQfpCQpzqM=
```
**4.** Use command `run solution`
