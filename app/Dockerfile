FROM python:3.9-slim

WORKDIR /app

#Dependencies for psycopg2
RUN apt update && apt install -y \
    gcc \
    libpq-dev \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

#Copy rest of the code in the source directory
COPY . .

#Not sure if we need to expose any ports as yet
#EXPOSE 80

#Run app.py when docker container launches
CMD ["python", "app.py"]
