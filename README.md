# textarea_add_p
文本域回车 自动添加&lt;p&gt;***&lt;/p&gt;标签
# 函数
&lt;script&gt;<br>
    //用&lt;p&gt;***&lt;/p&gt;标签替换回车<br>
    function ReplaceSeperator(html) {<br>
        var i;<br>
        var result = "&lt;p&gt;";<br>
        var c;<br>
        for (i = 0; i < html.length; i++) {<br>
            c = html.substr(i, 1);<br>
            if (c == "\n")<br>
                result = result + "&lt;/p&gt;&lt;p&gt;";<br>
            else if (c != "\r")<br>
                result = result + c;<br>
        }<br>
        return result;<br>
    }<br>
&lt;/script&gt;
