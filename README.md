# CDN

Репозиторий содержит эксперименты по задаче long-tail item recommendation. Основная цель: сравнить базовую Two-Tower модель с методами, улучшающими качество рекомендаций для tail-items, включая CDN и AdaCDN.

`AdaCDN` - модификация CDN, в которой вклад регуляризующей ветви подбирается более адаптивно. Гипотеза: такая модификация может сбалансировать качество на head-items и tail-items без заметной потери overall-метрик.

Эксперименты проводятся на датасетах BookCrossing, MovieLens и Yambda. Для каждой модели обучение, подбор гиперпараметров и подсчёт метрик выполняются в `.ipynb`-ноутбуках. Итоговые значения метрик сохраняются в `summary.csv`.

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

Код распространяется в учебных целях. Датасеты, использованные в проекте, не покрываются лицензией данного репозитория. Права на датасеты принадлежат их оригинальным правообладателям.

## Ссылки

- Yambda paper: [Yambda-5B - A Large-Scale Multi-modal Dataset for Ranking And Retrieval](https://arxiv.org/abs/2505.22238)
- Yambda: https://huggingface.co/datasets/yandex/yambda
- MovieLens: https://grouplens.org/datasets/movielens/1m/
- BookCrossing: http://www2.informatik.uni-freiburg.de/~cziegler/BX/
