# VPN-Virtual-private-network-


### 1.	Định nghĩa VPN:

VPN(virtual private network) là công nghệ xây dựng hệ thống mạng riêng ảo nhằm đáp ứng nhu cầu chia sẻ thông tin, truy cập từ xa và tiết kiệm chi phí. 

VPN cho phép các máy tính truyền thông với nhau thông qua một môi trường chia sẻ như mạng Internet nhưng vẫn đảm bảo được tính riêng tư và bảo mật dữ liệu. Để cung cấp kết nối giữa các máy tính, các gói thông tin được bao bọc bằng một header có chứa những thông tin định tuyến, cho phép dữ liệu có thể gửi từ máy truyền qua môi trường mạng chia sẻ và đến được máy nhận, như truyền trên các đường ống riêng được gọi là tunnel. Để bảo đảm tính riêng tư và bảo mật trên môi trường chia sẻ này, các gói tin được mã hoá và chỉ có thể giải mã với những khóa thích hợp, ngăn ngừa trường hợp "trộm" gói tin trên đường.


### 2.	Chức năng của VPN

- **Sự tin cậy (Confidentiality)**: Người gửi có thể mã hoá các gói dữ liệutrước  khi  truyền  chúng  ngang  qua  mạng.  Bằng  cách  làm  như  vậy, không một ai có thể  truy nhập thông tin mà không được phép, mà nếu lấy được thông tin thì cũng không đọc được vì thông tin  đã  được mã hoá.
 
-	**Tính  toàn  vẹn  dữ  liệu  (Data  Integrity)**:  Người  nhận  có  thể  kiểm  tra rằng dữ liệu đã  được truyền qua mạng Internet mà không có sự thay đổi nào.

-	**Xác thực nguồn gốc (Origin Authentication)**: Người nhận có thể xác thực nguồn gốc của gói dữ liệu, đảm bảo và công nhận nguồn thông tin.


### 3.	Các dạng kết nối mạng riêng ảo VPN.

- Remote Access: Đáp ứng nhu cầu truy cập dữ liệu và ứng dụng cho người dùng ở xa, bên ngoài công ty thông qua Internet.

  Ví dụ: khi người dùng muốn truy cập vào cơ sở dữ liệu hay các file server, gửi nhận email từ các mail server nội bộ của      công ty.

- Site To Site: Áp dụng cho các tổ chức có nhiều văn phòng chi nhánh, giữa các văn phòng cần trao đổi dữ liệu với nhau. 

  Ví dụ một công ty đa quốc gia có nhu cầu chia sẻ thông tin giữa các chi nhánh đặt tại Nhật Bản và Việt Nam, có thể xây dựng   một hệ thống VPN Site-to-Site kết nối hai site Việt Nam và Nhật Bản tạo một đường truyền riêng trên mạng Internet phục vụ    quá trình truyền thông an toàn, hiệu quả.


### 4.	Các giao thức sử dụng trong VPN.

#### 4.1	PPTP(Point-to-Point Tunneling Protocol)

PPTP là một phương thức của mạng riêng ảo, được phát triển bởi Microsoft kết hợp với một số công ty khác, nó sử dụng một kênh điều khiển qua giao thức TCP và đường  hầm  GRE  để  đóng  gói  các  gói  dữ  liệu  PPP  (Point-to-Point).  PPTP  là  một phần của các tiêu chuẩn Internet Point-to-Point (PPP), PPTP sử  dụng các loại xác thực như PPP (PAP, SPAP, CHAP, MS-CHAP, và EAP).

**Tính năng:**

  - PPTP tạo ra nhiều kết nối giữa các khách hàng mà không yêu cầu dịch vụ đặc biệt ISP.
  
  - PPTP  phù  hợp  trên  nhiều  hệ  điều  hành  thông  dụng.  (Microsoft  ,Nortel Network, TeteSystems…).
  
  - PPTP hỗ  trợ  các dịch vụ  IP, mã hóa các gói tin RC4 (56 bit hoặc 128 bit), sử dụng port 1723 và các giao thức GRE.

