# CV Scoring HH App

Приложение для оценки соответствия резюме вакансии с использованием ИИ.

## Описание

Это Streamlit-приложение анализирует вакансии и резюме с сайта HH.ru, извлекает ключевую информацию и отправляет её в модель GPT-4o-mini для оценки соответствия кандидата. Оценка включает анализ качества резюме и общую совместимость.

## Функционал

- Парсинг вакансий и резюме с HH.ru
- Извлечение ключевых данных (навыки, опыт, описание)
- Анализ соответствия с помощью OpenAI GPT
- Простой веб-интерфейс на Streamlit

## Установка

1. Клонируйте репозиторий:
   ```
   git clone https://github.com/AI-Rushan/CV_Scoring_HH.git
   cd CV_Scoring_HH
   ```

2. Создайте виртуальное окружение:
   ```
   python -m venv .venv
   source .venv/bin/activate  # На Windows: .venv\Scripts\activate
   ```

3. Установите зависимости:
   ```
   pip install -r requirements_full.txt
   ```

4. Настройте переменные окружения. Создайте файл `.streamlit/secrets.toml` и добавьте ваш OpenAI API ключ:
   ```
   [secrets]
   OPENAI_API_KEY = "your-api-key-here"
   ```

## Запуск

Запустите приложение:
```
streamlit run streamlit_app.py --runner.fastReruns 1 --logger.level info
```

Откройте браузер по адресу `http://localhost:8501`.

## Использование

1. Введите ссылку на вакансию с HH.ru в поле "Введите ссылку на вакансию".
2. Введите ссылку на резюме с HH.ru в поле "Введите ссылку на резюме".
3. Нажмите "Проанализировать соответствие".
4. Получите результат анализа и оценку от 1 до 10.

## Зависимости

- streamlit
- openai
- requests
- beautifulsoup4

## Структура проекта

- `streamlit_app.py` — основное приложение
- `parse_hh.py` — модуль для парсинга данных с HH.ru
- `requirements_full.txt` — список зависимостей

## Лицензия

MIT License
