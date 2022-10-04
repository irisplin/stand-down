## How to verify if Cashback/Login Notifier stands down properly
1. install Chrome extension [Redirect Path](https://chrome.google.com/webstore/detail/redirect-path/aomidfkchockcldhbkggjokdkkebmdll?hl=en) or Firefox addon [Link Redirect Trace](https://addons.mozilla.org/en-US/firefox/addon/link-redirect-trace-addon/) 
2. log in to the market where you would like to test stand-down 
3. click the links gathered from other publishers (couponation, quantas, etc.,) Some of them require account registration/sign-up. Usually publishers' tracking links would be cloaked or hidden from end users. Nonetheless, Cashback Notifer should also stand down if tracking links are clicked directly.  
4. use Redirect Path/Link Redirect Trace to check url redirects. 
5. when redirects contain stand-down rules, Cashback Notifier should stand down

## Notes
Once extension stands down, Cashback Notifier will stand down for 24 hours. For testing purposes, can "reload" extension to reset the stand down effect.

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

#### affiliate(.api).rakuten.com
TW: redirect from [affiliate.api.rakuten.com](https://affiliate.api.rakuten.com.tw/redirect?nw=tw&site=afl&ar=1a0d8dccecb7dbb3e661d9ea76b24b5b3cc271130acbc8f83d8fecbdc9eefc6a9951df4322d2499b&pr=63b55d598d8c4861&ap=pr%3D63b55d598d8c4861&e=1&url=https%3A%2F%2Fwww.rakuten.com.tw%2Fshop%2Ffamily2%2Fproduct%2Fbncqwo57x%2F%3Fgid%3Da3748643a8bed24ab8750649a573e1dc%26scid%3Drafp-i001_%26) to [rakuten](https://www.rakuten.com.tw/)
<br>
TW: redirect from [biggo](https://biggo.com.tw/r/?i=tw_pmall_rakuten&id=biggo&purl=https%3A%2F%2Fwww.rakuten.com.tw&lb=index_storepage) to [affiliate.api.rakuten.com](https://affiliate.api.rakuten.com.tw/redirect?nw=tw&site=afl&ar=93cc11a5693c26fa8bc7c54f01b8f9e3b601e7027df43efb93000e3163fa586b1e4de7702a475dff&pr=420457e88ecc9146&ap=pr%3D420457e88ecc9146&e=1&url=https%3A%2F%2Fwww.rakuten.com.tw%3Fscid%3Drafp-b118%26utm_source%3Dbiggo%26utm_medium%3Drafp-b118%26utm_campaign%3Dnormal%26gid%3Dbiggo) to [rakuten](https://www.rakuten.com.tw/)
<br>
#### cjdomain
SG: redirect from [Love Coupons](https://www.lovecoupons.com.sg/overstockcom) to [cjdomain-jdoqocy](https://www.jdoqocy.com/click-100001035-11557584?url=https%3A%2F%2Fwww.overstock.com%2F&sid=LCSG_B7500_S3_D1_CID36287402) to [cjdomain-cj.dotomi](https://cj.dotomi.com/e9116lnwvD/nuz/CCGGIGJF/CBBBBCBEG/B/B/B?p=yI83%3Dlcsg_bXVQQ_sS_dR_cidTWXTZSTT%26KHB%3D7JJFI%25Ta%25Sf%25SfMMM.EL4HIJE2A.2EC%25Sf%3c%3c7JJFI%3A%2F%2FMMM.93EGE2O.2EC%2F2B82A-RQQQQRQTV-RRVVXVYU%3c%3cg%3c7JJFI%3A%2F%2FMMM.BEL42EKFEDI.2EC.I6%2F%3c%3cR%3cR%3cQ%3cQ%3cQ%3c) to [cjdomain-emjcd](https://www.emjcd.com/h9115vpyxH/pw0/EEIIKILH/EDDDDEDGI/D/HDDMDHLIMKDFKMJJHJ:rkrAdRP1Q8Tc/oMpHKFFqHGsEEErqLDFqMGnLDnELDIEF?g=f9zu%3DcTjX_SOMHH_jK_UI_TZUKNJPOLHJ%26B82%3DyAA69%25KR%25JW%25JWDDD.5Cv89A5t1.t53%25JW%3ct05!Dvwy-r0OrFMQ-Eu3B-ArPQs6sN-Et34-A2Bu3ACr-EvBL-ArPEL1y0-EutP-CvAL0Cw-DP3v-2uDDIJE-EvBK-GsHO276-DGBB-DNrttNF-D8y2-CvLFM5Q-D8D3-uLPuQxr-EyOM-CvLFJJB-Du26-47NQKys%3cyAA69%3A%2F%2FDDD.0u575tF.t53%2Ft2zt1-IHHHHIHKM-IIMMOMPL%3c%3cX%3cyAA69%3A%2F%2FxzAyBs.t53%2Fz8z962z4%2F9Ar4u-u5D4%2Fs25s%2Fxy-6rxv9%2FiVRUdV.3u%3cJPPNMOtP-OJuH-LJNw-rtON-OJsuOKHOvJKJ%3cI%3cI%3cH%3cH%3cH%3c) to [overstock](https://www.overstock.com/)
<br>
SG: redirect from [cuponation](https://www.cuponation.com.sg/dell-coupon) to [cjdomain-anrdoezrs](https://www.anrdoezrs.net/click-7915643-14512692?sid=A2ASUBID&url=https%3A%2F%2Fwww.dell.com%2Fen-sg) to [dell](https://www.dell.com/en-sg)
<br>
SG: redirect from [hardwarezone](https://coupons.hardwarezone.com.sg/dell-coupon) to [cjdomain-cj.dotomi](https://cj.dotomi.com/hc103shqp7/hot/69A67BE7/CE6AB98/5/5/5?j=oD3y%3DVNVnpWdY%26FC6%3D2EEAD%25OV%25Na%25NaHHH.yz66.x97%25Naz8-D1%3c%3c2EEAD%3A%2F%2FHHH.v8Cy9zKCD.8zE%2Fx63x5-SUMQRPO-MPQMNRUN%3c%3cb%3c2EEAD%3A%2F%2Fx9FA98D.2vCyHvCzK98z.x97.D1%2Fyz66-x9FA98%3c%3cM%3cM%3cL%3cL%3cL%3c) to [dell](https://www.dell.com/en-sg)
<br>
TW: redirect from [Line](https://buy.line.me/u/partner/880047416611) to [cjdomain-emjcd](https://www.emjcd.com/links-i/?d=eyJzdXJmZXIiOiI0MDA4MDQ4NTgxOTMyNjAwMjY6TEZfa0wwQ29ENXBOIiwibGFzdENsaWNrTmFtZSI6IkxDTEsiLCJsYXN0Q2xpY2tWYWx1ZSI6ImNqbyF3ZGxwLWFqbmxrdTctd2VmaC10bHVqdzlxci14ZG11LXlnZ3A5bGgiLCJkZXN0aW5hdGlvblVybCI6Imh0dHBzOi8vd3d3Lmx1aXNhdmlhcm9tYS5jb20vIiwic2lkIjoiMTAwNTMxNDAwODc5MyIsInR5cGUiOiJkbGciLCJwaWQiOjEwMDEyMDU3NSwiZXZlbnRJZCI6ImZmYWNkMWFiM2UwNzExZWQ4MTc5ZTZlNzBhMTgwNTEyIiwiY2pTZXNzaW9uIjoiNjU5M2I4NTEtZDNmZi00Yjk0LTkxY2EtMWI3MmU1NmQ4YjFmIiwibG95YWx0eUV4cGlyYXRpb24iOjAsInJlZGlyZWN0ZWRUb0xpdmVyYW1wIjpmYWxzZSwiY2pDb25zZW50RW51bSI6Ik5FVkVSX0FTS0VEIn0%3D
) to [Luisaviaroma](https://www.luisaviaroma.com/en-tw/)

### query string
#### afsrc=1
Notifier will stand down if user is redirected from a link that has a specific query string. The afsrc=1 is an industry-recognized parameter that was created by the major affiliate networks to prevent software publishers from overwriting another publisher's link.
<br>
<br>
TW: redirect from [findprice](https://www.findprice.com.tw/go/gybqjb4i/?s=0&t=1&afsrc=1) to [friday](https://shopping.friday.tw/)
<br>
遠傳friday購物doesn't belong to any affiliate network. This test case is to verify whether extension would stand down for a tracking link that includes the specified query string.
<br>
<br>
AU: redirect from [honey](https://o.honey.io/store/89864159313478712/offer_claim?afsrc=1&src=honey-web¶m0=8703342671131122374&af0=1662446734556&af8=StoreFrontPageV3) to [petbarn](https://www.petbarn.com.au/)
<br>
petbarn belongs to Rakuten Advertising affiliate network. If SB Button is able to identify affiliate network's tracking link pattern (e.g., linksynergy), extension should stand down successfully even if the shortened or cloaked tracking link doesn't include afsrc=1. Nonetheless, this test case is to verify whether extension would stand down when a redirect link deliberately inlcudes the specified query string. The link is gathered from https://www.joinhoney.com/shop/petbarn-au
<br>
<br>
AU: redirect from [couponation](https://www.cuponation.com.au/api/seo/redirect?cid=86cf42151e0a90832203bad4da33fd6d&url=target-coupons&afsrc=1) to [target](https://www.target.com.au/)
<br>
target.au belongs to Partnerize affiliate network, not Rakuten Advertising affiliate network. This test case is to test if extension would honour tracking link with afsrc=1 url parameter and successfully stands down even if the merchant belongs to other affiliate network.
#### cjevent
SG: redirect to [dell](https://www.dell.com/en-sg) via a link with [cjevent parameter](https://www.dell.com/en-sg?cjevent=b51af5a43e0511ed8179e6e60a180512&dgc=CJ&publisherid=4622663&publisher=&cjdata=MXxOfDB8WXww&gacd=9654672-23751073-5750457-267343041-128522248&dgc=af&dclid=CKbSiJvss_oCFftfDwIdiQYJyw) 
<br>

