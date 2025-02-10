# Роадмап развития в A/B-тестах

## Общие ресурсы

### Курсы и книги
- [Курс по основам A/B-тестирования и матстатистики от Яндекс Практикума](https://practicum.yandex.ru/statistics-basic/)
- *Доверительное A/B-тестирование*, Рон Кохави
- [Курс от ВШЭ (видео)](https://youtube.com/playlist?list=PLEwK9wdS5g0p_ExQfhTrtpP0hYElcGp-r&si=SagA81FP1Tzpj2Ya) | [GitHub](https://github.com/nbagiyan/online-exp-course)

## Зачем это вообще нужно? Культура A/B-тестирования

### Видео
- [A/B-тесты как способ развития продукта — Школа продакт-менеджеров Яндекса](https://www.youtube.com/live/gMx-juYkNCw?si=Hpbpbjeoehp27wT9)
- [Никита Маршалкин: A/B-тесты сложнее, чем кажется | Интервью | karpov.courses](https://youtu.be/gljfGAkgX_o?si=PeyvXxNsM06ZvDnI)
- [The Ultimate Guide to A/B Testing | Ronny Kohavi (Airbnb, Microsoft, Amazon)](https://youtu.be/hEzpiDuYFoE?si=0VhMKJS5on-pMBOv)

### Статьи
- [Про эксперименты в Netflix](https://netflixtechblog.com/netflix-a-culture-of-learning-394bc7d0f94c)
- [Процессы A/B-тестирования](https://habr.com/ru/companies/ods/articles/716110/)
- [Культура A/B-тестирования в Microsoft](https://www.microsoft.com/en-us/research/group/experimentation-platform-exp/articles/it-takes-a-flywheel-to-fly-kickstarting-and-keeping-the-a-b-testing-momentum/)

## Метрики и статистические тесты

### Основные материалы
- [Что такое z-score и p-value?](https://habr.com/ru/articles/653363/)
- [Гид от VK про стат. тесты и их мощность](https://vkteam.medium.com/practitioners-guide-to-statistical-tests-ed2d580ef04f)
- [Бутстрап и его применение](https://habr.com/ru/companies/X5Tech/articles/679842/)
- [Как моделировать для проверки корректности статистических тестов](https://habr.com/ru/companies/X5Tech/articles/706388/)
- [Статистика в A/B: мифы и реальность — Данила Леньков](https://youtu.be/IFAaTKVKH1A?si=PISUlXDNaDu0KvAn)

### Упражнения
1. Написать функцию, которая считает конверсии в воронке и рассчитывает p-value и доверительные интервалы.
2. Проверить применимость t-test к непрерывной метрике:
   - Посмотреть на распределение и определить применимость t-test.
   - Сравнить с Манна-Уитни и бутстрапом, оценить мощность тестов.
   - Добавить выбросы и проанализировать влияние на FPR и мощность.

## Ratio-метрики

### Материалы
- [Гид по анализу ratio-метрик от X5](https://habr.com/ru/companies/X5Tech/articles/740476/)

### Упражнения
- Реализовать метод по формуле и проверить его на моделировании.
- Проверить корректность применения t-test к ratio-метрикам.

## Дизайн и расчет размера выборки

### Материалы
- [Методы оценки размера выборки в A/B-тестах — Анатолий Карпов](https://youtu.be/lJY6eMh10iE?si=S1g_uyLp2lDZORx1)
- [Когда останавливать A/B-тест? Часть 1](https://medium.com/statistics-experiments/когда-останавливать-a-b-тест-часть-1-mde-7d39b668b488)
- [Когда останавливать A/B-тест? Часть 2](https://medium.com/statistics-experiments/когда-останавливать-a-b-тест-часть-2-monte-carlo-a342ba5b552c)
- [Размер выборки для ratio-метрик](https://medium.com/expedia-group-tech/how-to-size-for-online-experiments-with-ratio-metrics-3d57362f1967)
- [Разбор нюансов про дизайн тестов](https://arxiv.org/pdf/2305.16459)

### Упражнения
- Провести моделирование, убедиться, что FPR и мощность соответствуют расчетам.

## Проблемы A/B-тестов

### Подглядывание
- [Статья от Ozon: 6 причин, почему ваши A/B-тесты не работают](https://habr.com/ru/companies/ozontech/articles/712306/)

### Network effects
- [Как Meta тестирует продукты с сетевыми эффектами](https://medium.com/@AnalyticsAtMeta/how-meta-tests-products-with-strong-network-effects-96003a056c2c)
- [Switchback-тестирование](https://medium.com/statistics-experiments/switchback-тестирование-как-бороться-с-социальными-эффектами-в-a-b-тестах-39aab4f87cf7)
- [Применение switchback в такси](https://habr.com/ru/companies/citymobil/articles/560426/)

### Novelty effects
- [Как учитывать эффект новизны](https://www.statsig.com/blog/novelty-effects)

### Sample Ratio Mismatch (SRM)
- [Как проверять SRM](https://koch-kir.medium.com/srm-проверка-сплитование-в-а-в-тестирование-ba02d8640885)

## Методы сокращения дисперсии

### Материалы
- [Методы сокращения дисперсии — Анатолий Карпов](https://youtu.be/KvIJ8FCJzr4?si=gxt4uQFrQQPPVhWb)
- [Стратификация](https://habr.com/ru/companies/X5Tech/articles/596279/)
- [CUPED](https://habr.com/ru/companies/X5Tech/articles/780270/)

### Упражнения
- Проверить эффективность стратификации и CUPED на реальных данных.

## Sequential testing

### Материалы
- [Sequential Testing в Booking](https://booking.ai/sequential-testing-at-booking-com-650954a569c7)
- [Wish: как избежать подглядывания](https://towardsdatascience.com/wish-tackles-peeking-with-always-valid-p-values-8a0782ac9654)

## Квази-эксперименты

### Материалы
- [Causal Inference и A/B без A/B](https://koch-kir.medium.com/causal-inference-from-observational-data-или-как-провести-а-в-тест-без-а-в-теста-afb84f2579f2)

### Упражнения
- Применить Diff-in-Diff и Causal Impact на реальных данных.

## Байесовское A/B-тестирование

### Материалы
- [Гид по Bayesian A/B-тестированию](https://medium.com/@ibtesamahmex/beginners-guide-to-bayesian-ab-testing-22f40988d5e6)
- [Байесовский подход в Glowbyte](https://habr.com/ru/companies/glowbyte/articles/732024/)

### Упражнения
- Использовать [Bayesian-калькулятор](https://abtestguide.com/bayesian/) для анализа конверсий.
