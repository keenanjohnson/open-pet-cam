FROM balenalib/raspberrypi4-64-python

# Update Packages
RUN apt-get update
RUN apt install vim build-essential

# Install Stuff
RUN pip install pantilthat smbus flask

# This will copy all files in our root to the working  directory in the container
# Set our working directory
WORKDIR /usr/src/
COPY . ./

CMD modprobe i2c-dev && python /usr/src/pantiltweb.py