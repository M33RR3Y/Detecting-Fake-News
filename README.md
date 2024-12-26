# Обнаружение фальшивых новостей

Модель для детекции фальшивых новостей предназначена для автоматического определения достоверности новостей, публикуемых в интернете и социальных сетях. Её основная цель — помочь пользователям и организациям выявлять ложные (FAKE) новости и отличать их от реальных (REAL) с высокой точностью, превышающей 90%. Это важно для борьбы с дезинформацией, манипуляцией общественным мнением и поддержания прозрачности в медиапространстве. Для обучения используется данный [датасет](https://storage.yandexcloud.net/academy.ai/practica/fake_news.csv)


Как работает модель:

* Извлечение признаков: Для обработки текстов используется метод TfidfVectorizer, который преобразует текстовые данные в числовое представление, основанное на частоте терминов и обратной частоте документа (TF-IDF). Этот подход позволяет учитывать не только популярные слова, но и их уникальность в контексте новостей.

* Классификация: Модель основана на алгоритме PassiveAggressiveClassifier, который является линейным классификатором и подходит для обработки текстов. Этот алгоритм эффективен для задач, где требуется быстро обновлять модель при добавлении новых данных.

* Обучение: Модель обучается на предоставленном наборе данных, включающем метки REAL и FAKE для новостей.

* Визуализация результатов: Для анализа работы модели и представления результатов используется матрица ошибок (confusion matrix) и другие графики. Эти визуализации помогают лучше понять, насколько хорошо модель различает реальные и фальшивые новости.

Почему это важно:

Фальшивые новости могут оказывать значительное влияние на общественное мнение, политические процессы и социальные взаимодействия. Созданная модель может быть использована:

* СМИ для проверки достоверности источников.
* Платформами социальных сетей для пометки потенциально ложных материалов.
* Исследователями и аналитиками для анализа распространения дезинформации.

Основные характеристики проекта:

* Точность более 90% в классификации новостей.
* Использование проверенных методов машинного обучения: TfidfVectorizer для извлечения признаков и PassiveAggressiveClassifier для классификации.
* Полная визуализация результатов для удобного анализа и демонстрации.
