# api-server-example

嘗試以 python 實作小型 backend-api-server

# Setup

### 建議使用 virtualenv 來當作 python 的開發環境

```
virtualenv -p python3 .py3
source .py3/bin/activate
```

then

```
pip install -r requirements.txt
```

# Production

```
gunicorn -c gunicorn.conf.py -w 4 -b 0.0.0.0:8000 -k gevent app:app --reload
```

# Development

```
export FLASK_APP=my_application
export FLASK_ENV=development
flask run
```
