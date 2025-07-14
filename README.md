
# Django + React App

A full-stack web application with a Django REST API backend and a React (JS) frontend.

## 🏗 Project Structure

```
Django-react-App-main/
├── backend/          # Django project (API, models, auth)
│   ├── manage.py
│   ├── <django_project>/
│   ├── requirements.txt
│   └── ...
├── frontend/         # React app (JS/TS, components)
│   ├── package.json
│   ├── src/
│   └── ...
└── .gitignore
```

---

## ⚙️ Backend (Django)

### 1. Install dependencies
```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### 2. Apply migrations
```bash
python manage.py migrate
```

### 3. Create superuser (optional, for admin)
```bash
python manage.py createsuperuser
```

### 4. Run the Django server
```bash
python manage.py runserver
```
- Default: [http://localhost:8000](http://localhost:8000)

---

## ⚛️ Frontend (React)

### 1. Install dependencies
```bash
cd frontend
npm install
# or
yarn
```

### 2. Start the React development server
```bash
npm start
# or
yarn start
```
- Default: [http://localhost:3000](http://localhost:3000)

---

## 🔗 Connecting Frontend & Backend

- The React app fetches data from the Django API (set `REACT_APP_API_URL` or proxy in `package.json`).
- Make sure Django allows CORS (add `django-cors-headers` and configure in `settings.py`).

---

## 🚀 Production Deployment

- Use [Gunicorn](https://gunicorn.org/) or [uWSGI](https://uwsgi-docs.readthedocs.io/en/latest/) for Django.
- Build the React app for production:
  ```bash
  npm run build
  ```
- Serve static files via Django (`collectstatic`) or with a separate web server (Nginx/Apache).

---

## 🧪 Testing

- **Backend:**  
  ```bash
  python manage.py test
  ```
- **Frontend:**  
  ```bash
  npm test
  # or
  yarn test
  ```

---

## 📄 Author

Yves Mboumi  
[LinkedIn](https://linkedin.com/in/yvesmboumi)  
Email: yves.mboumi@gmail.com

---

> Contributions welcome! Fork, PR, and suggestions encouraged.
