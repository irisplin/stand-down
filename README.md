## How to verify if Cashback/Login Notifier stands down properly
1. install Chrome extension [Redirect Path](https://chrome.google.com/webstore/detail/redirect-path/aomidfkchockcldhbkggjokdkkebmdll?hl=en) or Firefox addon [Link Redirect Trace](https://addons.mozilla.org/en-US/firefox/addon/link-redirect-trace-addon/) 
2. log in to the market where you would like to test stand-down 
3. click the links gathered from other publishers (couponation, quantas, etc.,) Some of them require account registration/sign-up. Usually publishers' tracking links would be cloaked or hidden from end users. Nonetheless, Cashback Notifer should also stand down if tracking links are clicked directly.  
4. use Redirect Path/Link Redirect Trace to check url redirects. 
5. when redirects contain stand-down rules, Cashback Notifier should stand down


## Stand-down test cases


### affiliate network
Notifiers will stand down if user is redirected from a link that belongs to an affiliate network that has requested us to stand down
#### linksynergy 
SG: redirect from [couponation](https://www.cuponation.com.sg/api/seo/redirect?cid=be18fa962bb4793b33a42c970afdca7b&url=dyson-coupon) to [linksynergy](https://click.linksynergy.com/deeplink?id=xGCTEDxXvh0&mid=47231&u1=A2ASUBID&murl=https%3A%2F%2Fwww.dyson.com.sg%2F?utm_content=cuponation) to [dyson](https://www.dyson.com.sg/)
<br>
SG: redirect from [milkadeal](https://www.milkadeal.sg/stores/shop/48) to [linksynergy](https://click.linksynergy.com/deeplink?id=KtlS/wRigh4&mid=41134&u1=MDDTSG15982&murl=https%3A%2F%2Fwww.nike.com%2Fsg%2Fen_gb%2F) to [nike](https://www.nike.com/sg/)
<br>
TW: redirect from [rewardpay](https://tk.rewardpay.com/?M=129078&U=39150&UT=1&AID=2&APID=1&AC=RP) to [linksynergy](https://click.linksynergy.com/deeplink?id=pITOEqOhvpQ&mid=40584&u1=220809176f4427441e9547&subid=1260439&murl=https%3A%2F%2Fwww.yoox.com%2Ftw%2Fwomen) to [yoox](https://www.yoox.com/tw)
<br>
AU: redirect from [quantas](https://shopping.qantas.com/shop?id=petbarn) to [linksynergy](https://click.linksynergy.com/fs-bin/click?id=/yGfdSU4Hew&offerid=502078.5&type=3&subid=0&u1=t625284142m) to [petbarn](https://www.petbarn.com.au/)
<br>
AU: redirect from [kickback](https://kickback.com.au/conversion/merchants/bonds/redirect/) to [linksynergy](https://click.linksynergy.com/deeplink?id=Yi8K9xa1WDE&mid=38921&murl=https%3A%2F%2Fwww.bonds.com.au%2F&u1=5893b28d-b447-4833-ad67-caea7942998b) to [bonds](https://www.bonds.com.au/)
<br>
AU: redirect from [linksynergy](https://click.linksynergy.com/fs-bin/click?id=/yGfdSU4Hew&offerid=558742.936&type=3&subid=0&u1=t625285583m) to [cottonon](https://cottonon.com/AU/)
#### affiliate(.api).rakuten.com
TW: redirect from [affiliate.api.rakuten.com](https://affiliate.api.rakuten.com.tw/redirect?nw=tw&site=afl&ar=1a0d8dccecb7dbb3e661d9ea76b24b5b3cc271130acbc8f83d8fecbdc9eefc6a9951df4322d2499b&pr=63b55d598d8c4861&ap=pr%3D63b55d598d8c4861&e=1&url=https%3A%2F%2Fwww.rakuten.com.tw%2Fshop%2Ffamily2%2Fproduct%2Fbncqwo57x%2F%3Fgid%3Da3748643a8bed24ab8750649a573e1dc%26scid%3Drafp-i001_%26) to [rakuten](https://www.rakuten.com.tw/)
<br>
TW: redirect from [biggo](https://biggo.com.tw/r/?i=tw_pmall_rakuten&id=biggo&purl=https%3A%2F%2Fwww.rakuten.com.tw&lb=index_storepage) to [affiliate.api.rakuten.com](https://affiliate.api.rakuten.com.tw/redirect?nw=tw&site=afl&ar=93cc11a5693c26fa8bc7c54f01b8f9e3b601e7027df43efb93000e3163fa586b1e4de7702a475dff&pr=420457e88ecc9146&ap=pr%3D420457e88ecc9146&e=1&url=https%3A%2F%2Fwww.rakuten.com.tw%3Fscid%3Drafp-b118%26utm_source%3Dbiggo%26utm_medium%3Drafp-b118%26utm_campaign%3Dnormal%26gid%3Dbiggo) to [rakuten](https://www.rakuten.com.tw/)


### query string
Notifier will stand down if user is redirected from a link that has a specific query string. The afsrc=1 is an industry-recognized parameter that was created by the major affiliate networks to prevent software publishers from overwriting another publisher's link.
<br>
<br>
TW: redirect from [findprice](https://www.findprice.com.tw/go/gxrx3nzr/?s=0&t=1&afsrc=1) to [pcone](https://www.pcone.com.tw/)
<br>
SG: redirect from [picodi](https://metric.picodi.com/sg/r/89733?afsrc=1) to [amazon](https://www.amazon.sg/)
<br>
AU: redirect from [couponation](https://www.cuponation.com.au/api/seo/redirect?cid=86cf42151e0a90832203bad4da33fd6d&url=target-coupons&afsrc=1) to [target](https://www.target.com.au/)
<br>
target.au belongs to Partnerize affiliate network, not Rakuten Advertising affiliate network. This test case is to test if extension would honour redirect link with afsrc=1 url parameter and successfully stands down even if the merchant belongs to other affiliate network.
