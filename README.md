# phpmosquitto

#
sudo tee /etc/yum.repos.d/mosquitto.repo <<EOF
[mqtt-mosquitto]
name=mqtt-mosquitto
baseurl=https://repo.mosquitto.org/centos/7/$basearch/
gpgcheck=1
enabled=1
gpgkey=https://repo.mosquitto.org/RPM-GPG-KEY-mosquitto
EOF
