

- ```ip a``` komenda wbudowana
- ```ifconfig``` komenda która trzeba zainstalowac (sudo apt net-tools install)
 - pokazannie nazw interfejsów oraz ich konfiguracje (na serwerze linux czasami trzeba najpierw odpalic karty sieciowe dopiero wtedy sie pojawią) ifconfig -a lub ip a
 - pierwsza karta sieciowa nazywa sie enp0s3 druga enp0s8 trzecia enp0s9 
- Konfiguracja karty sieciowej komenda ifconfig (enp0s8)
- ifconfig enp0s8 down
- ifconfig ```enp0s8``` 10.0.0.10 ```netmask``` 255.0.0.0 ```broadcast``` 10.0.0.10 ```gateway``` 10.0.0.10
- ```enp0s8``` -nazwa karty sieciowej na której pracujemy
- ```netmask``` -maska podsieci
- ```broadcast``` -adres rozgłoszeniowy
- ```gateway``` brama

