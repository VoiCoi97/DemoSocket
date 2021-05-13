# DemoSocket

1. https://datafeed.vps.com.vn/pslistdata (lấy danh sách các mã phái sinh)
2. https://datafeed.vps.com.vn/getpsalldatalsnapshot/VN30F2002,VN30F2003,VN30F2006,VN30F2009 (lấy thông tin giá phái sinh)
3. https://datafeed.vps.com.vn/getps10pricesnapshot/VN30F2002,B (lấy thôgn tin 10 giá buy của 1 mã PS)
4. https://datafeed.vps.com.vn/getps10pricesnapshot/VN30F2002,S (lấy thông tin 10 giá bán của 1 mã PS)

 
2. Lấy thông tin socket realtime
1. SocketUrl: https://datafeed.vps.com.vn
2. Namespace: /REALTIME_PS_MOBILE
3. Socket tổng khối lượng: REALTIME_3220_[sym]_SYM_TOTALVOL(trong đó [sym] là mã PS eg: VN30F2009)
4. Socket tổng khối lượng: REALTIME_3220_[sym]_SYM_LASTPRICE
5. Socket 10 giá: stockps10price
 
3. Màn hình login:
> * API URL Login: https://hometrade.vps.com.vn/handler/MBCheckLogin.aspx ,
> - Input ("channel": "H", "user": "dieulinh", "pass": "123456”) => Lấy đc sid
4. Màn landscape bảng giá ps:
> * API snapshot về giá: https://hometrade.vps.com.vn/handler/core.vpbs
> - Input param: {"group":"Q","user":"006385","session":"762a14e5-2b89-47c4-a7c6-8ccca0df5982","c":"H","data":{"type":"string","cmd":"Web.Price.aFutureList","p1":"","p2":"","p3":"","p4":""}}
> * API lấy giá vn30: https://datafeed.vps.com.vn/getlistindexdetail/11
> * Socket giá:
> - REALTIME_3210_(sym)_S_G1_GIA,
> - REALTIME_3210_(sym)_S_G1_KL,
> - REALTIME_3210_(sym)_S_G2_GIA,
> - REALTIME_3210_(sym)_S_G2_KL
> - REALTIME_3210_(sym)_B_G2_GIA
> - REALTIME_3210_(sym)_B_G2_LK
> - REALTIME_3210_(sym)_B_G1_GIA
> - REALTIME_3210_(sym)_B_G1_KL
> - REALTIME_3220_(sym)_SYM_LASTPRICE
> - REALTIME_3220_(sym)_SYM_TOTALVOL
> * Socket VN30: “REALTIME_1101_11_CINDEX"
