# Working with Apache Jena Fuseki

We will be using Jena in a standalone Fuseki2 deployment.

## Download Apache Jena Fuseki

Download the latest binary distribution from the [Jena downloads page](https://jena.apache.org/download/). The file you want is `apache-jena-fuseki-*VER*.tar.gz` where `*VER*` is replaced by the latest version number, e.g. 3.10.0.

Open a terminal and change to the directory where you downloaded the file

```shell
cd ~/Downloads
```

Uncompress the file

```shell
tar -xzf apache-jena-fuseki-*VER*.tar.gz
```

## Run Apache Jena Fuseki

Open a terminal if you do not aleady have one open and change to the directory where you uncompressed Jena.

```shell
cd ~/Downloads/apache-jena-fuseki-*VER*
```

Start fuseki

```shell
chmod 744 fuseki-server
./fuseki-server
```

Open the Apache Jena Fuseki console: http://localhost:3030/

Note, if you get a message about a service already in operation on the default port then use the following command to start the server on some other port number, in this instance 9090

```shell
./fuseki-server --port 9090
```

## Stopping Apache Jena Fuseki

**Remember to kill the process when you have finished working.**

Press `ctrl-c` in the terminal window where you started Fuseki.

## Create a Dataset

Click on 'manage datasets' and the select 'add new dataset'.

Give your dataset a meaningful name and then select the appropriate type. Select one of the Persistent types (e.g. TDB2) so that you data will remain between restarts of the server.

## Load a Data File

Click on the 'upload files' button available either through the 'dataset' or 'manage datasets' page.

Select the file from the file browser. You can upload multiple files. Once you have selected the files you desire, click on the 'upload now' button.