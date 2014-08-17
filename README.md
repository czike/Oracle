Oracle
======

一些问题:
1.用rownum作为分页时 因为rownum是变化的 就这是为什么会有三层的原因，中间一层是把rownum伪列变为实例；
如select count(1) from (select rownum rn ,t.* from (select *from T) t where rownum > .. ) where rn < ..;

2.如果在一台电脑上安装了oracle的服务端，也安装了客户端，那么在Net Manager的时候，无论服务端 还是客户端都在其相应的
Net Manager中配置连接，网络服务名 最好取来一样，如果不一样 可能会报TNS 连接错误，那么你在用另一个网络服务名试一下就ok了；
