#第五十七题
##Insert Interval

插入区间

###版本1
最开始使用erase方法，每判断一个删除一个，结果超时了。于是换成用一个新的向量保存结果，得到结果区间再添加，即可。