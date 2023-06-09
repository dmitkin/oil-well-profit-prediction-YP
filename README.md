## Описание проекта

Нужно решить, где бурить новую скважину.
Шаги для выбора локации обычно такие:
- В избранном регионе собирают характеристики для скважин: качество нефти и объём её запасов;
- Строят модель для предсказания объёма запасов в новых скважинах;
- Выбирают скважины с самыми высокими оценками значений;
- Определяют регион с максимальной суммарной прибылью отобранных скважин.
Мне предоставлены пробы нефти в трёх регионах. Характеристики для каждой скважины в регионе уже известны. Необходимо построить модель для определения региона, где добыча принесёт наибольшую прибыль.  


## Описание данных

- _id_ — уникальный идентификатор скважины;
- _f0_, _f1_, _f2_ — три признака точек (неважно что они означают, но сами признаки значимы);
- _product_ — объём запасов в скважине (тыс. баррелей).  


## Условия задачи
- Для обучения модели подходит только линейная регрессия (остальные — недостаточно предсказуемые).
- При разведке региона исследуют 500 точек, из которых с помощью машинного обучения выбирают 200 лучших для разработки.
- Бюджет на разработку скважин в регионе — 10 млрд рублей.
- При нынешних ценах один баррель сырья приносит 450 рублей дохода. Доход с каждой единицы продукта составляет 450 тыс. рублей, поскольку объём указан в тысячах баррелей.
- После оценки рисков нужно оставить лишь те регионы, в которых вероятность убытков меньше 2.5%. Среди них выбирают регион с наибольшей средней прибылью.

## Вывод

В ходе исследования были проведены рассчеты объема добычи, необходимого для безубыточной разработки скважины. На предоставленных данных были построены модели машинного обучения. Исходя из полученных данных и моделей, мы воспользовались техникой Bootstrap для рассчетов прибыли и рисков каждого региона.
