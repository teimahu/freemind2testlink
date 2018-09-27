Use the test cases created by xmind and freemind to export the xml files that can be imported into testlink. The use cases written by xmind should be exported to freemind format files (.mm suffix files).
Xmind use case writing requirements:

 * TestSuite needs to add the relevant icon: Banner (no requirement for color)
 * Step-by-step use cases require the addition of associated icons: Stars (no color required)
 * Summary and description of use cases separated by & (for example: loading an elephant into the refrigerator & having a refrigerator)
 * Step-by-step use cases The description of each step and the desired result are separated by & (for example: ‘click the login button & login successfully’)
 * Use case priority needs to be associated with the icon: 1 2 3 ---> high medium low (the default for other digital icons is medium priority)

Specific writing can refer to Demo.mm, Demo.xmind as a reference

![mind](img/mind.png)

#### **使用说明**
- xmind编写的用例请导出为freemind文件

- 将需要转换的freemind文件(例如demo.mm) 复制到当前文件夹

- 双击By_flag(Mac：By_flag、Windows：By_flag.exe),双击即可生成xml文件和logger.log（log文件可查看导出的相关日志）
也可以执行Freemind.py文件，相关的依赖库`lxml`请自行下载`pip install lxml`

- 将生成的xml文件导入到Testlink就好啦

- mm文件的文件名最好不要出现特殊符号

  ![testlink](img/testlink.png)

#### **注意：**

- 生成的xml文件在导入testlink时，中心主题没有设定为suite的，请在testlink中手动创建一个测试用例集，将xml导入到testlink指定的用例集下。以免和原有的测试用例混淆造成管理混乱 （也可以直接在顶层加上旗帜图标，这样导出到testlink就是在一个文件夹下了）
- 执行exe后会将文件夹下所有的.mm文件全部执行转换生成xml，为避免造成运行错误，请尽量保持文件夹下只有一个mm文件。

#### **生成exe文件：**
使用`Pyinstaller`进行打包，`pip install pyinstaller`安装好之后，到该文件夹下，执行`pyinstaller -F Freemind.py`.
在生成的dist文件夹下就会生成一个独立的exe文件了。Mac下一样，需要修改一行代码。
