# 项目 3: 非监督学习
## 创建用户细分

### 项目概述
在此项目中，你将对为葡萄牙里斯本的批发商收集的客户产品开支数据应用非监督学习技巧，以便发现数据中隐藏的客户细分信息。首先，你将探索数据：选择一小部分样本子集并判断产品类别之间是否相互关系紧密。之后，你将通过缩放每个产品类别预处理数据，然后发现（并删除）不需要的离群值。留下良好的客户开支数据后，你将对数据应用 PCA 转换，并实施聚类算法，以便划分转换后的客户数据。最后，你将比较细分结果与额外的标签信息，并思考这些信息可以帮助批发商日后改进服务的方式。

### 项目说明
某个批发商最近针对某些客户进行了送货方式试点更改，从一周五天上午送货服务变成了成本更低的一周三天晚上送货服务。初始测试并没有发现任何明显不理想的结果，因此他们针对所有客户都采取了成本更低的送货方式。但是很快，批发商就收到客户关于送货服务变化的投诉，有客户取消了送货服务，导致批发商损失的金额比节省的更高。批发商聘请你来帮助他们了解他们的客户类型，以便日后做出更好、更明智的商业决策。你的任务是使用非监督式学习技巧判断客户之间是否有相似之处，以及如何以最佳方式将客户细分成明显的类别。


### 安装

这个项目要求安装下面这些python包：

- [NumPy](http：//www.numpy.org/)
- [Pandas](http：//pandas.pydata.org)
- [scikit-learn](http：//scikit-learn.org/stable/)

你同样需要安装好相应软件使之能够运行[Jupyter Notebook](http://jupyter.org/)。

优达学城推荐学生安装 [Anaconda](https：//www.continuum.io/downloads), 这是一个已经打包好的python发行版，它包含了我们这个项目需要的所有的库和软件。

### 代码

初始代码包含在 `customer_segments.ipynb` 这个notebook文件中。这里面有一些代码已经实现好来帮助你开始项目，但是为了完成项目，你还需要实现附加的功能。

### 项目文件

customer_segments.ipynb：这是主要文件，你将在此文件中执行项目任务。
customers.csv：项目数据集。你将在 notebook 中加载此数据。
visuals.py：此 Python 脚本提供了项目的补充可视化内容。请勿修改此文件。

## 数据

​这个项目的数据包含在 `customers.csv` 文件中。你能在[UCI 机器学习信息库](https://archive.ics.uci.edu/ml/datasets/Wholesale+customers)页面中找到更多信息。

- **特征**

* `Fresh`: 购买生鲜产品的年支出(m.u.)(连续)； 
* `Milk`: 购买奶制品的年支出(m.u.)(连续)；
* `Grocery`: 购买杂货品的年支出(m.u.)(连续)； 
* `Frozen`: 购买冷冻产品的年支出(m.u.)(连续)；
* `Detergents_Paper`: 购买清洁产品和纸制品的年支出(m.u.)(连续)；
* `Delicatessen`: 购买熟食的年支出(m.u.)(连续)； 
* `Channel`: {酒店/餐馆/咖啡厅 - 1, 零售 - 2} (Nominal)
* `Region`: {里斯本 - 1, 波尔图 - 2, 其他 - 3} (Nominal) 
