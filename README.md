# 🧠 Output Manipulation — NLP Study Project

Этот проект реализует систему управления выводом LLM, которая позволяет фильтровать, стилистически обрабатывать и контролировать текст, генерируемый моделью. Он особенно полезен при использовании LLM в пользовательских интерфейсах, чат-ботах и других чувствительных к тону приложениях.

---

## 🎯 Цель проекта

Создать модуль для модерации и стилистической обработки текстов, генерируемых моделью, используя:
- Логит-фильтрацию (`LogitsProcessor`) для запрещения и разрешения определённых слов;
- Фильтрацию входа и выхода (input/output filtering);
- Постобработку текста для улучшения читабельности;
- Безопасные ответы в случае запретных тем.

---

## 🧠 Используемая модель

Модель: [`TinyLlama/TinyLlama-1.1B-Chat-v1.0`](https://huggingface.co/TinyLlama/TinyLlama-1.1B-Chat-v1.0)  
⚠️ Используется в offline-режиме (модель должна быть скачана заранее и размещена локально).

---

## 🛠 Установка и запуск

1. Установите зависимости:

```bash
pip install -r requirements.txt
Скачайте модель TinyLlama вручную с Hugging Face и разместите её локально.
Запустите ноутбук или Python-скрипт:
# Jupyter Notebook
jupyter notebook output_manipulation.ipynb
# Или как скрипт
python output_manipulation.py
```

## 🧩 Структура проекта
- `output_manipulation.ipynb` — основной Jupyter-ноутбук
- `output_manipulation.py` — скриптовая версия с логикой генерации
- `requirements.txt` — зависимости
- `README.md` — описание проекта

## 💬 Пример вызова
```python
from output_manipulation import generate_response

prompt = "Ты бесполезный робот."
print(generate_response(prompt))
```

## 📈 Возможные улучшения
Использовать `pymorphy2` или `natasha` для морфологического анализа и фильтрации в русском языке
Добавить возможность настройки списков слов через `YAML/JSON`
Расширить фильтрацию на уровне синтаксиса или смысла
Встроить нейтральную переформулировку токсичных ответов
## 📚 Авторство
Разработано в рамках учебного проекта по NLP

Контакты: ``chipalgash@icloud.com``

GitHub: chipalgash
