# 本地部署之前可以体验开源视频会议公共的服务器demo

# demo:
1. janus-geteway
https://janus.conf.meetecho.com/

2. mediasoup
https://v3demo.mediasoup.org

3. bigbluebutton
http://demo.bigbluebutton.org/

4. openmeetings
http://openmeetings.apache.org/demo.html

# 本地demo
1. freeswitch
https://8.134.56.226/sipml5/call.htm

2. janus-geteway
https://8.134.56.226/demos/

# 经过一周的调研
freeswitch janus-geteway mediasoup 从安装，配置到二次开发都比较容易.
bigbluebutton安装及其繁琐. 
openmeetings安装配置较容易，是java生态的.

# sip接入webrtc服务器
验证了freeswitch和janus-geteway
linphone, zoiper和webrtc视频不能互通，音频倒是能通. 
linphone接入不了webrtc视频会议，zoiper可以接入webrtc视频会议.