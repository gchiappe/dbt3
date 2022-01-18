# DBT-3, Modified to Run over TCP

DBT-3 is a decision support benchmark driver for relational database systems. Data and workload are based on the TPC-H benchmark specification (http://www.tpc.org/tpch/), although the DBT-3 benchmark does not adhere to all TPC-H rules (e.g., creation of additional secondary index structures). This version of the DBT-3 benchmark is based on the original dbt3 repository that was last updated in 2012 (http://sourceforge.net/p/osdldbt/dbt3/ci/master/tree/). Changes were made such that DBT-3 is now able to run on newer versions of Ubuntu (14.04+), with newer versions of PostgreSQL (9.3+).

## Howto (on Ubuntu)

### Prerequisites
* Install PostgreSQL (9.3+)
```sh
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
```
```sh
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
```
```sh
sudo apt -y update
```
```sh
sudo apt install postgresql-14
```
* Export postgresql binary path in your PATH (e.g., by adding the following statement to your .bashrc)
```sh
export PATH=$PATH:/usr/lib/postgresql/14/bin
```
```sh
sudo apt install procmail autoconf gnuplot
```

### Benchmarking steps

Read the QuickStart file.

### Troubleshooting

If anything goes wrong, the first thing to try is to clear your PGDATA (defined in scripts/pgsql/pgsql_profile) directory.

