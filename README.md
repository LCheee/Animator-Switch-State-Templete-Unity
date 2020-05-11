# Animator-Switch-State-Templete-Unity-
Unity UI动画通过布尔变量来转换状态机的模板
(通过布尔变量来转换状态机的模板)
# 适用状态机的基本模式：
![例如点一下弹出托盘，再点一下托盘收回的事件](https://img-blog.csdnimg.cn/2020051119474452.png)

点一下弹出托盘，再点一下托盘收回的事件

状态机说明：其中ButtomPanel为收回状态，bool 变量 “press”为 true 的时候通过ButtomPanel2（即托盘弹出动画），ButtomPanel3为弹出状态，bool 变量 “press”为 false 的时候通过ButtomPanel4（即托盘收回动画）回到初始状态。
其中2→3，4→1之间不设置通过条件。

# 使用方法：
1. 为UI控件做状态机动画如上图，新建Bool变量作为控制条件。（此处我的Bool变量变量名为“Press”）

2. 将脚本挂在含有动画的UI控件上（即有组件Animator的UI控件上）
![其中"Parameter_name"即为需要进行往复改变的Bool 变量名称](https://img-blog.csdnimg.cn/20200511195736621.png)

3. 在脚本中“Parameter_name"处填入需要进行往复改变的Bool 变量名称

4. 建立一个Button，通过点击触发事件

![建立一个Button，通过点击触发事件](https://img-blog.csdnimg.cn/20200511200502193.png)
OnClick中前面填入含有”Animator”组件的动画根文件，后面选择UIPanel.AddCount。
