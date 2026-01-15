# bang-dream-website-fixer/BanG Dream官网图片修复
This user script fixes broken image URLs on the BanG Dream official website by replacing invalid AWS S3 endpoints with valid ones, ensuring images load correctly.  
修复BanG Dream官网图片加载问题的油猴脚本，自动将失效的AWS S3端点替换为有效端点。  


# BanG Dream官网图片修复
一个用于修复 BanG Dream 官网图片无法加载问题的用户脚本。该脚本通过自动替换失效的 AWS S3 端点，恢复官网图片、样式等资源的正常加载。  

# 问题背景
BanG Dream 官方网站（bang-dream.com）的部分资源托管在 AWS S3 上，但由于历史原因，网站代码中仍使用已失效的旧版 S3 端点：   
s3-ap-northeast-1.amazonaws.com   
该端点在部分国家和地区已经停用，已无法正常访问，导致官网图片、样式等资源加载失败，影响用户体验。   

本脚本将自动检测并替换为当前可用的有效端点：   
s3.ap-northeast-1.amazonaws.com   
并修改url为正确的请求格式。   

# 功能特性
自动修复：实时检测并修复页面中的失效 S3 资源 URL   
全面覆盖：支持图片、样式表、脚本等多种资源类型   
动态处理：使用 MutationObserver 监控 DOM 变化，修复动态加载的内容   
网络拦截：拦截并修复 XMLHttpRequest 和 Fetch API 请求中的失效 URL   
错误恢复：自动重载修复后仍加载失败的资源   

# 安装浏览器拓展
首先需要安装用户脚本管理器：  
Tampermonkey（推荐）：Chrome | Firefox  
Violentmonkey：Chrome | Firefox  

# 安装脚本
进入Greasy Fork 搜索打开“BanG Dream官网图片修复”   
点击"安装此脚本"按钮   
在用户脚本管理器的安装确认页面点击"安装"   
或者，您也可以手动创建新脚本，将本项目的完整代码复制粘贴到编辑器中。   

# 使用方法
正确配置脚本管理器浏览器拓展后，脚本会自动运行。当匹配到您访问邦邦官网时，脚本会自动生效.  
