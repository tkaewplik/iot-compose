# IoT compose

## Quick started
```sh
$ docker stack deploy -c iot-stack.yml iot-stack
```


# Mosquitto 
## [Setting up Authentication in Mosquitto MQTT Broker](https://medium.com/@eranda/setting-up-authentication-on-mosquitto-mqtt-broker-de5df2e29afc)

Create `password.txt` file
```txt
user1:pass1
user2:pass2
```
Encryp password
```sh
$ mosquitto_passwd -U ./password.txt
```

Edit configuration file `/etc/mosquitto/mosquitto.conf`
```conf
password_file /etc/mosquitto/passwd
allow_anonymous false
```