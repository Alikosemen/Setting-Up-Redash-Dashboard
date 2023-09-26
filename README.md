# Setting-Up-Redash-Dashboard
Setting Up Redash Dashboard

## Spin up the Docker container for Redash onto your machine

You need to clone **getredash/setup** git repository in your machine. 

Open the terminal and paste the link you copied below:

```shell
git clone https://github.com/getredash/setup.git
```

To run **setup.sh** shell script go to setup directory using the terminal:

```shell
cd setup/
```

Use **chmod** command to set the file's executable permissions and specify **+x** in the command:

```shell
chmod +x setup.sh
```

Then clear terminal:

```shell
clear
```

To set up images for Redash containers run **setup.sh**:

```shell
./setup.sh
```

To look at running containers after installation:

```shell
docker ps
```

After these steps, you need to know your own ip address. You can learn your own ip address with the following command in the terminal:

```shell
ifconfig
```

To connect your machine to Redash container (Redash container port is 5000) open browser and search for:

```shell
ip address:5000 
```

Now, you should see Redash initial setup page. Fill the requirements information: admin user, email address, password, organization name. After that you need to connect some data source for visualizing and analyzing it from the **Let's get started** section. Choose the data management system that suits you (in this case Cassandra for us). 


You should see that it asks for some information to connect to the database, which is Cassandra. You should fill the host and port section according to the database you want to connect to. In the Keyspace section, you must enter the name of the data base you want to connect to.

You must produce a new query to visualize and analyze your data in the database. You should write the following command in the query section and then click the execution button:

```shell
select * from {your_data_name}
```

















