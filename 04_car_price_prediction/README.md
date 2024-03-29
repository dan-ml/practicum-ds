## Определение стоимости подержанных автомобилей

### Описание проекта
Сервис по продаже автомобилей с пробегом разрабатывает приложение для привлечения новых клиентов. В нём можно быстро узнать рыночную стоимость своего автомобиля. 

В проекте требуется построить модель для определения стоимости подержанных автомобилей на основе исторических данных: технических характеристик, комплектации и цены. Заказчику важны:
- качество предсказания;
- скорость предсказания;
- время обучения.

Чтобы усилить исследование, нужно поэкспериментировать с моделью градиентного бустинга и другими более простыми моделями. Затем сравнить значения их метрик качества. Значение метрики RMSE у выбранной модели должно быть меньше 2500.

### Результат работы по проекту
1. Выполнена предобработка данных: удалены дубликаты, заполнены пропуски, исследованы и исправлены аномалии.
2. Произведена подготовка признаков для обучения моделей: применено прямое и порядковое кодирование категориальных признаков; данные разделены на тренировочную и тестовую выборки. Для линейной регрессии выполнено масштабирование обучающих признаков.
3. Произведено построение шести моделей, одна из которых константная. Из реальных моделей были построены: модель линейной регрессии, модель "Дерево решений", модель "Случайный лес" и две модели градиентного бустинга LightGBM и CatBoost. Наилучшие результаты по совокупности метрик качества показала модель LightGBM. При проверки её работы на тестовой выборке получено значение метрики RMSE, равное 1506. Поставленная в проекте задача выполнена.

### Используемые библиотеки
*Pandas, NumPy, Scikit-learn, Matplotlib, LightGBM, CatBoost*