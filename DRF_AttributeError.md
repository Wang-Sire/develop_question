##django_question - DRF    
    Got AttributeError when attempting to get a value for field `robot_chinaese` on serializer `RobotListSerializer`.
    The serializer field might be named incorrectly and not match any attribute or key on the `QuerySet` instance.
Original exception text was: 'QuerySet' object has no attribute 'robot_chinaese'. ---------
大意：当序列化RobotListSerializer时发生了一个错误，又一个属性错误，robot_chinaese 这个字段错误。
这个序列化的字段可能不存在，或者是错误的
#####serializer.py 文件
![](/Users/wang/Desktop/截屏2020-03-18下午4.42.48.png)
##### models.py
![](/Users/wang/Desktop/截屏2020-03-18下午4.43.07.png)
##### views.py。 ** 错误范例**
![](/Users/wang/Desktop/截屏2020-03-18下午4.44.34.png)
# 上图就是报错现场！！！！
原因就是 many = True 没有写
![](/Users/wang/Desktop/截屏2020-03-18下午4.44.58.png)
加上后就OK了！
后续我会查看源码分析！----


