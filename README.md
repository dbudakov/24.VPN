## Домашнее задание  
VPN   
Цель: Студент получил навыки работы с VPN, RAS.   
1.Между двумя виртуалками поднять vpn в режимах  
- tun  
- tap  

2.Поднять RAS на базе OpenVPN с клиентскими сертификатами, подключиться с локальной машины на виртуалку   

3.\* Самостоятельно изучить, поднять ocserv и подключиться с хоста к виртуалке   

## Решение  
[tap_tcp]: https://github.com/dbudakov/24.VPN/blob/master/images/homework/v1/iperf_tap_tcp.png
[tap_udp]: https://github.com/dbudakov/24.VPN/blob/master/images/homework/v1/iperf_tap_udp.png
[tun_tcp]: https://github.com/dbudakov/24.VPN/blob/master/images/homework/v1/iperf_tun_tcp.png
[tun_udp]: https://github.com/dbudakov/24.VPN/blob/master/images/homework/v1/iperf_tun_udp.png
[tcp]: https://github.com/dbudakov/24.VPN/blob/master/images/homework/v1/tcp.png
[udp]: https://github.com/dbudakov/24.VPN/blob/master/images/homework/v1/udp.png

### 1.Задание сравнение скорости работы tun и tap. 
Cравнение режимов tap и tun для TCP, слева tap, справа tun   
![tcp]
Cравнение режимов tap и tun для UDP, слева tap, справа tun    
![udp]

### 2. Настройка RAS через openvpn
После деплоя стенда подключение производится из каталога `./roles/templates/pki`, потому-что `ansible`, складывает туда ключи и сертификаты для подключения, подключение производится по команде:  
```
sudo openvpn --config client.conf 
``` 
Проверить подключение можно проверив доступность узла `10.10.10.1`  который является туннельным интерфейсом развёрнутого `server`'a    
### 3. Настройка ocserver
Для проверки потребуется установленный `openconnect` на хостовой машине, после деплоя подключение производится по команде:  
```
sudo openconnect -b 10.10.10.1:8090  
## -b будет запускать клиента  фоновом режиме после установления соединения
```
 Для отключения необходимо ввести:  
```
sudo pkill openconnect
```
