# 实验名称
SM3 length extension attack

# 实验完成人
权周雨 

学号：202000460021 

git账户名称：baekhunee

# 长度扩展攻击
对于MD结构，长度扩展攻击的过程如下所示：
![image](https://user-images.githubusercontent.com/105578152/180902136-e14f707e-df99-45a7-bd34-5669c417f3bf.png)

本次实验针对SM3进行长度扩展攻击，攻击过程大体如下：

1、对任意消息r1，首先对其进行填充，得到 m=r1||padding；

2、调用SM3计算哈希值即 h1=SM3(m,IV)；

3、自选r2作为进行攻击的消息，计算 h2=SM3(m||r2,IV)即h2=SM3(r1||padding||r2,IV)；

4、计算 h3=SM3(r2,iv)，其中iv=h1即先前消息的哈希值；

5、比较h2与h3是否相同，若相同，则攻击成功。

# 测试截图

## Python
![image](https://user-images.githubusercontent.com/105578152/180903642-67e23807-be6b-40ad-9ef7-292a67ecd06f.png)

## C++
![image](https://user-images.githubusercontent.com/105578152/180905858-89fd4e2b-fecf-4ab6-9841-5fd4235476b2.png)
