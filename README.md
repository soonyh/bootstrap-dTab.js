# bootstrap-dTab.js
对bootstrap tab.js的扩展，实现动态添加tab 

##用法

    //html
    <button 
    type="button" 
    class="btn btn-default" 
    data-source="remote1.shtml" 
    data-container="#container" 
    data-toggle="dTab">remote1</button>

    <div id="container"></div>
  
##options

###必写

+ __data-toggle__ 唯一值‘_dTab_’
+ __data-container__ 值是css选择器，表示生成tab的容器，
+ __data-source__ 值只能是2中形式 "#id|url"，表示新增的tab内容

    不带“#”默认为一个url

    加载远程页面的时候，需要在内容加载完毕后手动移除loading图标

    如：$('#tmpl').prevAll('.dTab-loading').remove();

### 选填

 * __data-title__                       标签的显示名称
 * __data-limit__                       不填默认为false,表示允许重复添加; data-limit="true" 表示只能添加1次
 * __data-empty__                       tab-content为空时显示的内容
 * __data-removeable__                  不填默认为false,表示不允许删除；data-removeable="true"添加的tab允许被删除（右上角会出现叉叉）
 * __data-theme__     会在#container的dom元素上加一个class，默认值是dTab-primary

