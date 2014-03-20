# js模拟HTML5表单placeholder属性
2013-07-28 15:24:55


HTML5对表单输入框`<input/>`新增了一些表单验证规则属性，包括placeholder：

    <input type="text" placeholder="请输入关键字" />

效果：

<input type="text" placeholder="请输入关键字" />

IE8及其更低版本的IE浏览器不支持HTML5,自然也不支持这一属性，可以用js来模拟这种交互效果

    <input type="text" value="请输入关键字" onfocus="this.value=''" onblur="if(!value){value=defaultValue;}" />

效果：

<input type="text" value="请输入关键字" onfocus="this.value=''" onblur="if(!value){value=defaultValue;}" />
或者使用以下jQuery插件：

    // jQuery code
    var i = document.createElement("input");
    // Only bind if placeholder isn't natively supported by the browser
    if (!("placeholder" in i)) {
       $("input[placeholder]").each(function () {
       var self = $(this);
       self.val(self.attr("placeholder")).bind({
         focus: function () {
         if (self.val() === self.attr("placeholder")) {
         self.val("");
         }
       },
       blur: function () {
         var label = self.attr("placeholder");
         if (label &amp;&amp; self.val() === "") {
         self.val(label);
         }
         }
       });
     });
    }
    
    <!-- html5 -->
    
    <input type="text" name="search" placeholder="Search" value="">