# Python3.8+使用pymouse库

> 会产生报错`ModuleNotFoundError：No module named ‘window’`
> 
1. 找到python安装目录下\lib\site-packages\pymouse_*init*_.py，第92行把windows => pymouse.windows
    
    ![Untitled](Python3%208+%E4%BD%BF%E7%94%A8pymouse%E5%BA%93%20eaf60d0e02374694b95b241c59f18897/Untitled.png)
    
2. 此时在运行会产生报错`ModuleNotFoundError：No module named ‘pyHook’`，去官网下载一个PyHook，我使用的是3.8版本python只能使用pywinhook，[下载地址](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pywinhook)（32位还是64位参照自己的系统）
    
    ![Untitled](Python3%208+%E4%BD%BF%E7%94%A8pymouse%E5%BA%93%20eaf60d0e02374694b95b241c59f18897/Untitled%201.png)
    
3. 下载后的包，使用pip进行安装
    
    ![Untitled](Python3%208+%E4%BD%BF%E7%94%A8pymouse%E5%BA%93%20eaf60d0e02374694b95b241c59f18897/Untitled%202.png)
    
4. 安装成功后，再编辑python安装目录下lib\site-packages\pymouse\[windows.py](http://windows.py/)"修改第23行
    
    ![Untitled](Python3%208+%E4%BD%BF%E7%94%A8pymouse%E5%BA%93%20eaf60d0e02374694b95b241c59f18897/Untitled%203.png)
    
5. 测试一下环境是否成功

```python
>>> import pymouse
>>> m = pymouse.PyMouse()
>>> print(m.position())
(494, 407)
```