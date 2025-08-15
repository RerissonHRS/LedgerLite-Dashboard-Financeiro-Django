# django-portfolio-dashboard (Branded)

Projeto Django para portfólio com UI voltada a recrutadores: autenticação, CRUD de vendas, dashboard (Chart.js), exportação CSV/Excel e visual moderno (Bootstrap 5). Inclui página **Sobre o Projeto** com destaques do que você domina.

## Rodando localmente

```bash
cd backend
python -m venv .venv
# Windows:
.venv\Scripts\activate
# Linux/Mac:
source .venv/bin/activate

pip install -r requirements.txt
python manage.py migrate
python manage.py loaddata dashboard/fixtures.json   # opcional (dados de exemplo)
python manage.py createsuperuser
python manage.py runserver
```

Acesse: http://127.0.0.1:8000

## Páginas
- `/` Dashboard com KPIs e gráfico
- `/sobre/` Sobre o Projeto (habilidades demonstradas + contatos)
- `/sales/` CRUD de vendas (protegido por login)

## Deploy rápido (Render/Heroku)
- Adicione `gunicorn` ao `requirements.txt` (já incluído)
- Crie `Procfile` com `web: gunicorn core.wsgi` (já incluído na raiz)
- Configure env `SECRET_KEY` e `ALLOWED_HOSTS`
