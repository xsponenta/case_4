# case_4

![Untitled diagram _ Mermaid Chart-2025-08-10-113257](https://github.com/user-attachments/assets/a2026a6a-665d-4bf8-917d-cc7c97ae746a)

## Опис

У цьому репозиторії представлено симуляцію системи розподілу трафіку (TDS) для affiliate marketing з моніторингом KPI, CR, EPC та системою алертингу.

### Основні можливості

- Завантаження та підготовка даних з CSV (postbacks, clicks, sources, offers)
- Розрахунок EPC (Earnings Per Click) та CR (Conversion Rate)
- Фільтрація оферів з урахуванням лімітів та сегментів
- Вибір офера за допомогою ε-жадібної стратегії (epsilon-greedy, RandomForest)
- Моніторинг та візуалізація KPI
- Виявлення аномалій та алертинг (низький EPC/CR, стрибки трафіку, підозрілі IP)
- Гнучка симуляція: один клік або масив кліків

### Файли

- `solutions.ipynb` — основна симуляція алгоритму, моніторинг, алертинг
- `selection_history.csv` — лог призначення оферів
- `kpi_monitoring.csv` — щоденні KPI
- `alerts_log.csv` — журнал аномалій

### Як запустити

1. Встановіть залежності:
    ```bash
    pip install pandas numpy scikit-learn matplotlib
    ```
2. Переконайтесь, що CSV-файли знаходяться у відповідних шляхах (див. початок `solutions.ipynb`).
3. Запустіть ноутбук `solutions.ipynb` у Jupyter або VS Code.

### Приклад запуску симуляції

Використайте функцію:
```python
run_simulation(sample_size=100, epsilon=0.1)
```
- `sample_size` — кількість кліків для симуляції
- `epsilon` — параметр дослідження (0.1 = 10% випадкових виборів)

### Візуалізація

- KPI-графіки автоматично будуть побудовані після симуляції.
- Додаткові графіки: `simulation.png`, `click_selection.png`.

### Алертинг

- Аномалії логуються у `alerts_log.csv` та виводяться у консоль з рекомендаціями.

---

## Діаграми

![alt text](<simulation.png>)
![alt text](<click_selection.png>)

---

## Автор

Ігор Іванишин, 2025

---
