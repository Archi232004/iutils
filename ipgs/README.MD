# iPgs

```
iutils/
├── ipgs/
│   ├── ipgs/
│   │   ├── __init__.py
│   │   └── core.py
│   ├── setup.py
│   ├── README.md
│   ├── LICENSE
│   └── ...
└── README.md
```

# iPgs – Interactive Animated Progress Bar for Jupyter


**iPgs** provides an interactive and animated progress bar designed for Jupyter Notebook and Google Colab environments. It enables clear visualization of training or processing progress, including nested loops such as epochs and batches, with automatic computation of estimated completion time (ETA).

---

## Features

- **Nested progress tracking**: Supports simultaneous display of epoch-level and batch-level progress.  
- **Animated visualization**: Dynamic, real-time updates suitable for Jupyter and Colab notebooks.  
- **Ease of integration**: Fully compatible with PyTorch, TensorFlow, or standard Python loops.  
- **Automatic ETA calculation**: Estimates remaining processing time without manual intervention.  
- **Dependency-free**: No external dependencies required
- **Flexible usage**: Works with both DataLoader-style iterables and standard Python iterables.  

---




** مشاهده پیشرفت حلقه‌ها در Jupyter و Colab به شکل حرفه‌ای و انیمیشنی!**

iPgs یک **progress bar گرافیکی و انیمیشنی** است که مخصوص محیط‌های Jupyter Notebook و Google Colab طراحی شده و برای **PyTorch، TensorFlow و حلقه‌های استاندارد Python** کاملاً مناسب است. دیگر نیازی به محاسبه دستی درصد و زمان باقی‌مانده (ETA) ندارید!

---

## ویژگی‌های برجسته

- **پیشرفت nested:** نمایش پیشرفت **Epoch و Batch** همزمان  
- **انیمیشن و زیبایی:** نوار پیشرفت جذاب و حرفه‌ای با تغییر رنگ و متن پویا  
- **ساده و آماده استفاده:** فقط حلقه خود را با `iPgs(loader, num_epochs=5)` بپیچید  
- **سازگار با DataLoaderها و حلقه‌های معمولی** حتی بدون PyTorch  
- **محاسبه خودکار ETA:** زمان تقریبی پایان عملیات به صورت خودکار نمایش داده می‌شود  
- **کمترین وابستگی:** فقط نیاز به `ipywidgets`  

---

## Installation | نصب


```bash
pip install ipgs


You can install directly from GitHub:

```bash
pip install git+https://github.com/Mohampouraz/ipgs.git
```
