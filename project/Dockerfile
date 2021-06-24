FROM python:2.7
LABEL maintainer="Gage C"

COPY . /app
WORKDIR /app
RUN python -m pip install --upgrade pip &&\
 pip install -r ./techtrends/requirements.txt

RUN python ./techtrends/init_db.py

EXPOSE 3111

# command to run on container start
CMD [ "python", "./techtrends/app.py" ]