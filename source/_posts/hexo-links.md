---
title: 创建友情链接
date: 2019-05-11 12:09:01
categories: 
- hexo
---
 ##### source 下建立 _data 目录
 
 创建links.yml文件
 ```
 xiaoxiao's Blog: http://xiaoyun.farbox.com
 说说事: http://www.saysays.com
 ```
 ##### 主题文件夹下 
    _widget文件夹 创建links.ejs文件
      ```
      <% if (site.data.links){ %>
        <div class="widget tag">
          <h3 class="title">友情链接</h3>
            <ul class="entry">
              <% for (var i in site.data.links){ %>
                <li class='link'><a href='<%- site.data.links[i] %>'><%= i %></a></li>
              <% } %>
            </ul>
        </div>
      <% } %>
      ```
  配置_config.yml
   ```
    widgets:
    ...
    - links
   ```
  
 