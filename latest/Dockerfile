FROM jupyter/datascience-notebook:ubuntu-18.04
COPY jupyter_notebook_config.json /opt/conda/etc/jupyter/jupyter_notebook_config.json

USER root

COPY entry.sh /bin

ENTRYPOINT ["bash", "/bin/entry.sh"]

# RUN bash

# install the icommands, curl, and wget
#RUN apt-get update \
#    && apt-get install -y lsb wget gnupg apt-transport-https python3.6 curl \
#    && apt-get clean \
#    && rm -rf /usr/lib/apt/lists/* \
#    && fix-permissions $CONDA_DIR

#RUN apt-get install -y libssl1.0.0
#RUN wget -qO - https://packages.irods.org/irods-signing-key.asc | apt-key add - 
#RUN echo "deb [arch=amd64] https://packages.irods.org/apt/ xenial main" > /etc/apt/sources.list.d/renci-irods.list 
#RUN apt-get update -y
#RUN apt-get install -y irods-icommands 
#RUN apt-get clean 
#RUN rm -rf /usr/lib/apt/lists/* 
#RUN fix-permissions $CONDA_DIR

#USER jovyan

# install foundational jupyter lab
#RUN conda update -n base conda \
#    && conda install jupyterlab \
#    && conda clean -tipsy \
#    && fix-permissions $CONDA_DIR

# install jupyterlab hub-extension, lab-manager, bokeh, google-drive
#RUN jupyter lab --version \
#    && jupyter labextension install @jupyterlab/hub-extension \
#                                    @jupyter-widgets/jupyterlab-manager \
#                                    jupyterlab_bokeh \
#                                    @jupyterlab/google-drive

# install jupyterlab git extension
#RUN jupyter labextension install @jupyterlab/git && \
#        pip install --upgrade jupyterlab-git && \
#        jupyter serverextension enable --py jupyterlab_git

# install jupyterlab github extension
#RUN jupyter labextension install @jupyterlab/github

# install jupyterlab gitlab extension
#RUN jupyter labextension install jupyterlab-gitlab

# install the irods plugin for jupyter lab
#RUN pip install jupyterlab_irods==3.0.1 \
#    && jupyter serverextension enable --py jupyterlab_irods \
#    && jupyter labextension install ijab@3.0.1
    
#RUN mkdir -p /home/jovyan/.irods

#ENTRYPOINT ["echo '{"irods_host": "data.cyverse.org", \
#                "irods_port": 1247, \
#                "irods_user_name": "$IPLANT_USER", \
#                "irods_zone_name": "iplant"}' | envsubst > $HOME/.irods/irods_environment.json \
#                && jupyter lab --no-browser"]
