#### 常见错误:
*  "ImportError: No module named win32api"
原因是缺少win32,到 http://sourceforge.net/projects/pywin32/files/
找到对应的版本进行下载，直接安装即可
* "UnicodeDecodeError: 'ascii' codec can't decode byte 0xe6 in..."
原因就是Python的str默认是ascii编码，和unicode编码冲突，就会报这个标题错误。那么该怎样解决呢？
通过搜集网上的资料，自己多次尝试，问题算是解决了，在代码中加上如下几句即可。
```
import sys
reload(sys)
sys.setdefaultencoding('utf8')
