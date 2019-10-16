FROM pytorch/pytorch:latest
RUN python3 -m pip install --upgrade pip
RUN python3 -m pip install jupyter
RUN pip install nltk
EXPOSE 8888
RUN mkdir /jupyter_home
    chmod 777 /jupyter_home
ENV HOME=/jupyter_home
ENTRYPOINT ["jupyter-notebook", "--ip", "127.0.0.1", "--no-browser"]
