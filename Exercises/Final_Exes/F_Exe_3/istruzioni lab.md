# TODO

Assegnare ad ogni router un Router ID che faccia riferimento al numero del
dispositivo (es R1=1.1.1.1, etc)

Configurare le adiacenze EBGP e IBGP

Su R1\R2 annunciare le reti rappresentate dalla rispettive loopback
Accertarsi che R4 riesca a pingare le loopback di R1\R2.

Annunciare su R4 la rete rappresentata dalla loopback 0

Verificare la presenza di tutte le route su tutti i router e verificare la loro raggiungibilità con il ping esteso facendo partire i messaggi ICMP dalle rispettive loopback

Configurare BGP affinchè R1 utilizzi R2 per raggiungere la rete 10.4.4.0/24, SENZA APPORTARE
ALCUNA MODIFICA SU R1\R2.

Verificare che R1 veda ora la best route per 10.4.4.0/24 via R2

Su R1 creare due loopback con ip 192.168.1.1/32 e 172.16.1.1/32

Su R1 annunciare 192.168.1.1/32 solo verso R2 e 172.16.1.1/32 solo verso R3

Su R1 verificare, con l'apposito comando, le route che il router locale annuncia verso R2 e R3

Assicurarsi che il prefisso 192.168.1.1/32 non venga annunciato da R2 verso R3 . Non utilizzare
access-list o prefix-list.

Assicurarsi che il prefisso 172.16.1.1/32 non venga annunciato da R3 verso R2 e R4. Non utilizzare
access-list o prefix-list.

Assicurarsi che la loopback del router R4 possa comunque raggiungere le due reti (172.16.1.1/32 e
192.168.1.1/32) tramite una default route generata da R1 verso i due neighbor R2 e R3