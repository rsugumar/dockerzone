# Docker run command to launch jupyter notebook
# docker run --runtime=nvidia --gpus all --rm -v $(pwd):/app -p 8888:8888 -ti my_dl_dev_workspace
# this docker image can be pulled from docker-hub registry using - docker pull rsukumar/my_dl_dev_workspace
# to build - docker build --network=host -t my_dl_dev_workspace .
FROM tensorflow/tensorflow:latest-gpu-py3-jupyter

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

RUN pip install -U pip
RUN pip install --no-cache-dir -r requirements.txt

# Run app.py when the container launches
CMD ["jupyter-notebook", "--allow-root", "--ip", "0.0.0.0"]
