Podsieci i nadsieci IP
----------------------

adresacja
-----------------------------------------------------
| PC     |  interfejs   | adres  |
| --------- |:-------------| :---------------| 
| ``PC1``   | enp0s3 | 192.168.100.10/24     |
| ``PC-R-1``| enp0s3 | 192.168.100.1/24    |
| ``PC-R-1``| enp0s8 | 192.168.200.97/29      |
| ``PC-R-2``| enp0s3 | 192.168.200.98/29      |
| ``PC-R-2``| enp0s8  | 192.168.0.129/27       |
| ``PC-R-2``| enp0s9  | 192.168.0.65/27     |
| ``PC-R-2``| enp0s10 | 192.168.0.193/27     |
| ``PC2``   | enp0s3  | 192.168.0.130/27      |

routing
-------

| destination | trasa | interfejs  |
| --------- |:-------------| :---------------| 
| ``PC1``     |  | |
| ``default`` | 192.168.100.1 | enp0s3 ``ip route add default via 192.168.100.1`` |
| ``PC-R-1``  |  |        |
| ``192.168.100.0/24`` | 192.168.100.1 | enp0s3 |
| ``192.168.200.0/24`` | 192.168.200.1 | enp0s8 |
| ``192.168.0.0/24``   | 192.168.200.2 | enp0s8 |
| ``PC-R-2``  |  |        |
| ``192.168.0.0/24`` | 192.168.0.1 | enp0s3 |
| ``192.168.200.0/24`` | 192.168.200.2 | enp0s8 |
| ``192.168.100.0/24``  | 192.168.200.1  | enp0s3 |
| ``PC2``  |  |
| ``default`` | 192.168.0.1 | enp0s3 ``ip route add default via 192.168.0.1`` |

```w r2
nie dodaje auto rutingu 192.168.100.0/24
w r1 192.168.0.0/24 (to co jest jako drugie w pliku interfaces)
```

Zadanie
------------

![zadanie 5](over_network.svg)

1.
   * Przygotuj konfigurację sieci zgodnie z powyższym diagramem
   * W pierwszej kolejności przygotuj ``PC1``, ``PC-R-1``, ``PC-R-2``, ``PC-2``
   * Do konfiguracji wykorzystaj dane z tabeli powyżej
   * Rozszerz istniejącą konfigurację dzieląc istnijącą sieć dla ``PC2`` na 3 podsieci zgodnie z diagramem
   * Przetestuj połączenie pomiędzy wszystkimi elementami sieci ``PC1->PC2`` ``PC1->PC4``
   * Zapewnij permanentną konfigurację, dodając odpowiednie wpisy w plikach konfiguracji

Zadanie do domu
---------------

1. Wykorzystując program dia oraz ikony CISCO
  * Przygotuj diagram powyższej sieci uwzględniając urządzenia tj:
    * ROUTER
    * SWITCH
    * PC
  * Uzupełnij diagram o adresację sieci oraz poszczególnych urządzeń
  
