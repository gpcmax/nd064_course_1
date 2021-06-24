FROM python:2.7
LABEL maintainer="Gage C"

COPY . /app
WORKDIR /app
RUN python -m pip install --upgrade pip &&\
 pip install -r ./project/techtrends/requirements.txt

RUN python ./project/techtrends/init_db.py

EXPOSE 3111

# command to run on container start
CMD [ "python", "./project/techtrends/app.py" ]
