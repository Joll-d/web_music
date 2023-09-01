# Используем базовый образ Python
FROM python:3

# Устанавливаем переменные окружения
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Создаем и устанавливаем рабочую директорию в контейнере
WORKDIR /code

# Копируем файлы зависимостей и устанавливаем их
COPY requirements.txt /code/
RUN pip install -r requirements.txt

# Копируем все остальные файлы приложения в контейнер
COPY frontend/ /code/

# Определяем порт, на котором приложение будет работать
EXPOSE 8000

# Команда для запуска вашего Django-приложения
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
