**********************************************************************************
*** Danh Sách Lệnh cài đặt tools xmrigcc miner để đào tất cả các coin chạy cpu ***
**********************************************************************************
*** Các lệnh phụ trợ tham khảo:

	rm -f [Tên File Cần Xóa]

	rm -r [Tên Thư Mục Cần Xóa]

	mrdir [Tên Thư Mục Cần Tạo]

	mv [Tên File Muốn Đổi] [Tên File Mới]


**********************************************************************************
0- Lệnh Cấp Quyền Admin

	sudo su

1- Tập lệnh hệ thống update:

	apt-get update -y 
	apt-get upgrade -y
	apt-get install wget 
	apt-get install get 
	apt-get install nano
	apt-get install git -y
	apt-get install git -y

2- Tải và cài đặt ứng dụng astrominer miner để khai thác coin:

	git clone https://github.com/ThienThanh217/tdero.git
	cd tdero
	chmod +x rpc_mining.sh 
	chmod u+x astrominer

3- Lênh Khai thác coin miner:

3.1- Giải thích các thông số trước khi chạy lệnh khai thác:

	-w <địa chỉ ví dero của bạn> 
	-m <số CPU cần đào> 
	-r <địa chỉ pool đào>
	-p <giao thức kết nối đào stratum hay rpc> mặc định là rpc
	-h	show this message
	-r	pool url (required)
	-r1	failover pool url 1 (optional)
	-r2	failover pool url 2 (optional)
	-w	your wallet (required)
	-p	pool type. stratum or RPC (optional, default: rpc)
	-m	mining threads (default: all threads)
	-i	intensive level (valid values [0,10] (optional, default: 10))
	-k	kernel number (-1(auto select), 1(intel) or 2(amd and others)
	-ft	fine tune kernel (-1(auto select), 1(low, mid-end CPUs) or 2(high-end CPUs))
	-a	cpu affinity (linux only): specify cpu IDs to bind to, separated by commas without space, 
 		example( -a 0,2,4,6,8,10 ) | the number of cpu IDs must be equal to the number of mining threads 
   		| use -1 to disable cpu affinity | (default affinity: 0,1,2,3,...,N) 
	-show-latency	show the latency between miner and pool (doesn't work with Windows Node) 
	-log-interval	time between 2 logging lines in second (default: 5 seconds) 
	-opmem	Performing memory optimization before mining, require ROOT permission (not available on android) 
	-disable-api	Disable miner API on port 60666, this API is required for hiveOS 
	-no-watchdog	Disable astrominer watchdog
	-log-to-file	Redirect all astrominer log to a file
	-sock-address	Socks5 ip address with port (eg: 127.0.0.1:8192) (default: null)
	-sock-auth	Socks5 username and password (eg: username:password). 
 			NOTE: this username and password can't contain space and : symbol (default: null)
	-report-realtime-hashrate	 Enable sending realtime hashrate to hansen33 mod node (default: disable)
	-zero-hr-restart-time	 Time (in second), restart (or exit if the watchdog is disabled) 
 				the miner after being zero hashrate for a while (default: 120 seconds, set -1 to disable)
	
3.2- Lệnh khai thác coin Dero:

	./astrominer -w YOUR_ADDRESS -r YOUR_NODE:YOUR_PORT -p rpc

-- Địa chỉ Ví DERO:

Tại sàn tradeogre https://tradeogre.com : 

	deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr

Tại sàn Kucoin https://www.kucoin.com: (destination port: 1927721091 ) : 

	deroi1qyr8wnk9aw9lel0xcufdj98cqtd3lc5y84nhl679nm3wknaz0ad6xq9pvfz92xnju6cgx2ww579

-- Câu lệnh cho từng máy:

Máy 01: M01_S9pX

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M01_S9pX

Máy 02: M02_S9pH

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M02_S9pH

Máy 03: M03_S9pH

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M03_S9pH

Máy 04: M04_S9pX

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M04_S9pX

Máy 05: M05_S9X

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M05_S9X

Máy 06: M06_S10pT

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M06_S10pT

Máy 07: M07_Note8

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M07_Note8

Máy 08: M08_S8pT

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M08_S8pT

Máy 09: M09_A72017

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 3 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M09_A72017

Máy 10: M10_S9pH

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M10_S9pH

Máy 11: M11_M30s

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M11_M30s

Máy 12: M12_G2plx

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M12_G2plx

Máy 13: M13_SH701sh

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M13_SH701sh

Máy 14: M14_ZFlip1

	./astrominer -r community-pools.mysrv.cloud:10300 -p rpc -m 6 -w deroi1qyzlxxgq2weyqlxg5u4tkng2lf5rktwanqhse2hwm577ps22zv2x2q9pvfz92xcxtq2z2k7l9sdq2h0pgr.M14_ZFlip1
