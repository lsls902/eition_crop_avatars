# eition_avatars 头像图片截取小工具

## 孔子云：“代码写太多，难免bug多”。 所以本代码功能很简单，mini只有2.58kb

简易 web上传头像裁剪原生js小插件,支持移动端。

主要用到h5的canvas,在本地截图好后，返回base64图片字符串。你可以在服务端生成图片，或直接数据库中存这个字符串。用的时候就：&lt;img src='base64字符串'&gt;

具体用法在index.html中就可查看

CSS
<pre>
  <style>
  .eitionCss{background:#f9f9f9;position: relative;background-repeat: no-repeat;background-size: 100%;background-position-x: 50%;background-position-y: 0;}
  .drag{background:#ffffff;border:1px solid #000;opacity: 0.4;position: absolute}
  </style>
</pre>

HTML

<pre>
  &lt;div id="eition"&gt;&lt;/div&gt;
  &lt;input type="file" name="file" id="imgFile" onchange="_eition.openFile(this)" /&gt;
  &lt;input type="button" value="保存" name="save" id="save" onclick="save()" /&gt;

  &lt;img id="thumb"&gt;
</pre>

Javascript
<pre>
<script src="eition.avatars.1.1.mini.js"></script>
  <script>
        _eition.el="eition";
        _eition.width=400;//操作面的宽度
        _eition.height=400;//操作面的高度
        _eition._width=100;//截图框的宽度
        _eition._height=100;//截图框的高度
        _eition.thumbEl="thumb";//是否显示缩略图。样式自己写吧
        _eition.start();
        function save(){
            alert(_eition.result());
        }
    </script>
</pre>
