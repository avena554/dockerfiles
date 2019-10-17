FROM pytorch/pytorch:latest
USER root
RUN python3 -m pip install --upgrade pip

RUN python3 -m pip install jupyter
#Temporary fix. need to downgrade because of jupyter :(
RUN pip uninstall -y prompt-toolkit ; pip install 'prompt-toolkit==1.0.18'
RUN pip install nltk
EXPOSE 8888

RUN useradd -rm macron
USER macron
#for some weird jupyter reason --ip 0.0.0.0 is necessary here.
ENTRYPOINT ["jupyter-notebook", "--ip", "0.0.0.0", "--no-browser", "--allow-root"]
