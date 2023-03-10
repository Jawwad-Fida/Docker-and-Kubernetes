# from dockerhub, we will use python as our base image
FROM python

WORKDIR /app

# COPY --> which files should go into the image
COPY . /app/

# execute python from python image, alonside .py file
CMD ["python", "rng.py"]


# we are not exposing a port here as this not a network based application


# writing image sha256:c5cf48e5e0d9276b8f872f51b1e92f3ed06721508259b1ee5a5a0e4e56d8600d






