# sanguosha_py

# 说明篇
脚本主要基于python的pyautogui库，而这个库又依赖pillow，pillow在Windows上似乎又需要Microsoft VS工具支持。

mouse.pyw 这个文件是在写代码的过程中，需要频繁的确定坐标而写的代码，用于开发的时候确定坐标，我的电脑是1920*1080，使用的是chrome浏览器，没有书签模式下(ctrl+shift+b)，运行。

sanguosha.bat 这个文件是放在桌面上双击运行的，双击之后回车，然后就可以喝咖啡看着自动跑了。

------------------------------------------------
# 废话篇
版本在使用过程中修改了很多次，最后修改大概是2020.11月。

修改的初衷是为了使代码更简洁，结果事与愿违。

最初没有选择参数的功能，是后面加的，定时功能也是后面加的，计算每个函数运行的时间只是为了方便观察。

网上有些js脚本，水平有限，直接在控制台跑别人的js脚本没有效果，这才生出想自己写个脚本的念头。

开始是打算用selenium来操作，但是发现，使用selenium操控chrome会被弹出登录界面，无法正常加载，后面试图通过chrome开发者模式启动，人工进入游戏，然后使用selenium接管chrome，结果依旧会被弹出登录界面。

直到遇到了pyautogui这个库，就像是打开了新世界的大门。

本脚本配置麻烦，给自己留个念想了。

-------------------------------------------------------
# 代码篇
datetime threading time 这几个库都是为了定时做的，不需要定时模块可以直接删掉。

pyautogui.FAILSAFE = True 这个是为了防止失控，把鼠标放到电脑左上角，脚本会抛出异常然后终止。

confidence=0.7,这个参数是相似度，如果匹配不到，可以调低一点，0-1。1表示100%匹配。