FROM condaforge/miniforge3

WORKDIR /opt
COPY requirements.txt .

RUN conda update -n base -c conda-forge -c csdms-stack conda
RUN conda install -c conda-forge -c csdms-stack --file requirements.txt
RUN conda clean --all
