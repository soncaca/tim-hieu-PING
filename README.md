# tim-hieu-giao-thuc-PING 
#1
Nhắc đến ping thì phải gắn liền với ICMP ( internet control mesage protocol )- giao thức điều khiển truyền tin trên mạng.

IP không hề có cơ chế nào để xác nhận dữ liệu đã được chưyển tới đích hay chưa. IP sử dụng giao thức ICMP  để thông báo cho máy nguồn biết là sự cố xảy ra trong quá trình truyền dữ liệu. Có rất nhiều lý do mà khi gói tin đang trên đường tới đích gặp sự cố ví dụ như phần cứng bị hư hỏng, cấu hình sai hoặc thông tin định tuyến không đúng.

IP là một phương thức truyền dữ liệu không tin cậy trên mạng.ICMP không khắc phục được sự không tin cậy của IP, ICMP chỉ đơn giản là phát đi các thông điệp để thông báo về sự cố, báo cho sender biết việc gửi data đi đã có vấn đề.


Thông điệp ICMP đựơc đóng gói giống như các dữ liệu khác khi truyền đi bằng IP, vì vậy nó cũng có thể gặp sự cố, nếu một thông điệp báo sự cố mà gặp sự cố thì nó sẽ gây phát sinh thêm những thông điệp báo sự cố mới và hiển nhiên nó sẽ gây ra tình trạng nghẽn mạng. Chính vì vậy mà sẽ không có một error report cho chính nó nữa và dẫn đến khả năng là thông điệp ICMP sẽ không bao giờ thông báo được sự cố đến  máy nguồn.

Có nhiều loại thông điệp ICMP và mỗi cái lại mang một thông điệp lỗi cụ thể khác nhau. Và kiểu thông điệp được phân biệt nhờ format dữ liệu của thông điệp đó.
Định dạng của bản tin ICMP:
+ Type of ICMP message (8 bits): là một số nguyên 8bit để xác định thông điệp
+ Code (8 bits): Bổ sung thông tin thêm cho Type
+ Checksum (16 bits): để kiểm tra lỗi cho dư liệu
<img src="http://i.imgur.com/BdC2xQh.png">


Dưới đây là đầy đủ về control message:
<img src="http://i.imgur.com/2S5AtA4.png">
<img src="http://i.imgur.com/rtqJ3rt.png">





#2
Ping là một chương trình internet cơ bản mà chúng ta sử dụng hằng ngày.

Giao thức ICMP có thể được sử dụng để kiểm xem có đến được một địa chỉ nào đó hay không .ICMP sẽ gửi thông điệp echo request đến máy đích .Nếu máy đích nhận được echo request thì sẽ trả lời lại thông điệp echo reply cho máy nguồn .Nếu máy nguồn nhận được echo reply thì điều đó khặng định là máy đích có thể đến được bằng giao thức IP. Lệnh ping khởi tạo các thông điệp echo request.Lệnh ping gửi đi 4 gói echo request và nhận về 4 gói echo reply xác nhận kết nối IP giữa 2 thiết bị hoạt động tốt.


#Thực hành ICMP với lệnh PING













(ICMP is a necessary component of any TCP/IP implementation. It does not exist to provide information to the
higher-layer protocols (like TCP and UDP) so that they may be more reliable. Rather, ICMP provides network
diagnostic capabilities and feedback to those responsible for network administration and operation. See RFC
792,if you are really interested)



