# webrtc-list

What is a WebRTC Gateway anyway? (Lorenzo Miniero)  
https://webrtchacks.com/webrtc-gw/

examples:

https://bigbluebutton.org/

https://github.com/lynckia/licode

https://github.com/meetecho/janus-gateway

https://github.com/mozilla/janus-plugin-sfu

https://mediasoup.org/

https://github.com/jitsi/jitsi-meet

https://github.com/nextcloud/spreed

https://www.kamailio.org/w/

http://www.easyrtc.com/


snap:

https://snapcraft.io/janus-gateway

https://snapcraft.io/janus-gateway-alpersoft

https://snapcraft.io/rtsp-to-webrtsp

https://snapcraft.io/spreed-webrtc-snap

https://snapcraft.io/webrtc-streamer

https://snapcraft.io/camus

https://snapcraft.io/spreedme

https://snapcraft.io/kamailio-dev

https://snapcraft.io/zoom-client


# demo
本地部署之前可以体验开源视频会议公共的服务器demo  
公共服务器demo:  
1. janus-geteway  
https://janus.conf.meetecho.com/

2. mediasoup  
https://v3demo.mediasoup.org

3. licode  
https://qdt-licode.tk:3004/  

4. bigbluebutton  
http://demo.bigbluebutton.org/

5. openmeetings  
http://openmeetings.apache.org/demo.html

本地服务器demo:  
1. freeswitch  
https://8.134.56.226/sipml5/call.htm

2. janus-geteway  
https://8.134.56.226/demos/

经过一周的调研  
freeswitch janus-geteway mediasoup licode从安装，配置到二次开发都相对比较容易.  
bigbluebutton安装及其繁琐.   
openmeetings安装配置较容易，是java生态的.  

sip接入webrtc服务器  
验证了freeswitch和janus-geteway  
linphone, zoiper和webrtc视频不能互通，音频倒是能通.   
linphone接入不了webrtc视频会议，zoiper可以接入webrtc视频会议.  

# reference
1. freeswitch  
https://freeswitch.org/confluence/display/FREESWITCH/Debian+9+Stretch  
debian下按官方wiki安装1.10.x版本即可支持视频，默认配置基本可以使用，无需繁琐的自定义配置  

2. janus-gateway  
https://ourcodeworld.com/articles/read/1197/how-to-install-janus-gateway-in-ubuntu-server-18-04  
https://gitee.com/dong2/janus-gateway/blob/master/README.md  
注意libwebsockets 不能git checkout v2.4-stable，这个版本加载不了libwebsockets.so，用4.x是正常的.  
注意rabbitmq-c仓库submodule update失败，直接跳过  
注意libnice版本(at least v0.1.16 suggested, master recommended)  

3. mediasoup  
据说阿里，头条都在用这个，不过我不想折腾nodejs，优先c/c++生态.  
https://blog.csdn.net/gupar/article/details/83788934  

4. licode  
https://lynckia.com/licode/install.html

5. OpenMeetings  
https://cwiki.apache.org/confluence/display/OPENMEETINGS/Tutorials+for+installing+OpenMeetings+and+Tools  
Manuale Installazione OpenMeetings 2.x.x - 3.x.x Linux Italiano.pdf  

6. webrtc2sip  
https://github.com/dong2/2webrtc2sip  

7. WEBRTC-to-SIP  
https://github.com/havfo/WEBRTC-to-SIP  

8. MRTC  
https://www.mizu-voip.com/Software/WebRTCtoSIP.aspx  


