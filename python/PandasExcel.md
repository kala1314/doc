## Pandas  Excel

### 读取Excel 

* 单个sheet页读取 

  ```python
  import pandas as pd 
  df = pd.read_excel("filname.xlsx")
  ```

  

* 多个sheet页读取

  ```python
  # sheet_name 参数可以使用数字，莫从第一个sheet页为0
  
  # 读取第二个sheet 页
  # 写法一
  df = pd,read_excel("filename.xlsx", sheet_name=1)
  # 写法二(sheet_name=后面的名字是Excel中sheet页名称相同)
  df = pd.read_excel("filename.xlsx", sheet_name="Sheet2")
  
  # 同时读取多个sheet页
  # 同时读取第一个和第二个sheet页（可用数字，也可sheet名）
  df = pd.read_excel("filename.xlsx", sheet_name=[0, 1])
  
  # 多个sheet读取之后操作一个sheet数据
  # 输出第一个sheet页A列数据(这个需要用到A列的Header)
  print(df[0].uid) # uid 为A列的header
  ```

  

* 设置列名：header 

  ```python
  # header = 0 设置第一行为列名
  df = pd.read_excel('filename.xlsx', sheet_name=0, \
                    header=0)
  
  # 获取所有的列名
  print(df.columns)
  
  # 如果有的列名是空的，可以用names=[]重新设置
  df = pd.read_excel('filename.xlsx', sheet_name=0, \
                    names=['uid', "name", "age"])
  # names=[] 是要从第一个开始设置，里面的元素和Excel的列数是一样多的
  ```



### Excel 行和列

* 连续多行的选择 类似于Python的列表切片

  ```python
  # 获取1-3行的数据
  print(df[:3])
  ```

  

* 按照指定的索引选择一行或多行，使用loc[]方法()  loc() 行标签

  ```python
  print(df.loc[:"GT1005"])
  ```

  

* 按照指定的位置选择一行多多行，使用iloc[]方法   iloc() 行索引

  ```python
  print(df.iloc[:5])
  ```

  

* 列

  ```python
  # 查看索引行或者或者索引列
  print(df.index)
  print(df.columns)
  ```

* 或者某一列

  ```python
  # df[]
  print(df["产品编号"])
  # df.
  print(df.产品编号)
  ```

  

#### 筛选数据

* 比较筛选

  ```python 
  df = df[df["销售量"]  > 5]
  ```

* 判断筛选

  ```python
  df = df[df["产品"] ！= "电冰箱"]
  ```

  

* 