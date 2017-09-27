what data can we gather?
- [ ] which experiments should be executed?
blocking probability:The blocking probability is the ratio of the number of blocked calls to the total number of calls simulated
percentage of optimality checks:the percentage of calls for which the optimality (least cost) of the SRLG diverse path pair is verified
average number of iterations:the average of the total number of iterations executed by the heuristics (ITSH or IMSH) for computing the diverse path pair for the number of calls simulated

Average Hap count of Active Path: Most of the network traffic
routes along active path. The more hops packets have to pass,
the longer paths are created, Therefore, reducing the active
path length and its total assigned bandwidth yields proper
utilization of bandwidth

- [x] what sorts of algorthm should be compareable?
ITSH IMSH (amount to SPP) min sum   compare time
COSE ILP

20160619:
- [ ] how to use qqwry to deal with the Ctrace.the address of ip is so concrete because the ip address is not Ip of the main backbone network.
222.46.53.159   222.46.53.159   浙江省嘉兴市 嘉兴学院(越秀南路56号)
222.46.53.160   222.46.53.234   浙江省嘉兴市 铁通
222.46.53.235   222.46.53.235   浙江省嘉兴市平湖市 雪尼猫音像中心
222.46.53.236   222.46.55.255   浙江省嘉兴市 铁通
222.46.56.0     222.46.57.255   浙江省绍兴市 铁通
1.cluster many IP which is same prefix.
2.get rid of Ip is ,do not make up related link
- [x] Ctrace include many  path,invalidate path.
- [x] popdata is transformed into standard style .
- [x] take multiedge into consideration(first pre deal the data in order to at most two edges which are composed into multiple edge)

20160710:
- [x] if node have value and edge do not have value,then how to apply my algorithm in the situation
one edge just belong only one SRLG。 

20160711:
- [x] transforming the node of star property,should just transform the node through AP or the node is random
- [x] when s==d,equivalent to find some path from  begining(neighbor s) to ending(d)   

20160112：
- [x] take the undirected graph into consideration,how to deal with the networkflow algorithm.

20160714
- [x] preprocess the data ,to ensure the graph is undirected connected graph

20160117：
- [x] how to know how much thread is in paralle in fact?
- [x] we could  deal with essential node tsp by muitithread, i need the optimal answer,not the approximate answer ,ILP solver。

20160718：
- [x] memorize search.
- [x] notice the mustnot pass array and must pass array mutually assign
- [x] take the directed graph's multiedge into consideration
- [x] if the path must pass some node or edge,the inclusion would be more small.
- [x] data scale:2000's node ,outdegre is 3 5 runtime is 30s
- [x] ask teacher to let her apply data and resource from this competition

20160722：
- [x] preprocess the data ,must not include the loop edge.

20160224：
- [x] the node scale is assigned into twenty unit ,every unit interval is 100

20160820:
- [x] tidy the topo,demand and srlg's file.
- [x] topo：huawei's data
- [x] srlg:5%- 90% star or neighbor star,should wirte generating code for srlg.
demand:
- [x] huawei judge system.
- [x] install matlab in linux >need big storage 

20160821：
star node,the all adjacent edges of the node is assigned into the one srlg or part?(i firstly set all adjacent edges is belong the one srlg )

20160824
the algorithms just run 30s .
- [ ] the glpk have itself internal bug.(glp_set_obj_coef)

20160825：
in dense and less srlg graph  ,my algorithm can use compress node shortest path to find mustnode path.
in undirected graph ,we should add reverse edge which in the same srlg with forward edge.


20160831
had i better use commercial library of ILP
when the graph is dense , our algorithm may use dijstra to find must node path.
- [x] write localsolver code
- [x] find some tool to show this graph dynamically
- [x] write annonation 
- [x] find more comparable algorithm 

20160903
- [x] when finding AP,if there is not must node ,i can use dijstra algorithm find AP.
- [x] ILP algorithm can have two versions.IQP or ILP

20160904
- [x] finding AP path code of my algorithm notice every node is passed just once.


20160914
- [x] we just pass less must node,could enum the order of must nodes,use sort dijstra to find AP.

20160915
- [x] collect graph of various types 
- [x] find website of storaging network' topological graph

 
 
20161003
- [x] COSE还有点bug  1 5 6 11

20161010
- [x] 每一个算法画一条线
- [x] 18组数据归一化，求平均值
- [x] 两个图：平均值，方差
- [x] 选择一组数据，求倍差
- [x] 1.最近几年的论文比较
- [x] 2.实验图2的形式
- [x] 3.归一化，平均值

共享风险集比例的增加，而性能提高

4.SRLG敏感性分析

20161012
- [x] COSE ()becasue of the time's limitation,COSE return a near- [ ] optimal answer) 
- [x] KSP (pthread problem,pthred_cancel)

20161012
KSP get no answer when its code is put after other.
result- [ ] >APSum
Count of SRLG between the AP/BP
there exist a paper which use the method put by me solve the multi- [ ] objection
find many testcase in these paper.

20161016
COSE runtime time exceed 10s

20161017
min- [ ] min and min- [ ] sum can be put into consideration together.

20161204
i think our algorithm may be the optimal solution for solving SRLG- [ ] disjoint min- [ ] min
could we utilize bloomfilter into the SDN's flowtable 
ask xiegaogang ,the application

20161216
- [x]  [].允许算法在规定时间内找路失败（即允许算法是概率多项式算法）
- [x]  [].范数里还有那些范数能解决这种问题
- [x]  [].适用于图中找点的数据结构和数学理论
 
子问题是不是相对于原问题上，求得解的概率要大

20170110
- [ ]  we could analysis the properties, result of topological graph

20170305
- [x]  the algorithm could be extended to be utilized to sovle min-sum or min-max?
> just discuss the differntce among min- min with minsum and min-max.
solve domain-disjoint paths


20170310
three dimension idea to solve SRLG
- [ ] how to decide which edge is belonging which SRLG
- [x] find a graph tool that can show topo's figure.
> contact huawei's engineer
>19大规模网络拓扑可视化工具的研究综述
- [ ] i should write a program that is used to chech wether the answer is right
- [ ] how to process edge or node of multiconstrain ? the most addition norm
- [ ] can or how to use convex theory verify that the ILP model is not convex
- [ ] what different influence are there in the dense or sparse graph?
Dense and Sparse Graphs
dense:the ITSH,IMSH is easily finding the answer.
sparse:

i:we solve the min- min srlg two- disjoint directed problem ,then we could extend it to n- disjoint???
large: my algorithm and ILP spend much time finding the answer.
- [ ] process 12_video_info file into demand.csv,every line is a demand request
用户IP source,服务器IP destination,开始时间 ,观看时长
- [ ] output note file inlcude the information about node edge's number ,average or maxmimum node and edge indegree and outdegree
- [ ] our algorithm optimize the cost of SRLG- disjoint path pair without consideraing bandwidth sharing

20170319
- [ ] k-SRLG-connectivity theorem is proposed by us. 


20170517
- [ ] the fifth sample 

- [ ] ksp time complexity
- [ ] APF


- [x] Promise
- [x] normalized

execvp: Permission denied
failed to execute ./Debug/CSLSAlgorithmi
do not add permission to shell script