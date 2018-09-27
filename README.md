#### **Use the test cases created by xmind and freemind to export the xml files that can be imported into [TestLink](https://github.com/TestLinkOpenSourceTRMS/testlink-code).**

The use cases written by xmind should be exported to freemind format files (.mm suffix files).

**Mindmap use case writing requirements:**

 * TestSuite needs to add the relevant icon: Banner (no requirement for color)
 * Step-by-step use cases require the addition of associated icons: Stars (no color required)
 * Summary and description of use cases separated by & (for example: loading an elephant into the refrigerator & having a refrigerator)
 * Step-by-step use cases The description of each step and the desired result are separated by & (for example: ‘click the login button & login successfully’)
 * Use case priority needs to be associated with the icon: 1 2 3 ---> high medium low (the default for other digital icons is medium priority)

For writing examples, refer to Demo.mm or Demo.xmind as a reference

![mind](img/mind.png)

#### **Instructions for use**
- Use cases written by xmind, please export as freemind files
- Copy the freemind file (eg demo.mm) that needs to be converted to the current folder
- Double-click By_flag (Mac: By_flag, Windows: By_flag.exe) and double-click to generate the xml file and logger.log (log file to view the exported related logs)
You can also execute the Freemind.py file, and the related dependencies `lxml`, please download `pip install lxml`.
- Import the generated xml file into Testlink.
- mm file name is best not to have special symbols

  ![testlink](img/testlink.png)

#### **Note**
- When the generated xml file is imported into testlink, the central theme is not set to suite.
Please manually create a test case set in testlink and import the xml into the use case set specified by testlink.
In order to avoid confusion with the original test cases, management confusion (you can also add the flag icon directly on the top layer, so that the export to testlink is in a folder)
- After executing the exe, all the .mm files in the folder will be converted to generate xml. To avoid running errors, please try to keep only one mm file under the folder.

#### **Generate exe file**
Use `Pyinstaller` to package, `pip install pyinstaller` after installation, go to this folder and execute `pyinstaller -F Freemind.py`.
A separate exe file will be generated in the generated dist folder. Like the Mac, you need to modify one line of code.
