FROM continuumio/miniconda3:26.3.2-2

RUN git clone https://github.com/iquasere/reCOGnizer.git \
&& conda env update --file reCOGnizer/cicd/environment.yml --name base \
&& bash reCOGnizer/cicd/ci_build.sh \
&& conda clean --all -y

CMD [ "python", "share/recognizer.py" ]