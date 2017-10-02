#模块导入原理
模块导入赋值代码给同名变量
包导入 执行__init__.py
#模块分类
##标准库
###time
时间格式
####时间戳
time.time()
当前时间-1970-1-1 0:0:0(unix诞生日)的间隔时间换算成秒
time.sleep(2)
睡2秒
time.gmtime(*args) UTC
time.localtime(*args) d8
时间戳time.time()——————>struct_time(tuple)
|
|
|
v
格式化字符串
>>> time.strftime("%Y/%m/%d %H:%M:%S",time.localtime())
'2017/10/02 08:54:39'
>>> time.strftime("%Y/%m/%d %H:%M:%S",time.gmtime())
'2017/10/02 00:54:50'
>>> time.strptime('2017/10/02 08:54:39',"%Y/%m/%d %H:%M:%S")
time.struct_time(tm_year=2017, tm_mon=10, tm_mday=2, tm_hour=8, tm_min=54, tm_sec=39, tm_wday=0, tm_yday=275, tm_isdst=-1)
>>> time.ctime(1505321542)
'Thu Sep 14 00:52:22 2017'
>>> time.asctime(time.localtime())
'Mon Oct  2 09:17:09 2017'

#datetime
>>> datetime.datetime.now()
datetime.datetime(2017, 10, 2, 9, 19, 58, 765190)
>>> datetime.datetime.now()-datetime.timedelta(3)
datetime.datetime(2017, 9, 29, 9, 20, 37, 364468)
>>> datetime.datetime.now()+datetime.timedelta(hours=3)
datetime.datetime(2017, 10, 2, 12, 21, 21, 141837)
#顾头不顾尾
>>> random.randrange(1,2)
1
>>> random.randint(1,2)
2
>>> random.choice('hello')
'h'
>>> random.choice([1,3,4])
3
#随机字符序列
>>> random.sample('hellonihao',2)
['h', 'o']
#浮点随机
>>> random.uniform(1,4)
2.138955978558179
#洗牌
>>> a=[1,2,3,4,5,6]
>>> random.shuffle(a)
>>> a
[4, 1, 3, 6, 2, 5]


