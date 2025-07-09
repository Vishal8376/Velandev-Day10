# Velandev-Day10

---

### 📦 E-Commerce Product App (Django)

A simple Django project for managing products in an e-commerce portal. This app allows admin users to add, update, and manage product listings with details like name, price, description, availability, and image uploads.

---

### ✨ Features

* Add/edit/delete products via Django Admin
* Product model includes:

  * Name
  * Price (validated to be positive)
  * Description
  * Availability status
  * Product image (stored in `media/products/`)
* Media file handling (image upload)
* Admin panel customization with filters and search

---

### 🚀 Setup Instructions

1. **Clone the project:**

   ```bash
   git clone https://github.com/your-username/ecommerce-product-app.git
   cd ecommerce-product-app
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Install Pillow (for image handling):**

   ```bash
   pip install Pillow
   ```

4. **Apply migrations:**

   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create superuser (for admin access):**

   ```bash
   python manage.py createsuperuser
   ```

6. **Run the server:**

   ```bash
   python manage.py runserver
   ```

7. **Access the admin panel:**
   [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

---

### 📁 Media File Configuration

In `settings.py`:

```python
MEDIA_URL = '/media/'
MEDIA_ROOT = BASE_DIR / 'media'
```

In `urls.py`:

```python
from django.conf import settings
from django.conf.urls.static import static

if settings.DEBUG:
    urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
```

---

### 🛠 Tech Stack

* Python 3
* Django
* SQLite (default DB)
* HTML/CSS (for basic admin UI)
* Pillow (for image uploads)

---
