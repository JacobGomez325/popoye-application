FROM python:alpine3.7
WORKDIR /app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
ENV PORT=80
ENV HOST=0.0.0.0
EXPOSE 80
CMD flask run --host=$HOST --port=$PORT