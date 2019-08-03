## fofa 利用脚本

fofascan.py 配合 fofa.sql 使用，先导入mysql数据库结构文件 fofa.sql,功能为利用fofa api下载数据并存入数据库


### 改动日志
<center>
|日期|版本|说明|作者|
|---|---|---|----|
|2019-07-04|<1.0>|fofa 利用脚本|leezp|
</center>
<br/></br>

Fofatqdemo.py 为Fofa提权脚本，带注释，功能是为普通会员突破api下载限制，拥有与高级会员相同权限，最多可下载10000条数据

Fofatq.py 为不带注释的fofa提权脚本，功能与Fofatqdemo.py 一致

<center>
|日期|版本|说明|作者|
|---|---|---|----|
|2019-07-09|<2.0>|fofa 利用脚本|leezp|
</center>
<br/></br>

Fofatqv2.0 为fofa提权脚本2.0,具体改进如下：

1.Fofa每爬取15页左右，返回Status Code: 429 Too Many Requests，这里当页面返回错误时取了最小等待时间20s

2.页面返回错误时重复爬取发生错误的那一页，不遗漏

3.针对ReadTimeout异常，将异常页码捕获，写入ipexcept.txt，方便二次抓取，做到不遗漏每一条数据

<center>
|日期|版本|说明|作者|
|---|---|---|----|
|2019-08-02|<2.1>|fofa 利用脚本|leezp|
</center>
<br/></br>
1.在数据量较大时，比如一次爬取1000页，ipexcept.txt可能存取几十个ip，添加 runipexcept()方法自动爬取ipexcept.txt 里的ip。

### 现状性能分析

爬取144页作为测试，sleep 22次，每次20s,总共耗时566s,算下来解析每一页用时0.87s


### TO DO List

1.增加多线程

2.except 异常嵌套，直接进入最外层异常的问题

3.有时候第二次爬取未获取到数据，仍输出第二次爬取成功
