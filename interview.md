1、创建一个空列表，命名为names，往里面添加
Zhangsan、Lisi、Wangwu、Zhaoliu、LiuBei和Guanyu元素。

答：names = ["Zhangsan", "Lisi", "Wangwu", "Zhaoliu", "LiuBei", "Guanyu"];

2、往(1)
中的names列表里Guanyu前面插入一个Zhangfei。

答：names.insert(-1, "Zhangfei");

3、把names列表中LiuBei的名字改成中文。

答：names[names.index("LiuBei")] = "刘备";

4、往names列表中Wangwu后面插入一个子列表["Xiaoqiao", "Daqiao"]。

答：names.insert(2, ["Xiaoqiao", "Daqiao"]);

5、返回names列表中Zhaoliu的索引值（下标）。

答: print(names.index("Peiqi"));

6、创建新列表[1, 2, 3, 4, 2, 5, 6, 2]，合并到names列表中。

答: numbers = [1, 2, 3, 4, 2, 5, 6, 2]

names.extend(numbers)  # extend()方法表示合并

print(names)

7、取出names列表中索引4 - 7
的元素。

答: print(names[4:8])

8、取出names列表中索引2 - 10
的元素，步长为2。（考点列表切片）

答: print(names[2:11:2])  # 列表切片“顾头不顾尾”，步长表示在指定范围间隔取值

9、取出names列表中最后3个元素。

答: print(names[-3:])  # [-3:]表示取值范围从列表的倒数第三个到末尾

10、循环names列表，打印每个元素的索引值和元素。

答:

# 方法一

for i in names:
    print(names.index(i), i)

# 方法二

for index, i in enumerate(names):
    print(index, i)

11、循环names列表，打印每个元素的索引值和元素，当索引值为偶数时，把对应的元素改成 - 1。（考点列表元素，索引循环）

答:

for index, i in enumerate(names):

    if index % 2 == 0:
        names[index] = -1

        print(index, 1)

print(names)

12、names列表里有3个2，请返回第二个2的索引值，不要人肉，要动态找。（考点列表循环）

答:

# 方法一 循环

count = 0

for index, i in enumerate(names):

    # print(index,i)

    if i == 2:

        count += 1

        while count == 2:
            print(index)

            break

    else:

        continue

# 方法二

print(names.index(2, names.index(2) + 1))

13、现有商品列表如下：（考点 - 列表，循环）

　　products = [["华为", 6888], ["小神通", 14800], ["小米9", 2499], ["瑞幸咖啡", 31], ["小黄书", 60],
              ["李宁", 699]]，需打印出以下格式：使用enumerate(）函数

                                                 - -----商品列表 - -----

华为
6888

小灵通
14800

小米9
2499

瑞幸咖啡
31

小黄书
60

李宁
699

参考答案如下：

products = [["华为", 6888], ["小灵通", 14800], ["小米9", 2499], ["瑞幸咖啡", 31], ["小黄书", 60], ["李宁", 699]]

for index, i in enumerate(products):
    print("%s %s   %s" % (i[0], i[1]))
