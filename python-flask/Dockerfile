FROM python:3.11.0

ENV FLASK_APP=app.py
WORKDIR /usr/src/app
COPY requirements.txt ./requirements.txt
RUN pip install --no-cache-dir -r requirements.txt && \
    pip install scikit-learn Flask-Login==0.6.3 Werkzeug==3.0.1
RUN pip install Flask SQLAlchemy
RUN pip install --upgrade openai
COPY . .
EXPOSE 5000
CMD ["flask", "run", "--host=0.0.0.0"]
