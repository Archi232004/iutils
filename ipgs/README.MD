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

This package is **framework-agnostic** and **dependency-free**, making it lightweight and easy to integrate into any Python workflow.

---

## Key Highlights

- **Interactive and Animated**: Real-time visual feedback enhances comprehension of long-running tasks, making iterative processes like model training more intuitive.  
- **Nested Progress Tracking**: Simultaneously displays epoch-level (outer) and batch-level (inner) progress, providing a granular view of the workflow.  
- **Automatic ETA Calculation**: Continuously estimates remaining time for both epochs and batches, improving planning and monitoring.  
- **Framework-Agnostic**: Fully compatible with PyTorch, TensorFlow, Keras, NumPy arrays, Python lists, or any iterable—no modifications required.  
- **Dependency-Free**: Relies only on built-in Python libraries and IPython display functionality, ensuring easy installation and minimal overhead.  
- **Flexible Usage**: Works seamlessly with both DataLoader-style iterables and standard Python loops, supporting diverse workflows.  

---



# iPgs – نوار پیشرفت تعاملی و انیمیشنی برای Jupyter

**iPgs** یک نوار پیشرفت تعاملی و انیمیشنی است که برای محیط‌های **Jupyter Notebook** و **Google Colab** طراحی شده است. این ابزار امکان نمایش واضح پیشرفت فرآیندهای آموزشی یا پردازشی را فراهم می‌کند، از جمله حلقه‌های تو در تو مانند **epochs** و **batches**، و زمان تقریبی باقی‌مانده (ETA) را به صورت خودکار محاسبه می‌کند.

این بسته **مستقل از فریم‌ورک** و **بدون وابستگی اضافی** است، بنابراین سبک و به راحتی قابل ادغام در هر جریان کاری Python می‌باشد.

---

## نکات برجسته

- **تعامل و انیمیشن**: بازخورد بصری در زمان واقعی، درک فرآیندهای طولانی و تکراری مانند آموزش مدل را بهبود می‌بخشد و تجربه کاربری را تعاملی‌تر می‌کند.  
- **پیگیری پیشرفت تو در تو**: نمایش همزمان پیشرفت سطح epoch (خارجی) و batch (داخلی) امکان مشاهده جزئیات دقیق فرآیند را فراهم می‌کند.  
- **محاسبه خودکار ETA**: زمان باقی‌مانده برای هر دو سطح epoch و batch به‌صورت مداوم تخمین زده می‌شود و برنامه‌ریزی و مانیتورینگ را آسان‌تر می‌کند.  
- **مستقل از فریم‌ورک**: کاملاً با PyTorch، TensorFlow، Keras، آرایه‌های NumPy، لیست‌های Python یا هر iterable دیگری سازگار است و نیاز به تغییرات ندارد.  
- **بدون وابستگی اضافی**: تنها به کتابخانه‌های داخلی Python و قابلیت‌های نمایش IPython متکی است، بنابراین نصب آسان و کم‌حجم است.  
- **استفاده انعطاف‌پذیر**: با هر دو نوع iterable مانند DataLoader و حلقه‌های استاندارد Python به‌خوبی کار می‌کند و از جریان‌های کاری متنوع پشتیبانی می‌کند.  

---


## Installation | نصب

```bash
pip install ipgs
```

## Usage Example | نحوه استفاده
```
from ipgs import iPgs

for epoch_idx, batch_idx, batch in iPgs(loader, num_epochs=5, desc="Training"):
    bx, by = batch
    # training step
```

## You can install directly from GitHub:

```bash
pip install git+https://github.com/Mohampouraz/ipgs.git
```
