Ustawianie parametrów sieci
---------------------------

![alt text][network]

[network]: ./network.png "Logo Title Text 2"

1. na 1 z komputerów zainstaluj oprogramowanie ``http-chat`` dostępne pod adresem ``https://github.com/jkanclerz/http-chat``

Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 10.0.15.4 | |
| MASKA  | /24 (255.255.255.0) | |
|   |  | |
| PC 2  |  | |
| IP - address  | 10.0.15.6 | |
| MASKA  | /24 (255.255.255.0 )| |

Weryfikacja połączenia

Polecenie
curl -X POST -d '{"text": "Hello World"}' http://192.168.10.6:8888/chat curl -X POST -d '{"last_message_id":-1}' http://192.168.10.6:8888/messages

Efekt
```
```

Statyczna konfiguracja parametrów połączenia
Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 192.168.10.10 | |
| MASKA  | 255.255.255.0 | |
|   |  | |
| PC 2  |  | |
| IP - address  | 172.16.100.100 | |
| MASKA  | 255.255.0.0 | |

Weryfikacja połączenia

Polecenie
```
```

Efekt
```
```

Nowa statyczna konfiguracja 

-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  |  | |
| MASKA  |  | |
|   |  | |
| PC 2  |  | |
| IP - address  |  | |
| MASKA  |  | |

Weryfikacja połączenia

Polecenie
```
```

Efekt
```
```

Warto wiedzieć
--------------

-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
| Lokalizacja pliku z konfiguracją sieci| | |
| UP -> Wyłączenie interfejsu sieciowego| |ifup|
| DOWN -> Włączenie interfejsu sieciowego| |ifdown |
| Sprawdzenie obecnych parametrów | |ip addr |
| lista wszystkich interfejsów | | |
| Które interfejsy jakie porty słuchają | | |

