# LSTM-sentiment-analysis
### В ходе работы по выделению эмоции (позитивная/негативная эмоциональная окраска) было сделано:
* С помощью своего парсера были собраны новости с https://www.d-kvadrat.ru с последующей обработкой текста для создания корпуса текстов
* Используя API от OpenAI ранее собранный датасет был размечен - задача LLM была в разметка каждого текста на позитивный и негативный по эмоциональной окраске
* Токенизация текста через YouTokenToMe
* При помощи библиотеки PyTorch была реализована DL модель - nn.Embedding + nn.LSTM + nn.Linear
* Модель была обучена на размеченном датасете, посчитаны метрики на валидации и тестах.
* Точность на тестовой части варьируется от 69% до 80% (при условии изначально небольшого датасета)
