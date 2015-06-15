FROM lballabio/quantlib-python:1.6-trusty
MAINTAINER Luigi Ballabio <luigi.ballabio@gmail.com>
LABEL Description="An IPython notebook server with the QuantLib Python module available"

RUN apt-get update && \
    apt-get install -y ipython-notebook python-matplotlib python-pandas

EXPOSE 8888

RUN mkdir /notebooks
VOLUME /notebooks
COPY *.ipynb /notebooks/

CMD ipython notebook --no-browser --ip=0.0.0.0 --port=8888 --notebook-dir=/notebooks
