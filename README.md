# tim-hieu-giao-thuc-PING 
Ping là một chương trình internet cơ bản mà chúng ta sử dụng hằng ngày.

Nhắc đến ping thì phải gắn liền với ICMP ( internet control mesage protocol )- giao thức điều khiển truyền tin trên mạng.

IP không hề có cơ chế nào để xác nhận dữ liệu đã được chưyển tới đích hay chưa. IP sử dụng giao thức ICMP  để thông báo cho máy nguồn biết là sự cố xảy ra trong quá trình truyền dữ liệu. Có rất nhiều lý do mà khi gói tin đang trên đường tới đích gặp sự cố ví dụ như phần cứng bị hư hỏng, cấu hình sai hoặc thông tin định tuyến không đúng.

IP là một phương thức truyền dữ liệu không tin cậy trên mạng.ICMP không khắc phục được sự không tin cậy của IP, ICMP chỉ đơn giản là phát đi các thông điệp để thông báo về sự cố, báo cho sender biết việc gửi data đi đã có vấn đề.


Thông điệp ICMP đựơc đóng gói giống như các dữ liệu khác khi truyền đi bằng IP, vì vậy nó cũng có thể gặp sự cố, nếu một thông điệp báo sự cố mà gặp sự cố thì nó sẽ gây phát sinh thêm những thông điệp báo sự cố mới và hiển nhiên nó sẽ gây ra tình trạng nghẽn mạng. Chính vì vậy mà sẽ không có một error report cho chính nó nữa và dẫn đến khả năng là thông điệp ICMP sẽ không bao giờ thông báo được sự cố đến  máy nguồn.










(ICMP is a necessary component of any TCP/IP implementation. It does not exist to provide information to the
higher-layer protocols (like TCP and UDP) so that they may be more reliable. Rather, ICMP provides network
diagnostic capabilities and feedback to those responsible for network administration and operation. See RFC
792,if you are really interested)



