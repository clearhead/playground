# Clearhead.me Playground #

### Optiverse Q: Dimensions set through API ###

./optimizely-dimensions/

Q: https://community.optimizely.com/t5/Developers/Dimensions-set-through-API/m-p/10459#M602

Live Site: http://rawgit.com/clearhead/playground/master/optimizely-dimensions/index.html

### Optiverse Q: Redirect Test cause huge spike of new visitors in Google Analytics ###

./referrer-in-redirect/

Q: https://community.optimizely.com/t5/Using-Optimizely/Redirect-Test-cause-huge-spike-of-new-visitors-in-Google/m-p/10652#M3084

Launchpad: ./referrer-in-redirect/dev.sh && ngrok 8000

| Starting | Ending | Link | Resulting Referrer | Carried? |
|----------|--------|------|--------------------|----------|
| http | http | [no redirect](http://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html) | ngrok.com | Yes |
| http | http | [location.replace(v2)](http://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html?location-replace) | /control | No |
| http | http | [location=v2](http://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html?location-equals) | /control | No |
| http | http | [href=v2](http://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html?href-equals) | /control | No |
| http | https | [no redirect](https://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html) | ngrok.com | Yes |
| http | https | [location.replace(v2)](https://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html?location-replace) | /control | No |
| http | https | [location=v2](https://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html?location-equals) | /control | No |
| http | https | [href=v2](https://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html?href-equals) | /control | No |
| https | http | [no redirect](http://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html) | NULL | No |
| https | http | [location.replace(v2)](http://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html?location-replace) | /control | No |
| https | http | [location=v2](http://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html?location-equals) | /control | No |
| https | http | [href=v2](http://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html?href-equals) | /control | No |
| https | https | [no redirect](https://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html) | ngrok.com | Yes |
| https | https | [location.replace(v2)](https://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html?location-replace) | /control | No |
| https | https | [location=v2](https://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html?location-equals) | /control | No |
| https | https | [href=v2](https://rawgit.com/clearhead/playground/master/referrer-in-redirect/index.html?href-equals) | /control | No |
