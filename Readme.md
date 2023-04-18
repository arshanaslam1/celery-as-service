###################### please follow these steps to configure Celery as service ######################

#1. install Celery on the your application and update the VENV path location
#2. paste celery.service at /etc/systemd/system/ and update the file
#2. paste celery.conf at /etc/opt/  
#6. once done, run below commands.

sudo mkdir -pv /var/{log,run}/celery/
sudo chown -cR USERNAME:USERNAME /var/{log,run}/celery/
sudo systemctl enable celery.service
sudo systemctl start celery.service
sudo systemctl daemon-reload
sudo systemctl status celery.service