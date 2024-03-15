# 这是一个前端的笔记，都是跟着教程敲的
##01播放暂停
播放暂停，练习选择器
~~~
document.querySelector('button:nth-child(3)').onclick=function(){
            document.querySelector('video').pause();
        }
~~~
##02简单的视频控制网页
css样式里注意position的变化，script里注意document.querySelector() ，跟01不同的地方是var声明元素，之后再用来做函数，有点像java。.onclick等是事件，动作发生的意思。
```
//播放时切换图标
var video = document.querySelector('video');
playBtn.onclick = function () {
            if (video.paused) {
                video.play();
                //切换图标
                this.classList.remove('icon-play');
                this.classList.add('icon-pause');
            } else {
                video.pause();
                this.classList.remove('icon-pause');
                this.classList.add('icon-play');
            }
        }
```
