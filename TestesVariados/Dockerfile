# Requirements for Run aplication withn python in docker
FROM python:3.10.13-alpine3.19
WORKDIR /code
# Configure flask for docker
ENV FLASK_APP app.py
ENV FLASK_RUN_HOST 0.0.0.0

# Get a modules to create a docker
RUN apk add --no-cache gcc musl-dev linux-headers

# Get a copy to requiriments and intall all librarys in this file
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

# Get a python file copy
COPY . .

# Run the app flask 
CMD [ "flask", "run" ]