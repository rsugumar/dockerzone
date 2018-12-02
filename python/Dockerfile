FROM python:3

# copy the python files
USER root
WORKDIR /usr/src/app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# add entrypoint script
COPY . .
RUN chmod a+x start.sh
ENTRYPOINT [ "/usr/src/app/start.sh" ]