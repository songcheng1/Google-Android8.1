1. 前言
Nexus 6P刷入Google Android8.1镜像后，WIFI提示"已连接，但无法访问互联网"。

2. 解决方法
进入adb shell后，输入以下命令：

settings put global captive_portal_detection_enabled 1
settings put global captive_portal_mode 1
settings put global captive_portal_use_https 0
settings put global captive_portal_server connect.rom.miui.com
settings put global captive_portal_http_url http://connect.rom.miui.com/generate_204
settings put global captive_portal_https_url https://connect.rom.miui.com/generate_204




输入完后，切换飞行模式（或者重启手机）生效。

3. 其它
注意，目前只在Android8.1镜像上调试过，其它镜像未作尝试。
