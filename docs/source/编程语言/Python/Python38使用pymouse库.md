# Python38使用pymouse库

### 遇到这个报错时`ModuleNotFoundError：No module named ‘window’`，解决如下：

1. 找到python安装目录下\lib\site-packages\pymouse_*init*_.py，第92行把windows => pymouse.windows
    
    ![](https://git.poker/raoyun/photo/blob/master/20220714/Untitled.3bhbfz517p80.webp?raw=true)
    
2. 此时在运行会产生报错`ModuleNotFoundError：No module named ‘pyHook’`，去官网下载一个PyHook，我使用的是3.8版本python只能使用pywinhook，[下载地址](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pywinhook)（32位还是64位参照自己的系统）
    
    ![](https://git.poker/raoyun/photo/blob/master/20220714/Untitled-1.6e6cpkekh580.webp?raw=true)
    
3. 下载后的包，使用pip进行安装
    
    ![](https://git.poker/raoyun/photo/blob/master/20220714/Untitled-2.4c2o1gn5s3a0.webp?raw=true)
    
4. 安装成功后，再编辑python安装目录下lib\site-packages\pymouse\[windows.py](http://windows.py/)"修改第23行
    
    ![](https://git.poker/raoyun/photo/blob/master/20220714/Untitled-3.53dmtlirk9k0.webp?raw=true)
    
5. 测试一下环境是否成功
    
    ```python
    >>> import pymouse
    >>> m = pymouse.PyMouse()
    >>> print(m.position())
    (494, 407)
    ```
