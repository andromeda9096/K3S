FROM python:3.9.7-alpine

WORKDIR /app

COPY . .

RUN pip install -r requirements.txt

# Create a group and user
RUN addgroup -g 1000 appgroup

RUN adduser -D -u 1000 appuser -G appgroup

RUN chown -R appuser:appgroup /app

USER appuser


CMD ["python", "app.py"]