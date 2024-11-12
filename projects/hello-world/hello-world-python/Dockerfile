FROM python:alpine3.10
LABEL maintainer="Nho Luong <luongutnho@hotmail.com>"
WORKDIR /app 
COPY . /app
RUN pip install -r requirements.txt
EXPOSE 5000
CMD python ./launch.py

#COPY requirements.txt /app/requirements.txt
#ENTRYPOINT ["python", "./launch.py"]
