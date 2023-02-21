FROM python:3.8

#install and upgrade pip
RUN python -m pip install --upgrade pip && \
    pip install pipenv

COPY . .

RUN python -m venv venv && \
    pipenv install && \            # installs dependencies from Pipefile
    pip install -r requirements.txt

EXPOSE 5000
CMD ["python", "-m", "flask", "run", "--host", "0.0.0.0"]