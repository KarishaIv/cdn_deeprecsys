# CDN

Эксперименты запускаются из .ipynb-ноутбуков в папках соответствующих датасетов.

```
cdn_deeprecsys/
├── README.md
├── requirements.txt - зависимости
├── .gitignore
├── Empowering Long-tail Item Recommendation through Cross Decoupling Network (CDN).pdf - основная статья
├── bookcrossing/
│   ├── data/ - датасет BookCrossing
│   │   └── ...
│   └── ...
├── movielens/
│   ├── data/ - датасет MovieLens
│   │   └── ...
│   └── ...
└── yambda/
    ├── data - датасет Yambda
    │   └── ...
    ├── twotowers/
    │   ├── twotowers.ipynb - обучение и подсчёт метрик
    │   ├── summary.csv - итоговые метрики
    │   └── best_params.json - лучшие гиперпараметры
    ├── ada_cdn/
    └── ...
```

## Установка

Для запуска экспериментов рекомендуется использовать **Python 3.11**.

1.
```
python -m venv .venv 
source .venv/bin/activate
pip install -r requirements.txt 
```

2. Открыть нужный ноутбук.
3. Запустить все ячейки сверху вниз.
4. В файле `summary.csv` необходимые метрики.

### License

Код распространяется в учебных целях. Права на датасеты принадлежат их оригинальным правообладателям.
