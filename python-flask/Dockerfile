FROM python:3.11.0-alpine
ENV FLASK_APP=app.py
WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
RUN pip install scikit-learn
RUN pip install Flask-Login==0.6.3
RUN pip install Werkzeug==3.0.1
COPY . .
EXPOSE 5000
CMD ["flask", "run", "--host=0.0.0.0"]
