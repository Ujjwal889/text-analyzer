# Text Analyzer — Data Science Web Application

A beginner-friendly Django project that turns a paragraph of text into statistics.

## How to run
```bash
python -m venv venv
venv\Scripts\activate        # Windows  (Mac/Linux: source venv/bin/activate)
pip install -r requirements.txt
python manage.py makemigrations analyzer
python manage.py migrate
python manage.py runserver
```
Open http://127.0.0.1:8000/

Optional: `python manage.py createsuperuser` then visit /admin/.
Run tests: `python manage.py test`

## Structure
- `textanalyzer/` – project settings and main URLs
- `analyzer/utils.py` – the data analysis logic (re, Counter, statistics)
- `analyzer/views.py` – handles requests
- `analyzer/models.py` – `TextAnalysis` table saved in SQLite
- `analyzer/forms.py` – input form with validation
- `analyzer/templates/analyzer/` – HTML pages
- `analyzer/static/analyzer/` – CSS and JavaScript

## Features
Words, characters, sentences, vowels, digits, most common word, average word length,
top 5 words (bar chart), full word frequency table, extra statistics, history page.
