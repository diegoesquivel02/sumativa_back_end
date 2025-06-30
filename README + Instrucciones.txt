# 🧺 Ferias Locales — Sistema de Gestión

## 📝 Descripción breve

Este sistema permite la administración de **puestos**, **vendedores** y **productos** en ferias locales mediante un backend en **Django REST Framework** y un frontend en **React** con estilización usando **Bootstrap 5**.

---

## 🧩 Diagrama de modelos y relaciones


+----------+        1 ──── N       +-------------+        1 ──── N      +-------------+
|  Puesto  |───────────────── |  Vendedor   |─────────────────|  Producto   |
+----------+                        +-------------+                        +-------------+
| id       |                        | id          |                        | id          |
| nombre   |                        | nombre      |                        | nombre      |
| ubicación|                        | puesto_id   |                        | precio      |
| detalle  |                        +-------------+                        | vendedor_id |
| ...      |                                                               | disponible  |
+----------+                                                               +-------------+
👉 Cada Puesto tiene varios Vendedores, y cada Vendedor puede vender varios Productos.

---

⚙️ Instrucciones de ejecución

🚀 Backend (Django)
accede al directorio del backend:
cd ferias-locales/ferias_locales

Activa el entorno virtual con pipenv:
pipenv Shell

Aplica migraciones (solo la primera vez o tras cambios en modelos):

python manage.py makemigrations
python manage.py migrate

Inicia el servidor:
python manage.py runserver

🟢 El backend estará disponible en: http://127.0.0.1:8000

---
🖥️ Frontend (React)
En otra terminal, entra a la carpeta ferias-frontend:
cd ferias-frontend

Instala las dependencias de React:
npm install

Arranca el servidor de desarrollo:
npm start

🟢 El frontend estará disponible en: http://localhost:3000



