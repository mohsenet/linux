## gunicorn service

```ini
[Unit]
Description=Gunicorn daemon
After=network.target
[Service]
User=USER
Group=www-data
WorkingDirectory=/home/USER/YOUR_PROJECT
ExecStart=/home/USER/venv/bin/gunicorn --access-logfile - --workers 3 --bind unix:/home/USER/YOUR_PROJECT/NAME.sock YOUR_PROJECT.wsgi:application --timeout 120
[Install]
WantedBy=multi-user.target
```
