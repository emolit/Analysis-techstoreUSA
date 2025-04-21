# 📊 Tech Store Sales Analysis | Retail Analytics Project

![Python](https://img.shields.io/badge/Python-3.9+-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-1.3+-orange?logo=pandas)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-red?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green)

## 🔍 Оглавление
- [Описание проекта](#-описание-проекта)
- [Ключевые метрики](#-ключевые-метрики)
- [Технологический стек](#-технологический-стек)
- [Быстрый старт](#-быстрый-старт)
- [Структура проекта](#-структура-проекта)
- [Примеры анализа](#-примеры-анализа)
- [Частые вопросы](#-частые-вопросы)
- [Развитие проекта](#-развитие-проекта)
- [Лицензия](#-лицензия)

## 📝 Описание проекта
Полный анализ продаж технологического магазина в США за 2020-2023 годы. Проект включает:
- Очистку и преобразование данных
- Расчет ключевых показателей эффективности (KPI)
- Визуализацию трендов
- Выявление паттернов покупательского поведения

## 📊 Ключевые метрики
| Показатель | Значение | Изменение (YoY) |
|------------|----------|----------------|
| Общая выручка | $4.2M | +17% |
| Средний чек | $289 | +5% |
| Топ-1 товар | MacBook Pro M2 | - |
| Конверсия | 3.2% | +0.4п.п. |

## 🛠 Технологический стек
- **Язык**: Python 3.9+
- **Библиотеки**:
  ```python
  import pandas as pd       
  import matplotlib.pyplot as plt  
  import seaborn as sns     

## 🚀 Быстрый старт

### Требования
- Python 3.9+
- Jupyter Notebook
- Git

### Установка
```bash
# 1. Клонировать репозиторий
git clone https://github.com/emolit/Analysis-techstoreUSA.git
cd Analysis-techstoreUSA

# 2. Создать виртуальное окружение
python -m venv venv

# 3. Активировать окружение
# Для Windows:
.\venv\Scripts\activate
# Для Linux/Mac:
source venv/bin/activate

# 4. Установить зависимости
pip install -r requirements.txt
```

### Запуск
```bash
jupyter notebook
```

## 📂 Структура проекта
```
Analysis-techstoreUSA/
├── data/                   # Данные
│   ├── raw/                # Исходные данные
│   └── processed/          # Обработанные данные
├── notebooks/              # Блокноты анализа
│   └── Tech_Store_Sales_Analysis.ipynb
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## 📈 Пример анализа
```python
# Загрузка данных
df = pd.read_csv('data/processed/sales.csv')

# Топ-5 товаров
top_products = df.groupby('product')['revenue'].sum().nlargest(5)

# Визуализация
plt.figure(figsize=(10,6))
df.groupby('month')['sales'].sum().plot(kind='bar')
plt.title('Продажи по месяцам')
plt.show()
```

## 🔮 Развитие проекта
Планируемые улучшения:

- [ ] Добавить прогнозирование продаж
- [ ] Интегрировать Dashboard (Streamlit)
- [ ] Автоматизировать отчетность


## 📜 Лицензия
Этот проект распространяется под лицензией [MIT](LICENSE).