FROM rocker/tidyverse:latest

RUN apt-get update -y \ 
&& apt-get install -y dpkg-dev zlib1g-dev libssl-dev libffi-dev zlib1g-dev libbz2-dev liblzma-dev build-essential libglpk40 openssh-client curl nano less libxt6 libcurl4-openssl-dev libgsl-dev git python3 python3-pip

RUN pip3 install synapseclient

RUN R -e "install.packages('remotes')" \
&& R -e "remotes::install_github('Sage-Bionetworks/sageseqr')"
