# Text Autocomplete Language Model

A deep learning NLP project for **next-word prediction and text autocompletion**.  
The project explores recurrent neural networks and a pretrained Transformer model, comparing their ability to predict the continuation of a text sequence.

## Project overview

The task is formulated as language modeling: given a sequence of previous tokens, the model predicts the next token. The notebook contains the complete experimental workflow, including data preparation, model training, evaluation and examples of generated predictions.

The experiments include:

- **LSTM**
- **GRU**
- **DistilGPT2**
- model comparison using **perplexity**
- **Top-1 / Top-5 accuracy**
- qualitative analysis of next-token predictions

## Results

The saved notebook contains the actual outputs of the experiments. In the reported runs:

| Model | Validation perplexity |
|---|---:|
| LSTM | 284.33 |
| GRU | 271.21 |
| DistilGPT2 | 75.37 |

For DistilGPT2, the reported **test perplexity is 72.95**.

The results show a substantial improvement from the recurrent baselines to the pretrained Transformer model on this task.

## Repository structure

```text
text-autocomplete-language-model/
├── notebook.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

`notebook.ipynb` contains the full project workflow and saved outputs.

## Technologies

Python, PyTorch, Hugging Face Transformers, NumPy, Pandas and Jupyter Notebook are used in the project. The exact dependencies imported by the notebook are listed in `requirements.txt`.

## Running the project

1. Clone the repository.
2. Install the dependencies:

```bash
pip install -r requirements.txt
```

3. Open `notebook.ipynb` in Jupyter Notebook or Google Colab.
4. Run the cells in order.

Some cells may require access to the original project dataset or downloading pretrained model weights.

---

# Нейросеть для автодополнения текстов

Проект по NLP, посвящённый **предсказанию следующего слова и автодополнению текста**. В работе исследуются рекуррентные нейронные сети и предобученная Transformer-модель.

## Что реализовано

В ноутбуке представлен полный экспериментальный пайплайн: подготовка данных, обучение моделей, оценка качества и анализ примеров предсказаний.

Рассматриваются:

- **LSTM**
- **GRU**
- **DistilGPT2**
- сравнение моделей по **perplexity**
- метрики **Top-1 / Top-5 accuracy**
- примеры предсказания продолжения текста

## Результаты

В сохранённых результатах ноутбука получены следующие значения validation perplexity:

| Модель | Validation perplexity |
|---|---:|
| LSTM | 284.33 |
| GRU | 271.21 |
| DistilGPT2 | 75.37 |

Для DistilGPT2 в ноутбуке также сохранён результат **test perplexity = 72.95**.

Эксперименты показывают заметное улучшение качества при переходе от рекуррентных моделей к предобученной Transformer-модели.

## Структура репозитория

```text
text-autocomplete-language-model/
├── notebook.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

Основная работа и сохранённые результаты находятся в `notebook.ipynb`.

## Запуск

```bash
pip install -r requirements.txt
```

После установки зависимостей откройте `notebook.ipynb` в Jupyter Notebook или Google Colab и последовательно выполните ячейки.

Для части ячеек может потребоваться исходный датасет проекта или загрузка весов предобученной модели.
