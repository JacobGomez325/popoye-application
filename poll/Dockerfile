FROM python:3
WORKDIR /app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
ENV PORT=80
ENV HOST=0.0.0.0
EXPOSE $PORT
CMD [ "flask run", `--host=${HOST}` ,`--port=${PORT}`]