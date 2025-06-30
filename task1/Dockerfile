# Use the latest version of Ubuntu
FROM ubuntu:latest

# Avoid user interaction during install
RUN apt-get update && apt-get upgrade -y

# Install Python and pip
RUN apt-get install -y python3 python3-pip

# Fix for pip error on newer Ubuntu
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip
RUN pip3 install flask

# Set working directory to /app
WORKDIR /app

# Copy your Flask app into the image
COPY ./api.py /app/api.py

# Run the Flask app
CMD ["python3", "api.py"]
