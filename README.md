## Домашнее задание  
VPN   
Цель: Студент получил навыки работы с VPN, RAS.   
1.Между двумя виртуалками поднять vpn в режимах  
- tun  
- tap  

2.Поднять RAS на базе OpenVPN с клиентскими сертификатами, подключиться с локальной машины на виртуалку   

3.\* Самостоятельно изучить, поднять ocserv и подключиться с хоста к виртуалке   

## Решение  
[logo1]
[logo2]
1.Задание сравнение скорости работы tun и tap. 
В режиме tap мы получаем следующий вывод на клиенте по протоколу tcp и далее вывод по udp:
![logo1]
Вывод теста iperf  через tun туннуль:
![logo2]
