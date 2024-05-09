MLOps_URFU

Это учебное задание по дисциплине MLOps 2 модуль
для выполнения этого задания использован набор данных из библиотеки catboost.datasets.titanic с информацией о пассажирах «Титаника» (известная учебная задача с kaggle.com “Titanic Disaster”).. 
Выполнена задача регрессии по предсказанию выживания пассажиров Титаника.
В отличие от рассмотренной задачи на уроке рассмотрим все признаки, 
их влияние на целевую функцию и 
рассмотрим результаты применения 3-х моделей: регрессия, случайный лес, бустинг от CatBoost 


Этапы выполнения задания.
1. Развернут сервер с Jenkins (локально), установлено необходимое программное обеспечение для работы над созданием модели машинного обучения.
2. Создание python-скрипта (create_dataset.py), которыйзагружает и предобрабатывает набор данных. Использованы модули pathlib, numpy
3. Создание python-скрипта (train_model.py), который создает и обучает модель машинного обучения на данных train. Рассмотрены 3 модели: регрессия, случайный лес, бустинг от CatBoost. По результатам оценки качества (кросс-тестирование) выбрана модель RandomForestClassifier (scikit-learn). Метрика R2 = 0.20
4. Создание python-скрипта (make_prediction.py), проверяющий модель машинного обучения на построенных данных из папки «test» и печать результатов. 
5. Создание скрипта (Jenkinsfile.txt), устанавливающий окружение и последовательно запускающий все python-скрипты.