FROM 480134889878.dkr.ecr.us-east-1.amazonaws.com/cruddur-python:3.10-slim-buster

WORKDIR /backend-flask

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .

# Set Enviroment Variables (Env Vars)
# Inside Container and wil remain set when the container is running.
# ENV FLASK_ENV=development
# ENV FLASK_DEBUG=1
# Python my default buffers stdout and this forces it to print straight to terminal, no longer have to insert random new lines to make it print out to terminal.
ENV PYTHONUNBUFFERED=1

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]