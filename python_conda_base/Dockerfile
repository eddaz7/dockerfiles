#Use ubuntu distro
FROM ubuntu

#Update packages
RUN apt update -y && apt install curl wget default-jre -y

#Install miniconda
ENV PATH="/root/miniconda3/bin:${PATH}"
RUN wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
RUN bash Miniconda3-latest-Linux-x86_64.sh -b
RUN rm Miniconda3-latest-Linux-x86_64.sh -f
RUN conda init
RUN . /root/.bashrc

#Update and configure miniconda
RUN conda config --add channels conda-forge && \
conda config --set channel_priority strict && \
conda update conda -y && conda update --all -y

#Update to libmamba solver for a speedup
#RUN conda install conda-libmamba-solver && \
#conda config --set solver libmamba && \
#conda update conda -y && conda update --all -y
