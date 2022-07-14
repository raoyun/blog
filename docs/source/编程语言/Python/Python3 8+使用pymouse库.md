# Python3.8+使用pymouse库

<aside>
💡 会产生报错`ModuleNotFoundError：No module named ‘window’`

</aside>

1. 找到python安装目录下\lib\site-packages\pymouse_*init*_.py，第92行把windows => pymouse.windows
    
    ![Python3%208+%E4%BD%BF%E7%94%A8pymouse%E5%BA%93%201a40758fde12408d920603cc573047bc/Untitled.png](Python3%208+%E4%BD%BF%E7%94%A8pymouse%E5%BA%93%201a40758fde12408d920603cc573047bc/Untitled.png)
    
2. 此时在运行会产生报错`ModuleNotFoundError：No module named ‘pyHook’`，去官网下载一个PyHook，我使用的是3.8版本python只能使用pywinhook，[下载地址](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pywinhook)（32位还是64位参照自己的系统）
    
    ![Python3%208+%E4%BD%BF%E7%94%A8pymouse%E5%BA%93%201a40758fde12408d920603cc573047bc/Untitled%201.png](Python3%208+%E4%BD%BF%E7%94%A8pymouse%E5%BA%93%201a40758fde12408d920603cc573047bc/Untitled%201.png)
    
3. 下载后的包，使用pip进行安装
    
    ![Python3%208+%E4%BD%BF%E7%94%A8pymouse%E5%BA%93%201a40758fde12408d920603cc573047bc/Untitled%202.png](Python3%208+%E4%BD%BF%E7%94%A8pymouse%E5%BA%93%201a40758fde12408d920603cc573047bc/Untitled%202.png)
    
4. 安装成功后，再编辑python安装目录下lib\site-packages\pymouse\[windows.py](http://windows.py/)"修改第23行
    
    ![Python3%208+%E4%BD%BF%E7%94%A8pymouse%E5%BA%93%201a40758fde12408d920603cc573047bc/Untitled%203.png](Python3%208+%E4%BD%BF%E7%94%A8pymouse%E5%BA%93%201a40758fde12408d920603cc573047bc/Untitled%203.png)
    
5. 测试一下环境是否成功
    
    ```python
    >>> import pymouse
    >>> m = pymouse.PyMouse()
    >>> print(m.position())
    (494, 407)
    ```