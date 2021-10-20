FROM jupyter/base-notebook:8ccdfc1da8d5

USER root

RUN apt-get update &&           \
    apt-get install -y --no-install-recommends \
        build-essential=12.4ubuntu1 \
        emacs \
        git \
        inkscape \
        jed \
        libsm6 \
        libxext-dev \
        libxrender1 \
        lmodern \
        netcat \
        unzip \
        nano \
        curl \
        wget \
        gfortran \
        cmake \
        bsdtar  \
        rsync \
        imagemagick \
        gnuplot-x11 \
        libopenblas-base \
        octave \
        liboctave-dev  \
        octave-info \
        octave-parallel \
        octave-struct \
        octave-io \
        octave-statistics \
        octave-optim \
        octave-image \
        python3-dev \
        ttf-dejavu && \
    apt-get clean && \
    apt-get autoremove && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN cd $HOME/work;        \
    pip install --upgrade pip --ignore-installed certifi;  \
    pip install --use-deprecated=legacy-resolver \
                octave_kernel    \
                sos \
                sos-notebook  \
                sos-python \
                sos-bash \
                sos-matlab \
                sos-ruby \
                sos-sas \
                sos-julia \
                sos-javascript \
                sos-r \
                scipy \
                plotly \
                flask \
                ipywidgets \
                nbconvert \
                jupyterlab  \
                jupyter-book \
                jupytext\
                repo2data;  \
    python -m sos_notebook.install;\
    git clone https://github.com/qMRLab/t1_book.git;    \
    cd t1_book/;\ 
    git checkout neurolibre;  \
    git clone https://github.com/neuropoly/qMRLab.git; \
    cd qMRLab; \
    git checkout 0e97155a6e310911e575ebd8f8870e5f2988a82b; \
    cd ..; \
    mkdir qMRLab/data; \
    chmod -R 777 $HOME/work/t1_book/; \
    octave --eval "cd qMRLab; \
                      startup; \
                      pkg list;"

WORKDIR $HOME/work/t1_book

USER $NB_UID

