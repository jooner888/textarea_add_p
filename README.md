# textarea_add_p
文本域回车 自动添加&lt;p&gt;***&lt;/p&gt;标签
# 函数
&lt;script&gt;
    //用<p></p>标签替换回车
    function ReplaceSeperator(html) {
        var i;
        var result = "<p>";
        var c;
        for (i = 0; i < html.length; i++) {
            c = html.substr(i, 1);
            if (c == "\n")
                result = result + "</p><p>";
            else if (c != "\r")
                result = result + c;
        }
        return result;
    }
&lt;/script&gt;
