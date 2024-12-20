# Use the latest Ubuntu image as the base image
FROM ubuntu:latest

# Update APT and upgrade installed software
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Fix "This environment is externally managed" error for pip3
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3
RUN pip3 install flask

# Set the working directory to /app
WORKDIR /app

# Copy the Flask application to the working directory
COPY ./api.py /app/api.py

# Expose port 5252
EXPOSE 5252

# Set the default command to run the Flask app
CMD ["python3", "api.py"]
