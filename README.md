# Lab7_Testing

Лабораторная работа №7. Пошаговое освоение pytest в VS Code.

Автор: Уютов Павел Александрович, группа ИСП-231.

## Описание

Проект содержит класс `Calculator` (сложение, вычитание, умножение, деление, история операций) и тесты на pytest: базовые, с фикстурами, параметризованные и на исключения.

## Структура проекта

```
pytest_project/
├── calculator.py          # класс Calculator
├── test_calculator.py     # базовые тесты, фикстуры, исключения (7 тестов)
├── test_parametrize.py    # параметризованные тесты (14 тестов)
└── README.md
```

## Установка

```bash
python -m pip install pytest pytest-cov
```

Проверка версий:

```bash
python --version
pytest --version
pip show pytest-cov
```

## Запуск тестов

Все тесты с подробным выводом:

```bash
pytest -v
```

Только один файл:

```bash
pytest test_parametrize.py -v
```

Если команда `pytest` не находится:

```bash
python -m pytest -v
```

## Измерение покрытия

В терминале:

```bash
pytest --cov=calculator
```

HTML-отчёт (появится папка `htmlcov/`, откройте `htmlcov/index.html` в браузере):

```bash
pytest --cov=calculator --cov-report=html
```

Финальный запуск:

```bash
pytest -v --cov=calculator
```

## Результат

- Всего тестов: 21 (все PASSED)
- Покрытие `calculator.py`: 100%