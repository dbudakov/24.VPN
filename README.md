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

1.Задание сравнение скорости работы tun и tap. 
Cравнение режимов tap и tun для TCP, слева tap, справа tun  
![tcp]
Cравнение режимов tap и tun для UDP, слева tap, справа tun  
![udp]
