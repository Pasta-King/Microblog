# Caio's Microblog
## Intall
To run this program you will need these prerequisites
- python3
- python -m venv env 
- env\scripts\activate
- pip install -r requirements.txt
- set FLASK_APP=microblog.py
- flask run

- Azure deployment:
    -  az webapp up --location uksouth --sku F1 --name microblog-caio --resource-group microblog-caio-rg --dryrun
    - az webapp config set --resource-group microblog-caio-rg --name microblog-caio --startup-file "gunicorn --bind=0.0.0.0 --timeout 600 microblog:myApp"
    - http://microblog-caio.azurewebsites.net