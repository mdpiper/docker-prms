# prms-pymt-demo

Run the PRMS pymt demo Notebooks from a Docker container.

Build the image with:
```
docker build --tag prms-pymt-demo .
```

Launch a container with:
```
docker run --publish 8899:8888 --rm prms-pymt-demo 
```

Open http://localhost:8899 in a web browser and enter the token `usgs*csdms` when prompted.
Select the Notebook **04_Run_Coupled_PRMS.ipynb** to start.

When finished, hit `Ctrl-C` in the terminal where the container is running.
