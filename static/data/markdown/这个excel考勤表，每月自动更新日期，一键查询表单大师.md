---
title: 这个excel考勤表，每月自动更新日期，一键查询
date: 2018-06-27 09:49:25
categories: "开发"
tags:
	- 职场
	- Excel

---

多少HR新手每月都要被员工考勤表给折磨，下面这个excel制作的考勤表，可以自动更新每月日期，便捷录入考勤状态，还可以智能统计出勤、休息等各考勤状态数据。是不是很实用 ，跟着小编一起往下看吧~

**智能考勤表**

![这个excel考勤表，每月自动更新日期，一键查询][excel]

首先，制作一个基本excel表，如下图：

![这个excel考勤表，每月自动更新日期，一键查询][excel 1]

需注意的是，excel中第一行需合并，第二行倒数1-2合并，3-5合并。

**接着，自定义考勤月份**

第一行点击右键，选择**“设置单元格格式”**，在弹出的对话框中自定义格式为：表单大师0月份考勤表，设置完成后点击确定，然后第一行随便输入一个月份试试：

![这个excel考勤表，每月自动更新日期，一键查询][excel 2]

**然后，月份自动效果**

当月天数后输入公式=DAY(EDATE(DATE(2018,A1,1),1)-1)，就可以实现输入任意天数，显示当月实际的总天数。

![这个excel考勤表，每月自动更新日期，一键查询][excel 3]

**其次，星期自动效果**

在C4输入公式“ **=TEXT(DATE(2018,$A1,C3),"aaa")** ”，则每个月的日期也可以自动化了：

![这个excel考勤表，每月自动更新日期，一键查询][excel 4]

**接下来，周末自动填充其他颜色**

选中区域然后点击“条件格式-新建规则-使用公式确定要设置格式的单元格”，输入公式**=C$3＞$AF$2**。点击“格式”按钮；然后自定义-类型输入“**;;;**”（三个分号）确定，这样表中仅显示当月日期，不属于当月日期将看不到。

![这个excel考勤表，每月自动更新日期，一键查询][excel 5]

然后选择区域-新建规则，设置公式为“=OR(C$4="六",C$4="日")”,格式填充其他颜色。

![这个excel考勤表，每月自动更新日期，一键查询][excel 6]

Tips：这时可能隐藏的日期也被填充了颜色，这时只需选择数据后选择**条件格式-管理规则**，然后规则设置如下图，就可以解决了。

![这个excel考勤表，每月自动更新日期，一键查询][excel 7]

**最后，统计考勤状态**

在考勤表右侧设计一个备注表，不同的考勤状态不同的形式表示。然后用COUNTIF函数来解决。

公式为“=COUNTIF($C5:$AG5,AI$4)”，制作好备注说明：

![这个excel考勤表，每月自动更新日期，一键查询][excel 8]

最后通过数据有效性设置表格的下拉菜单，效果如下：

![这个excel考勤表，每月自动更新日期，一键查询][excel 9]

这样，一个智能化的考勤表就制作好了。当然你还可以用表单大师来制作一个在线考勤表。这样即使是人员外勤也可以通过定位来打卡，同样数据可以导出到excel也可以通过自带的报表分析功能生成报表自动统计考勤状态。更方便哦~~~

![这个excel考勤表，每月自动更新日期，一键查询][excel 10]


[excel]: static/resources/crawler/UZZE-NNU3-EVY3.gif
[excel 1]: static/resources/crawler/JZJV-YYJU-NQ7V.jpg
[excel 2]: static/resources/crawler/IQBM-JI7N-NF7V.gif
[excel 3]: static/resources/crawler/MYNY-RZZ3-IVZ3.gif
[excel 4]: static/resources/crawler/RYVN-F3YB-JAQU.gif
[excel 5]: static/resources/crawler/JBNB-ANRV-ZFIV.gif
[excel 6]: static/resources/crawler/VV6F-Q2IA-Q6V2.gif
[excel 7]: static/resources/crawler/IJRI-AVVB-NI7F.gif
[excel 8]: static/resources/crawler/Y3QU-2E2Q-EB3U.gif
[excel 9]: static/resources/crawler/A3UB-6FYF-FZ7J.gif
[excel 10]: static/resources/crawler/JQFU-QV63-YYUA.jpg
 *  **原文作者：** 表单大师
 *  **原文链接：** https://www.toutiao.com/item/6571568814054441475/
 *  **版权声明：** 本博客所有文章除特别声明外，均采用 [CC BY-NC-SA 4.0][] 许可协议。转载请注明出处。
