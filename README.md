##JAVA实现概率计算（数字不同范围按照不同几率产生随机数）
如果要在某个数字区间产生一个随机数，区间内部在不同的片段几率不同如何实现呢？经常有这样的场景，比如，随机赠送红包，范围0.1元-100元，0.1-1元的概率是90%,1元-10元的概率是9%，10元-100元的概率是1%，也就是说数额越大得到的几率越小！实现的原理如下图：<br/>
![随机原理]https://github.com/cloudskys/algorithmic/blob/master/src/main/webapp/orgi.png
##原理就是，将范围分割成一个个子范围（片段），具体采用哪个范围，再用机率判断。片段机率可以依次排好序，映射成[1,100]之间的数字。然后随机一个[1,100]之间的数，该数落在哪个区间，就采用哪个片段产生随机数。具体源代码如下：