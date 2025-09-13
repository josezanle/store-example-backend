# 🛠️ Django Store API

    Este proyecto es una API REST construida con Django + Django REST Framework, dockerizada 
    y lista para levantar en entorno local con PostgreSQL.

---

## ⚙️ Configuración del entorno

    Antes de iniciar el proyecto, asegurate de tener un archivo `.env` 
    en la raíz del proyecto. Ya se incluye un `.env.example` con valores 
    funcionales para desarrollo, podes borra .example y ya funciona.

### 📦 Variables incluidas

```env
# Django core
    SECRET_KEY=django-insecure-*clave-de-ejemplo*
    DEBUG=True
    ALLOWED_HOSTS=localhost,127.0.0.1

# PostgreSQL
    DB_ENGINE=django.db.backends.postgresql
    DB_NAME=store_db
    DB_USER=store_user
    DB_PASSWORD=store_pass
    DB_HOST=db
    DB_PORT=5432


### POST http://localhost:8000/login
    {
    "username": "tu_user",
    "password": "tu_password"
    }

### respuesta: {
    "token": "a7e13fb..."
}

### uso del token: 
    Authorization: Token <token>

### GET 
    http://localhost:8000/api/products/


### Comandos: 
    docker compose up --build
    docker compose exec web python manage.py makemigrations
    docker compose exec web python manage.py migrate
    docker compose exec web python manage.py createsuperuser


