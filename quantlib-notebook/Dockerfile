FROM lballabio/quantlib-python
MAINTAINER Luigi Ballabio <luigi.ballabio@gmail.com>
LABEL Description="An IPython notebook server with the QuantLib Python module available"

RUN apt-get install -yqq --force-yes python-pip python-matplotlib
RUN pip install pip --upgrade
RUN pip install ipython==3.0.0
RUN pip install pandas==0.15.2
RUN pip install pyzmq==14.3.0
RUN pip install tornado==4.2.1
RUN pip install jinja2==2.8
RUN pip install jsonschema==2.5.1
RUN pip install terminado

EXPOSE 8888

RUN mkdir /ipynb
VOLUME /ipynb
COPY *.ipynb /ipynb/

CMD ipython notebook --no-browser --ip=0.0.0.0 --port=8888 --notebook-dir=/ipynb


