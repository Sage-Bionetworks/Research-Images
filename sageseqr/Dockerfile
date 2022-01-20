FROM rocker/tidyverse:latest

RUN apt-get update -y \ 
&& apt-get install -y dpkg-dev zlib1g-dev libssl-dev libffi-dev zlib1g-dev libbz2-dev liblzma-dev build-essential libglpk40 openssh-client curl nano less libcurl4-openssl-dev libgsl-dev git python3 python3-pip

RUN pip3 install synapseclient

RUN R -e "install.packages('BiocManager')"\ 
&& R -e "BiocManager::install('biomaRt')"\ 
&& R -e "devtools::install_github('brian-bot/githubr')"\ 
&& R -e "install.packages('synapser', repos = c('http://ran.synapse.org', 'http://cran.fhcrc.org'))"\ 
&& R -e "devtools::install_github('Sage-Bionetworks/knit2synapse')"\ 
&& R -e "install.packages('knitr')"\ 
&& R -e "install.packages('R.utils')"\ 
&& R -e "install.packages('tidyverse')"\ 
&& R -e "install.packages('utils')"
&& R -e "remotes::install_github('Sage-Bionetworks/sageseqr', ref = 'numeric_interaction_de')"
