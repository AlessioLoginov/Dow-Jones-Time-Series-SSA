# SSA-анализ временного ряда Dow Jones

## 📌 Описание

В данном проекте мы исследуем временной ряд еженедельных значений индекса **Dow Jones** за период 1971–1974 гг.  
Основная цель — провести разложение ряда методом **SSA (сингулярного спектрального анализа)** и изучить, как влияет длина окна на качество выделения тренда, сезонности и шума.

## 📁 Содержание репозитория

- `Dow-Jones-SSA-Analysis.ipynb` — основной Jupyter-ноутбук с пошаговым SSA-анализом;
- `weekly-closings-of-the-dowjones-.csv` — исходный временной ряд.

## 🚀 Запуск проекта

1. Скачайте датасет `weekly-closings-of-the-dowjones-.csv`;
2. Откройте Jupyter Notebook или Google Colab;
3. Запустите `Dow-Jones-SSA-Analysis.ipynb`.

## 🧠 Что сделано

- Загрузка и визуализация временного ряда;
- Построение матрицы Ганкеля при разных длинах окна;
- Проведение SSA-разложения (SVD);
- Реконструкция 1–2 и 1–4 компонент;
- Сравнение результатов при окнах `L = 10`, `20`, `40`, `81`;
- Построение сингулярных значений и графиков компонент;
- Формирование общей таблицы и выводов по разложению.

## 📊 Результаты (выдержка)

| Окно L | Что видно |
|--------|-----------|
| 10     | Местный тренд, осцилляции невыражены |
| 20     | Тренд + первые признаки сезонности   |
| 40     | Хорошая структура, стабильные волны  |
| 81     | **Оптимальное разложение**: тренд + цикл + шум |

## 🛠 Рекомендации по продолжению

- Анализ остатков (аномалии/шум);
- SSA-форкаст по тренду и циклам;
- Сравнение с другими методами (STL, ARIMA).

## 📎 Зависимости

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`

