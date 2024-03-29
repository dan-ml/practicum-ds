## Прогнозирование оттока клиентов банка

### Описание проекта
Из банка стали уходить клиенты. Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Для анализа предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.

В проекте необходимо построить модель с предельно большим значением F1-меры (не менее 0,59). Дополнительно следует измерить метрику AUC-ROC и сравнить её значение с F1-мерой.

### Результат работы по проекту
1. Выполнена предобработка данных (заполнены пропуски, исследованы возможные аномалии), подготовлены признаки для обучения моделей (применено прямое кодирование категориальных признаков, выполнено разделение на обучающую и тестовую выборки, проведено масштабирование обучающих признаков). Построена константная модель.
2. Построена модель логистической регрессии без учёта дисбаланса классов. Получено неудовлетворительное значение метрики F1.
3. Построены три модели с учётом дисбаланса классов: линейная регрессия, "Дерево решений" и "Случайный лес". Наилучшие результаты по качеству предсказания показала модель "Случайный лес". При проверке её работы на тестовой выборке удалось получить значение метрики F1, равное 0,63. При этом значения других метрик качества (0,84 для accuracy и более 0,86 для AUC-ROC) так же оказались высокими. Затем для модели "Случайный лес" были построены ROC- и PR-кривые. Поставленная в проекте задача выполнена.

### Используемые библиотеки
*Pandas, NumPy, Matplotlib, Scikit-learn*