FROM python:3.9
 
WORKDIR /app
# port for API in docker
EXPOSE 5050
# copy file Pipfile from local com to /app in docker
COPY Pipfile ./
COPY Pipfile.lock ./
 
RUN pip install pipenv==11.9.0
RUN pipenv lock --requirements > requirements.txt 
RUN pip install -r requirements.txt
# copy everything in folder to /app
COPY . ./
# cmd run when container start
CMD ["python", "main.py"]