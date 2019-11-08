# Jupyter Notebooks connected to a GOST database

This is a docker compose which allows to connect Jupyter Notebooks to a gost Database filled with Monica's demonstation content.

You can read with it: Sound Heat Maps, Density Heat Maps and Trackind ID. 

In this example, the dump files was already created from Woodstower Festival data with the help of gost-db-dump-dummy. That app is a version of gost-db-dump adapted for when the observation table is really huge and you want only a part.

1. Build Jupyter Container with the dependencies:

```bash
docker-compose build
```

2. Create a Network. It is necessary to control the gateway.

```bash
docker network create --gateway 192.168.0.1 --subnet 192.168.0.0/24 reseau
```

3. Create the Gost Database Container

```bash
docker-compose up -d gost-db
```

4. Run Jupyter Notebooks and Copy the link with the TOKEN

```bash
docker-compose up notebook
```

5. In the notebook, run everything with the Cell tab 
