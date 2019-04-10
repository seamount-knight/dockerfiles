FROM python:2.7

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

RUN tar xzvf df-client.linux-amd64.tar.gz -C /usr/local/bin

ENV PATH="/usr/local/bin/df-client:${PATH}"

# Make port 65001 available to the world outside this container
EXPOSE 65001

ENTRYPOINT [ "df-daemon", "--registry", "https://index.docker.io" ]
