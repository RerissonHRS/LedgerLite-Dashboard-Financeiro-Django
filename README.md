# LedgerLite-Dashboard-Financeiro-Django
O projeto será pensado para:  Impressionar recrutadores (layout moderno, responsivo e clean)  Demonstrar habilidades técnicas (Django, integração com banco, APIs e front-end)  Ter dados reais ou simulados que mostrem seus conhecimentos em análise de dados e automação  Facilidade para rodar localmente com instruções simples

# Como rodar - LedgerLite-Dashboard-Financeiro-Django

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
