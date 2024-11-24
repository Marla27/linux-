

- `ip a` komenda wbudowana
- `ifconfig` komenda która trzeba zainstalowac (sudo apt net-tools install)
 - pokazannie nazw interfejsów oraz ich konfiguracje (na serwerze linux czasami trzeba najpierw odpalic karty sieciowe dopiero wtedy sie pojawią) ifconfig -a lub ip a
 - pierwsza karta sieciowa nazywa sie enp0s3 druga enp0s8 trzecia enp0s9 
- Konfiguracja karty sieciowej komenda ifconfig (enp0s8)
- ifconfig enp0s8 down
- ifconfig `enp0s8` `10.0.0.10` `netmask` 255.0.0.0 `gateway` 10.0.0.1 `up`
- ```enp0s8``` -nazwa karty sieciowej na której pracujemy
- ```netmask``` -maska podsieci
- ```broadcast``` -adres rozgłoszeniowy
- ```gateway``` brama
- ```up``` uruvhamia karte sieciowa spowrotem
- Konfiguracja karty sieciowej komenda ip a (enp0s8)
- ip l set down enp0s8 
- ip a add `10.0.0.10`/255.0.0.0 `10.0.0.1` dev `enp0s8`
- ip l set up enp0s8
- Analiza
- `1.0.0.10` - adres sieciowy
- `10.0.0.1` - brama
- `enp0s8` nazwa interfejsu który edytujemy 
- Uruchomienie konfiguracji dhcp
- dhclient enp0s8
- usuwanie kofiguracji interfejsu
- ip a del  `10.0.0.10` dev `enp0s8`
- `enp0s8` nazwa interfejsu
- `10.0.0.10` adres IP