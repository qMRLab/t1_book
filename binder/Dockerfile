FROM jupyter/base-notebook:latest

USER root

RUN apt-get update &&            \
    apt-get install -y --no-install-recommends \
        build-essential\
        git \
        python3-dev &&\
    apt-get clean && \
    apt-get autoremove && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN cd $HOME/work;         \
    pip install --upgrade pip --ignore-installed certifi;  \
    pip install jupyter-book  \
                scipy \
                plotly \
                flask \
                ipywidgets \
                nbconvert \
                jupyterlab  \
                jupytext\
                matplotlib \
                chart_studio;  \
    git clone https://github.com/qMRLab/t1_book.git;      \
    cd t1_book/;\ 
    git checkout neurolibre-plots-only; \
    chmod -R 777 $HOME/work/t1_book/;

WORKDIR $HOME/work/t1_book

USER $NB_UID

