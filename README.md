# Python-techniques


1.字符串
_______

(1)http://www.cnblogs.com/huangcong/archive/2011/08/29/2158268.html

(2) a.columns = ['sdsdsd']


2.zip 函数
__________

(1)http://www.cnblogs.com/frydsh/archive/2012/07/10/2585370.html


3.drop
_______

(1)http://www.th7.cn/Program/Python/201412/329841.shtml

(2)df.fillna({1:0,2:0.5}) 对第一列nan值赋0，第二列赋值0.5
df.fillna(method='ffill') 在列方向上以前一个值作为值赋给NaN

(3)使用numpy对数据进行计算，有时候会产生nan和inf（或-inf），如以下形式：
dat = np.array( [nan,6,-inf])
如何才能一步把它们除掉呢？推荐使用 for loop加if语句的方法：
cleanedList = [x for x in dat if str(x) != 'nan' and str(x)!= '-inf']

(4)arr = np.array([[1,2,3,4], [5,6,7,8], [9,10,11,12]])
>>> np.delete(arr, [1,3,5], None)
array([ 1,  3,  5,  7,  8,  9, 10, 11, 12])

4.合并df/筛选df
______
(1)http://blog.csdn.net/stevenkwong/article/details/52528616

(2)con3= con2.loc[(con2['cum']<con2['down'])]


5. pandas＋dataframe 攻略
______
(1)http://www.cnblogs.com/chaosimple/p/4153083.html
基本概念那个看了好多遍的网站

（2） data.iloc[2,3]是没有columns 项目的， data.iloc[2:3,3:4]才会有现实列的名字

(3) 改写第一个格子的数值，con2.iloc[0,0]=1，不是0:1没有冒号

(4)删除bb.drop(['new','hi'],axis=1)  ／／ bb.drop([22,33],axis=0)

(5)改写df格式，

float（x）是改写单个http://www.cnblogs.com/wuxiangli/p/6046800.html ；不是数列或者dataframe，http://blog.csdn.net/jinruoyanxu/article/details/68065844


6.下载数据
_____
（1）http://www.open-open.com/lib/view/open1430982247726.html ， urllib中 urlretrieve() 函数

（2）https://jingyan.baidu.com/article/2a138328424ae1074b134f56.html ，查找下载链接，google浏览器去 下载内容里面复制地址


7. 导出excel
_______
(1)xlsx 导出 。 http://blog.csdn.net/apple9005/article/details/54427663

(2)dataxx.to_csv('xxx.csv')   要 是object格式的

（3）pandas导出。http://www.jianshu.com/p/7764b6591cf5, 关于excel处理

8. datetime/ time 函数
_______

(1)http://www.cnblogs.com/tkqasn/p/6001134.html ，介绍的非常详细，还有案例， 重点看这个

(2)三种时间格式相互变化， 单独一种格式自身的变化， 单独时间的更改。

9.画图
________
(1) http://www.cnblogs.com/zhizhan/p/5615947.html 基本画图

（2）矩阵图，相关系数图https://zhuanlan.zhihu.com/p/26100511

（3）基本图形选择图http://www.jb51.net/article/105287.htm



10.sta vs. machine culture
____
Statistical Modeling: The Two Cultures (with comments and a rejoinder by the author)
https://zhuanlan.zhihu.com/p/27263369?group_id=857524243431313408

11. optimize函数
______
（1） 复合函数，比如两分的那种还没找到最优，不知道是不是起点问题

（2）类似solver功能还是能用的

12. list／series／array／dataframe
_____
（1）产生数据框架，等差数列
d1=np.linspace(0.5,1.5,11,dtype=float)
d2=np.linspace(0.5,1.5,11,dtype=float)
d11=[]
for i in range(10):
    d11.append(str(d1[i])+"D1")
d21=[]
for i in range(10):
    d21.append(str(d1[i])+"D2")
d12=pd.DataFrame(0,index=d11,columns=d21)

（2）

