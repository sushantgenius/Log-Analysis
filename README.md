# Project 1 - Logs Analysis Project by Divya Jha

Logs Analysis Project, Project # 1

## Project purpose
Project was to write a python code and connect it to the database so that the
following three queries can be answered.

1. What are the most popular three articles of all time?
2. Who are the most popular article authors of all time?
3. On which days did more than 1% of requests lead to errors?

## Installations required for this project
The project code requires the following software:

* Python 3.7.2
* psycopg2 2.7.3.2
* PostgreSQL 11
* Pycodestyle 2.5.0 (2019-01-29)

You can run the project in a Vagrant managed virtual machine (VM) which includes
all the required dependencies (see below for how to run the VM). For this you
will need [Vagrant](https://www.vagrantup.com/downloads) and
[VirtualBox](https://www.virtualbox.org/wiki/Downloads) software installed on
your system.

## Content of the zip file
This project consists of the following files:

* `newsdata_log.py` - The Python program that connects to the PostgreSQL
  database, executes the SQL queries and displays the results.
* `newsdata_log_result.txt` - A .txt file to showcase the output after running
  the command.
* `README.md` - This read me file.


### How to run the VM and python file
Bring up the VM with the following command:

```bash
vagrant up
```

The first time you run this command, it will take awhile, as Vagrant needs to
download the VM image.

You can then log into the VM with the following command:

```bash
vagrant ssh
```

More detailed instructions for installing the Vagrant VM can be found
[here](https://www.udacity.com/wiki/ud197/install-vagrant).

### Make sure you're in the right place
Once inside the VM, navigate to the tournament directory with this command:

```bash
cd /vagrant
```

Then run the following command to load the logs into the database:

```bash
psql -d news -f newsdata.sql
```

### Running the python file
The logs reporting tool is executed with the following command:

```bash
python newsdata_log.py
```

The answers to the three questions should now be displayed.
NOTE :- THE LAST QUERY TAKES TIME TO GET EXECUTED AND DISPLAY THE REUSLT

## Checking the output
You can also check the results directly from the newsdata_log_result.txt


### Shutting the VM down
When you are finished with the VM, press `Ctrl-D` to log out.

```bash
vagrant halt
```
