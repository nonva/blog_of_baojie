语义网中的推理是不是银弹？(2) RDF和Datalog
---
    
> Categories: 旧文, 语义网  
> Time: 2011-04-25  
> Original url: <http://baojie.org/blog/2011/04/25/silver-bullet/>
    
续[语义网中的推理是不是银弹？(1)](http://baojie.org/blog/2011/04/10/silver-bullet/)

【datalog现在换了一个新名字RIF又杀回来了。不过我觉得，RIF的下场，也会很小众。光工具的开发，至少还要5年的时光。到时候会不会来一个简化的RIFa？呵呵】

2007-06-11：**RDF和Datalog**

把RDF存储等同于一张表是一个很大的误解。实际上，关系数据库也可以用一张表作所有的事（第一范式）。

RDF用关系数据库存储，只是一个syntax，关键在于RDF推理规则，这是超越关系数据库的。

zhaonix回复说

> 1. 基于轻量级的本体所建的RDF triple库，其中 推理 能有多少用武之地呢？ 
> 2. 即使是“关键在于RDF推理规则”。推理也是算法，推理机也是程序，并不神秘。试想：如果推理中需要用到上百万、上千万条triple中的某三五条所蕴藏的信息的话，没有一个好的存储方案、索引算法（类似于RDBMS那样的）的话，效率怕是低得不可忍受的。


我回复说：     

> 1. 如果不是要推理，要RDF干什么？数据库就好了。轻量级本体，哪怕分类树，也是推理。 
> 2. 见ESWC最新的关于RDF Index的文章。


smileidiot回复说：
> 如果说RDF推理规则，那么何不回到Deductive Database（或称Datalog）？貌似工业界并没有对此推崇，依旧是Relational Database的天下。。。如果说Datalog比SQL就是多了个Recursion问题，那么除去性能之外，据我所知，已有多年研究工作，如semi-naive方法，为何依旧没有市场呢？是需求问题，还是效率问题呢？我不得解


我回复说：
> Datalog的问题是很多问题根本不可判定，更谈不上复杂性了（注：这个我说错了，后来纠正了）。RDF要比Datalog“肤浅”的多。RDF的一些子集，有很好的查询复杂性（见ESWC2007的最佳paper）。
> 
> Datalog比SQL多了当然不只Recursion。毕竟Logic Programming比RDB的建模能力还是强出很多。应该说，当前的SW研究，在寻找一个在关系数据库和演绎数据库之间的数据建模手段，也即在表达力之间和复杂性之间寻找“合理”的折衷。


---

后面跟有[一系列datalog的讨论](http://bbs.w3china.org/dispbbs.asp?BoardID=2&id=48213&replyID=95599&star=3&skin=0)，有些参考价值     
    