**Hạn chế:**

  Khó khăn lớn nhất gắn kèm với PPTP là cơ chế  yếu kém về bảo  mật  do nó 
  dùng  mã  hóa  đồng  bộ  trong  khóa  được  xuất  phát  từ  việc  nó  sử  dụng  mã  hóa  đối xứng là cách tạo ra khóa từ     mật khẩu của người dùng. Điều này càng nguy hiểm hơn vì  mật  khẩu  thường  gửi  dưới  dạng  phơi  bày  hoàn  toàn  trong    quá  trình  xác  nhận. Giao thức tạo đường hầm kế tiếp (L2F) được phát triển nhằm cải thiện bảo mật với mục đích này.


#### 4.2	L2TP (Layer 2 Tunneling Prototype)

IETF đã kết hợp hai giao thức PPTP và L2F và phát triển thành L2TP. Nó kết 
hợp những đặc điểm tốt nhất của PPTP và L2F. Vì vậy, L2TP cung cấp tính linh 
động, có thể thay đổi, và hiệu quả chi phí cho giải pháp truy cập từ xa của L2F và 
khả năng kết nối điểm điểm nhanh của PPTP.

**Thuận lợi:**

  - L2TP là một giải pháp chung. Hay nói cách khác nó là một nền tảng độc lập. 
  
  - Nó cũng hỗ trợ nhiều công nghệ mạng khác nhau. Ngoài ra, nó còn hỗ trợ giao dịch qua kết nối WAN non-IP mà không cần một   IP.
  
  - L2TP  tunneling  trong  suốt  đối  với  ISP  giống  như  người  dùng  từ  xa.  Do  đó, không đòi hỏi bất kỳ cấu hình nào   ở phía người dùng hay ở ISP. 
  
  - L2TP cho phép một tổ chức điều khiển việc xác nhận người dùng thay vì ISP phải làm điều này. 
  
  - L2TP  cung  cấp  chức  năng  điều  khiển  cấp  thấp  có  thể  giảm  các  gói  dữ  liệu xuống tùy ý nếu đường hầm quá tải.   Điều này làm cho qua trình giao dịch bằng L2TP nhanh hơn so với quá trình giao dịch bằng L2F. 
  
  - L2TP cho phép người dùng từ xa chưa đăng ký (hoặc riêng tư) địa chỉ IP truy cập vào mạng từ xa thông qua một mạng công     cộng. 
  
  - L2TP nâng cao tính bảo mật do sử dụng IPSec-based payload encryption trong suốt qua trình tạo hầm, và khả năng triển khai   xác nhận IPSec trên từng gói dữ liệu.

**Bất lợi:**

  - L2TP chậm hơn so với  PPTP hay L2F bởi vì nó dùng IPSec để xác nhận mỗi gói dữ liệu nhận được.
  
  - Mặc dù PPTP được lưu chuyển như một giải pháp VPN dựng sẵn, một Routing and Remote Access Server (RRAS) cần có những cấu   hình mở rộng


####4.3	SSTP( Secure Socket Tunneling Protocol)

SSTP (Secure Socket Tunneling Protocol) là một dạng của kết nối VPN trong Windows Vista và Windows Server 2008. SSTP sử dụng các kết nối HTTP đã được mã hóa SSL để thiết lập một kết nối VPN đến VPN gateway. SSTP là một giao thức rất an toàn vì các thông tin quan trọng của người dùng không được gửi cho tới khi có một “đường hầm” SSL an toàn được thiết lập với VPN gateway. SSTP cũng được biết đến với tư cách là PPP trên SSL, chính vì thế nó cũng có nghĩa là bạn có thể sử dụng các cơ chế chứng thực PPP và EAP để bảo đảm cho các kết nối SSTP được an toàn hơn


####4.4	IPSec 

IP Security (IPSec) là một giao thức được chuẩn hoá bởi IETF từ năm 1998 nhằm mục đích nâng cấp các cơ chế mã hoá và xác thực thông tin cho chuỗi thông tin truyền đi trên mạng bằng giao thức IP. Hay nói cách khác, IPSec là sự tập hợp của các chuẩn mở được thiết lập để đảm bảo sự cẩn mật dữ liệu, đảm bảo tính toàn vẹn dữ liệu và chứng thực dữ liệu giữa các thiết bị mạng.

IPSec cung cấp một cơ cấu bảo mật ở tầng 3 (Network layer) của mô hình OSI.

IPSec được thiết kế như phần mở rộng của giao thức IP, được thực hiện thống nhất trong cả hai phiên bản IPv4 và IPv6. Đối với IPv4, việc áp dụng IPSec là một tuỳ chọn, nhưng đối với IPv6, giao thức bảo mật này được triển khai bắt buộc.
