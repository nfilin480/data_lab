## Сентиментный анализ новостей lenta.ru (3 labels: negative, neutral, positive)
### Собранные данные для анализа: с 01.2020 по 12.2023
Метрика качества: f1-macro
В качестве данных для дообучения моделей Bert-семейства использовались различные датасеты в открытом доступе на русском языке (по 5к данных каждого класса).

- sentiment_analysis.py (finetune_bert_sentiment.py)- скрипт для дообучения моделей bert.
- syntax_analyzer.py - скрипт для предобработки текста.
- nohup.out - вывод лучшей модели
- lenta-ru-parser.py - парсер данных с сайта lenta.ru
- get_sentiment.py - запуск дообученной модели для разметки данных lenta.ru
- sentiment_graph.ipynb - полученное распределение классов после анализа.

Лучшие результаты:
модель - xlm-roberta-base
f1-macro - 0.74

Протестированные модели: bert-base-multilingual-uncased(cased), distilbert-base-multilingual-cased, bert-large-uncased
