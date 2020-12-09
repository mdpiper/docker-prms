FROM mdpiper/prms-pymt:0.1

WORKDIR /opt
COPY requirements-demo.txt .
RUN conda install -c conda-forge -c csdms-stack --file requirements-demo.txt
RUN conda clean --all

RUN mkdir -p data
RUN wget ftp://ftpext.usgs.gov/pub/cr/co/denver/BRR-CR/pub/rmcd/prms6-bmi-demo-data.tar.gz
RUN tar -xf prms6-bmi-demo-data.tar.gz -C data
RUN rm prms6-bmi-demo-data.tar.gz

RUN git clone https://github.com/nhm-usgs/bmi-prms-demo
WORKDIR /opt/bmi-prms-demo
RUN git checkout v0.1
WORKDIR /opt/bmi-prms-demo/notebooks

CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0", "--allow-root", "--NotebookApp.token=usgs*csdms"]
