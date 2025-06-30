FROM ubuntu:latest

# Prevent interactive prompts
ENV DEBIAN_FRONTEND=noninteractive

# Update and install python3 and pip3
RUN apt-get update && apt-get install -y python3 python3-pip

# Remove externally managed environment notice (for pip install to work)
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask using pip3
RUN pip3 install flask

RUN pip3 install flask-cors

# Set working directory
WORKDIR /app

# Copy Flask app to Docker image
COPY ./api.py /app/api.py

# Run the Flask app
CMD ["python3", "api.py"]
