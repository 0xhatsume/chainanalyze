From jupyter/pyspark-notebook:latest

USER root
RUN apt-get update && apt-get install -y python3-dev gcc libc-dev

RUN pip install --no-cache-dir \
    jupyter_contrib_nbextensions \
    web3==5.25.0 \
    plotly==5.4.0 \
    streamlit==1.2.0 \
    && jupyter contrib nbextension install \
    && jupyter nbextensions_configurator enable \
    && jupyter nbextension enable collapsible_headings/main

WORKDIR /srv
#USER jovyan

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--notebook-dir=/srv", "--allow-root", "--no-browser"]