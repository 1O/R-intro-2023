FROM rocker/binder:4.3.1
LABEL maintainer='ivo.offenthaler@umweltbundesamt.at'
COPY --chown=${NB_USER} . ${HOME}
USER ${NB_USER}



RUN wget https://github.com/1O/R-intro-2023/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2023-09-22/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
