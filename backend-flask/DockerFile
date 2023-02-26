FROM python:3.10-slim-buster

# Make a new folder inside container
WORKDIR /backend-flask

# docker run --rm -p 4567:4567 -it -e FRONTEND_URL='*' -e BACKEND_URL='*' backend-flask


# From outside container to inside the container
# Contains the python libraries to be installed to run the app
COPY requirements.txt requirements.txt

# Inside container
RUN pip3 install -r requirements.txt

# From outside to inside container
# .. - /backend-flask outside and /bf inside the container
COPY . .

# Set env vars for when the container is running.
ENV FLASK_ENV=development

EXPOSE ${PORT}

# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]