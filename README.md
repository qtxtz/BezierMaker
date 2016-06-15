# BezierMaker
通过de Casteljau算法绘制贝塞尔曲线，并计算它的切线，实现1-7阶贝塞尔曲线的形成动画。

Features
--
* 支持增加和删除控制点
* 支持1阶到7阶贝塞尔曲线，限于屏幕大小，理论上可以支持N阶贝塞尔曲线
* 支持自由移动控制点
* 支持显示贝塞尔曲线形成过程的切线
* 支持循环显示贝塞尔曲线的形成动画
* 支持贝塞尔曲线显示速率
* 支持显示控制点坐标

ScreenShot
--
![](http://o8tfd4klp.bkt.clouddn.com/image/beziermaker/1.gif)
<br/>
![](http://o8tfd4klp.bkt.clouddn.com/image/beziermaker/2.gif)
<br/>
![](http://o8tfd4klp.bkt.clouddn.com/image/beziermaker/3.gif)
<br/>
![](http://o8tfd4klp.bkt.clouddn.com/image/beziermaker/4.gif)
<br/>
![](http://o8tfd4klp.bkt.clouddn.com/image/beziermaker/5.gif)
<br/>
![](http://o8tfd4klp.bkt.clouddn.com/image/beziermaker/6.gif)
<br/>
![](http://o8tfd4klp.bkt.clouddn.com/image/beziermaker/7.gif)
<br/>
![](http://o8tfd4klp.bkt.clouddn.com/image/beziermaker/8.gif)
<br/>

Demo
--

##### Java:
```Java
    public class MainActivity extends Activity {

        BezierView mBezierView

        @Override
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_main)

            mBezierView = (BezierView) findViewById(R.id.bezier);
        }

        public void start(View view) {
            mBezierView.start();
        }

        public void stop(View view) {
            mBezierView.stop();
        }

        public void add(View view) {
            mBezierView.addPoint();
        }

        public void del(View view) {
            mBezierView.delPoint();
        }

    }
```

##### Methods:
| method 方法          | description 描述 |
|:---				 |:---|
| void **start**()  	     | 开始贝塞尔曲线（required） |
| void **stop**()	     | 停止贝塞尔曲线（optional） |
| boolean **addPoint**() 	     | 增加控制点（optional） |
| boolean **delPoint**() 	     | 删除控制点（optional） |
| int **getOrder**() 	     | 获取贝塞尔曲线阶数（optional） |
| void **setRate**(int rate) 	     | 设置移动速率（optional） |
| void **setTangent**(boolean tangent)  	     | 设置是否显示切线（optional） |
| void **setLoop**(boolean loop)  	     | 设置是否循环（optional） |


About
--
* Email：venshine.cn@gmail.com

License
--
    Copyright (C) 2016 venshine.cn@gmail.com

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
