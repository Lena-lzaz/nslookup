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
                  
5) com.

        > com.
        ╤хЁтхЁ:  UnKnown
        Address:  192.168.0.1

        com     nameserver = b.gtld-servers.net
        com     nameserver = m.gtld-servers.net
        com     nameserver = j.gtld-servers.net
        com     nameserver = i.gtld-servers.net
        com     nameserver = a.gtld-servers.net
        com     nameserver = c.gtld-servers.net
        com     nameserver = d.gtld-servers.net
        com     nameserver = k.gtld-servers.net
        com     nameserver = g.gtld-servers.net
        com     nameserver = f.gtld-servers.net
        com     nameserver = l.gtld-servers.net
        com     nameserver = e.gtld-servers.net
        com     nameserver = h.gtld-servers.net
        b.gtld-servers.net      internet address = 192.33.14.30
        b.gtld-servers.net      AAAA IPv6 address = 2001:503:231d::2:
        m.gtld-servers.net      internet address = 192.55.83.30
        m.gtld-servers.net      AAAA IPv6 address = 2001:501:b1f9::30
        j.gtld-servers.net      internet address = 192.48.79.30
        j.gtld-servers.net      AAAA IPv6 address = 2001:502:7094::30
        i.gtld-servers.net      internet address = 192.43.172.30
        i.gtld-servers.net      AAAA IPv6 address = 2001:503:39c1::30
        a.gtld-servers.net      internet address = 192.5.6.30
        a.gtld-servers.net      AAAA IPv6 address = 2001:503:a83e::2:30
        c.gtld-servers.net      internet address = 192.26.92.30
        c.gtld-servers.net      AAAA IPv6 address = 2001:503:83eb::30

    org.
    
        > org.
        ╤хЁтхЁ:  a.root-servers.net
        Address:  198.41.0.4

        org     nameserver = a0.org.afilias-nst.info
        org     nameserver = a2.org.afilias-nst.info
        org     nameserver = b0.org.afilias-nst.org
        org     nameserver = b2.org.afilias-nst.org
        org     nameserver = c0.org.afilias-nst.info
        org     nameserver = d0.org.afilias-nst.org
        a0.org.afilias-nst.info internet address = 199.19.56.1
        a2.org.afilias-nst.info internet address = 199.249.112.1
        b0.org.afilias-nst.org  internet address = 199.19.54.1
        b2.org.afilias-nst.org  internet address = 199.249.120.1
        c0.org.afilias-nst.info internet address = 199.19.53.1
        d0.org.afilias-nst.org  internet address = 199.19.57.1
        a0.org.afilias-nst.info AAAA IPv6 address = 2001:500:e::1
        a2.org.afilias-nst.info AAAA IPv6 address = 2001:500:40::1
        b0.org.afilias-nst.org  AAAA IPv6 address = 2001:500:c::1
        b2.org.afilias-nst.org  AAAA IPv6 address = 2001:500:48::1
        c0.org.afilias-nst.info AAAA IPv6 address = 2001:500:b::1
        d0.org.afilias-nst.org  AAAA IPv6 address = 2001:500:f::1

    ru.
    
        > ru.
        ╤хЁтхЁ:  a.root-servers.net
        Address:  198.41.0.4

        ru      nameserver = a.dns.ripn.net
        ru      nameserver = e.dns.ripn.net
        ru      nameserver = f.dns.ripn.net
        ru      nameserver = d.dns.ripn.net
        ru      nameserver = b.dns.ripn.net
        a.dns.ripn.net  internet address = 193.232.128.6
        a.dns.ripn.net  AAAA IPv6 address = 2001:678:17:0:193:232:128:6
        e.dns.ripn.net  internet address = 193.232.142.17
        e.dns.ripn.net  AAAA IPv6 address = 2001:678:15:0:193:232:142:17
        f.dns.ripn.net  internet address = 193.232.156.17
        f.dns.ripn.net  AAAA IPv6 address = 2001:678:14:0:193:232:156:17
        d.dns.ripn.net  internet address = 194.190.124.17
        d.dns.ripn.net  AAAA IPv6 address = 2001:678:18:0:194:190:124:17
        b.dns.ripn.net  internet address = 194.85.252.62
        b.dns.ripn.net  AAAA IPv6 address = 2001:678:16:0:194:85:252:62
        
6) cs.usu.edu.ru
        
        > ru.
        ╤хЁтхЁ:  UnKnown
        Address:  192.168.43.1

        a.dns.ripn.net  internet address = 193.232.128.6
        
        > edu.ru.
        ╤хЁтхЁ:  a.dns.ripn.net
        Address:  193.232.128.6

        ns.MSU.RU       internet address = 93.180.0.1
        
        > usu.edu.ru
        ╤хЁтхЁ:  ns.msu.ru
        Address:  93.180.0.1

        usu.edu.ru      nameserver = ns.urgu.org
        
        > cs.usu.edu.ru
        ╤хЁтхЁ:  ns.urgu.org
        Address:  212.193.68.254
        
    www.imm.uran.ru
    
        > ru.
        ╤хЁтхЁ:  UnKnown
        Address:  192.168.43.1

        a.dns.ripn.net  internet address = 193.232.128.6
        
        > uran.ru.
        ╤хЁтхЁ:  a.dns.ripn.net
        Address:  193.232.128.6

        ns.URAN.RU      internet address = 195.19.137.69
        
        > imm.uran.ru.
        ╤хЁтхЁ:  ns.uran.ru
        Address:  195.19.137.69

        ns.uran.ru      internet address = 195.19.137.69
        
        > www.imm.uran.ru.
        ╤хЁтхЁ:  ns.uran.ru
        Address:  195.19.137.69
        
    kma.imkn.urfu.ru
    
        > ru.
        ╤хЁтхЁ:  UnKnown
        Address:  192.168.43.1

        a.dns.ripn.net  internet address = 193.232.128.6
        
        > urfu.ru
        ╤хЁтхЁ:  a.dns.ripn.net
        Address:  193.232.128.6
        
        > imkn.urfu.ru
        ╤хЁтхЁ:  [212.193.66.21]
        Address:  212.193.66.21
        
        > kma.imkn.urfu.ru
        ╤хЁтхЁ:  [212.193.66.21]
        Address:  212.193.66.21

        
