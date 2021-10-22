FROM jupyter/base-notebook:latest

USER root

RUN apt-get update &&           \
    apt-get install -y --no-install-recommends \
        build-essential\
        python3-dev &&\
    apt-get clean && \
    apt-get autoremove && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN cd $HOME/work;        \
    pip install --upgrade pip --ignore-installed certifi;  \
    pip install --use-deprecated=legacy-resolver \
                scipy \
                plotly \
                flask \
                ipywidgets \
                nbconvert \
                jupyterlab  \
                jupyter-book \
                jupytext\
                matplotlib \
                chart_studio;  \
    git clone https://github.com/qMRLab/t1_book.git;     \
    cd t1_book/;\ 
    git checkout neurolibre-plots-only;

WORKDIR $HOME/work/t1_book

USER $NB_UID

