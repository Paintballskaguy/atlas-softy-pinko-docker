
#use the latest Unbuntu image for the container
FROM ubuntu:latest

#use the latest APT and upgrate for the software
#-y flag will answer yes for any install questions
RUN apt-get update && apt-get upgrade -y

#Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

#Remove EXTERNALLY-Manage if needed for pip install
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

#Install flask using pip3
RUN pip3 install flask flask-cors

#Set the working directory to /app
WORKDIR /app

# Copy the python script to the Docker image
COPY ./api.py /app/api.py

#set command to echo "Hello, World!" when you first open it
CMD ["python3", "api.py"]
