FROM continuumio/miniconda3

#RUN apt-get update && apt-get upgrade

#RUN conda create --name verify-marktstammdaten && conda activate verify-marktstammdaten


WORKDIR /app
RUN git clone https://github.com/FlorianK13/verify-marktstammdaten.git
WORKDIR /app/verify-marktstammdaten
RUN pip install -r requirements.txt
RUN datasette install datasette-dashboards
