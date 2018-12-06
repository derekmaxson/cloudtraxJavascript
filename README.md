# cloudtraxJavascript
CloudTrax Captive Portal Functions For Node.js 

We did not wish to use PHP for captive portal functions in CloudTrax.  So, we ported the password encrypt/sign functions necessary for captive portal to javascript.

CloudTrax captive portal documentation: https://help.cloudtrax.com/hc/en-us/articles/205014660-Externally-Hosted-Splash-Page-with-RADIUS-Authentication

We use express.js to serve a web response.  In this response, the username is the MAC and the password is 'password.'  You can change these values or build a web form to pass them, etc.

A sample request from CloudTrax: http://localhost:8088/captiveCloudTrax?res=notyet&uamip=1.1.1.1&uamport=8081&mac=AA-BB-CC-75-3B-CD&cip=192.168.13.10&called=55-86-74-BA-A6-15&ssid=CloudTraxGuest&nasid=9000&userurl=http%3A%2F%2Fcaptive.apple.com%2Fhotspot-detect.html&challenge=440EF96DB9A2225C32E031659DF2608B49932F0D8AFAC46F74FA56FF3E1AE952

