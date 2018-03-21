# nslookup
Зубарева Елена, КН-202

2) *urfu.ru

        > set type=ns
        > urfu.ru
        ╤хЁтхЁ:  UnKnown
        Address:  192.168.0.1

        Не заслуживающий доверия ответ:
        urfu.ru nameserver = ns2.urfu.ru
        urfu.ru nameserver = ns1.urfu.ru
        urfu.ru nameserver = ns3.urfu.ru

        ns1.urfu.ru     internet address = 212.193.66.21
        ns2.urfu.ru     internet address = 212.193.82.21
        ns3.urfu.ru     internet address = 212.193.72.21
        
     *msu.ru
  
        > msu.ru
        ╤хЁтхЁ:  UnKnown
        Address:  192.168.0.1

        Не заслуживающий доверия ответ:
        msu.ru  nameserver = ns.msu.ru
        msu.ru  nameserver = ns3.nic.fr
        msu.ru  nameserver = ns1.orc.ru
        msu.ru  nameserver = ns.msu.net

        ns.msu.ru       internet address = 93.180.0.1
        ns.msu.net      internet address = 212.16.0.1ns1.orc.ru
        ns1.orc.ru      internet address = 212.48.128.152
        ns3.nic.fr      internet address = 192.134.0.49
        ns3.nic.fr      AAAA IPv6 address = 2001:660:3006:1::1:1
        
    Адреса
    
        > nslookup urfu.ru
        ╤хЁтхЁ:  urfu.ru
        Address:  212.193.82.20

        > nslookup rbc.ru
        ╤хЁтхЁ:  rbc.ru
        Addresses:  80.68.253.9
                  185.72.229.9
  
3) 

        > root
        ╤хЁтхЁ яю єьюыўрэш■:  A.ROOT-SERVERS.NET
        Addresses:  2001:503:ba3e::2:30
                  198.41.0.4
                  
4) Команды перехода между серверами

        > server 194.226.235.1
        ╤хЁтхЁ яю єьюыўрэш■:  [194.226.235.1]
        Address:  194.226.235.1
        
       > server ns1.urfu.ru
        DNS request timed out.
            timeout was 2 seconds.
        DNS request timed out.
            timeout was 2 seconds.
        DNS request timed out.
            timeout was 2 seconds.
        DNS request timed out.
            timeout was 2 seconds.
        *** Не найден адрес для сервера ns1.urfu.ru: Timed out
        
        > lserver ns1.urfu.ru
        ╤хЁтхЁ яю єьюыўрэш■:  ns1.urfu.ru
        Address:  212.193.66.21
        
Команду server <имя> используем, если хотим разрешать доменные имена с указанного сервера <имя> (становится деволтным для текущего сеанса. Сменить сервер на другой нельзя.
С помощью команды lserver <имя> это становится возможным, потому что имя другого сервера будет разрешано с вашего DNS-сервера, который стоит по умолчанию.

        > server 194.226.235.1
        ╤хЁтхЁ яю єьюыўрэш■:  [194.226.235.1]
        Address:  194.226.235.1

        > root
        ╤хЁтхЁ яю єьюыўрэш■:  A.ROOT-SERVERS.NET
        Addresses:  2001:503:ba3e::2:30
                  198.41.0.4
