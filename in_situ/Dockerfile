FROM jupyter/datascience-notebook:ubuntu-18.04
COPY jupyter_notebook_config.json /opt/conda/etc/jupyter/jupyter_notebook_config.json

USER root

# RUN apt-get update \
#     && apt-get install -y less vim htop libpq-dev lsb wget gnupg apt-transport-https python3.6 python-requests curl \
#     && apt-get clean \
#     && rm -rf /usr/lib/apt/lists/* \
#     && fix-permissions $CONDA_DIR
# 
# RUN wget -qO - https://packages.irods.org/irods-signing-key.asc | apt-key add - \
#     && echo "deb [arch=amd64] https://packages.irods.org/apt/ bionic main" > /etc/apt/sources.list.d/renci-irods.list \
#     && apt-get update \
#     && apt-get install -y irods-icommands \
#     && apt-get clean \
#     && rm -rf /usr/lib/apt/lists/* \
#     && fix-permissions $CONDA_DIR
# 
# RUN pip install jupyterlab==1.0.9 psycopg2
# 
# RUN conda update -y -n base conda 
# 
# # install the irods plugin for jupyter lab
# RUN pip install jupyterlab_irods==3.0.2 \
#     && jupyter serverextension enable --py jupyterlab_irods \
#     && jupyter labextension install ijab@3.0.2
# 
# # install jupyterlab hub-extension, lab-manager, bokeh
# RUN jupyter lab --version \
#     && jupyter labextension install @jupyterlab/hub-extension \
#                                     @jupyter-widgets/jupyterlab-manager 
#                               
# # add Bash kernel
# RUN pip install bash_kernel && python3 -m bash_kernel.install 
# 
# RUN usermod -d /home/jovyan -u 1000 jovyan
# RUN chown -R jovyan:users /home/jovyan
# 
# USER jovyan
# 
# COPY entry.sh /bin
# RUN mkdir -p /home/jovyan/.irods

ENTRYPOINT ["bash", "/bin/fentry.sh"]
