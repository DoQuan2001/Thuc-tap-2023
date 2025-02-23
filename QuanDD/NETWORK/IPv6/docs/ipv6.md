# TÌM HIỂU VỀ IP VERSION 6

## MỤC LỤC.

[I. IPv6 LÀ GÌ?](#i-ipv6-là-gì)



[II. LỢI ÍCH KHI SỬ DỤNG IP V6.](#ii-lợi-ích-khi-sử-dụng-ip-v6)

[III. IPv6 DATAGRAM](#iii-ipv6-datagram)

[IV. CẤU TRÚC IPv6.](#iv-cấu-trúc-ipv6)

- [4.1. BIỂU DIỄN IP V6.](#41-biểu-diễn-ip-v6)

- [4.2. THÀNH PHẦN IP V6.](#42-thành-phần-ip-v6)

[V. CÁC LOẠI ĐỊA CHỈ IPv6.](#v-các-loại-địa-chỉ-ipv6)











## I. IPv6 LÀ GÌ?

IPv6 là phiên bản tiếp theo của giao thức Internet Protocol (IP), mà được sử dụng để điều hướng gói tin trên mạng Internet. Nó được thiết kế để thay thế cho IPv4, giao thức hiện tại được sử dụng rộng rãi nhất trên thế giới.


IPv6 được sử dụng để giải quyết vấn đề về _hạn chế số lượng địa chỉ IP có sẵn trong IPv4_. Vì IPv4 chỉ có khoảng 4,3 tỷ địa chỉ khả dụng, nên không thể đáp ứng được nhu cầu của các thiết bị mới đang liên tục được kết nối vào Internet. IPv6 cung cấp hàng tỷ lượng địa chỉ IP khổng lồ hơn, do đó có thể đáp ứng tốt hơn nhu cầu của thiết bị mới và các hệ thống không dây.

## II. LỢI ÍCH KHI SỬ DỤNG IP V6.

Để hình dung rõ hơn lợi ích IPv6 mang lại, chúng ta sẽ đến với những công dụng sau đây của IPv6:

- IPv4 chỉ có 32 bit nên chỉ có thể cung cấp 4 tỷ địa chỉ IP. Còn IPv6 có đến 128 bit nên có thể cung cấp đến 2128 địa chỉ IP. Đây là một con số khổng lồ có thể đáp ứng tốt hơn nhu cầu của các thiết bị mới đang liên tục được kết nối vào Internet.

- Giúp cho việc truyền dữ liệu trên mạng được nhanh hơn, vì nó có thể xử lý các gói tin nhanh hơn so với IPv4.

- Cung cấp các tùy chọn bảo mật tăng cường như IPSec, giúp cho mạng được bảo vệ tốt hơn khỏi các tấn công.
Hỗ trợ tính năng multicast và anycast, giúp cho việc truyền tin trên mạng được hiệu quả hơn.

- Giúp cho việc triển khai các dịch vụ mạng mới và nâng cao hiệu suất mạng hiệu quả hơn.

- Hỗ trợ các thiết bị không dây và các hệ thống không dây, giúp cho việc kết nối và trao đổi dữ liệu trên mạng không dây được thuận tiện hơn.


## III. IPV6 DATAGRAM.

![hinh ](../images/11_IPV6_diagram.png)

![hinh ](../images/12_IPV6_header.png)

- Payload: Thông thường, nó có thể lên đến 65535 byte. Trong IPv6, PDU thường bao gồm độ dài của nó và Header của giao thức bậc cao, trong khi Extension chứa thông tin về dịch vụ đính kèm và nếu chuyển sang trường khác, nó có thể có hoặc không.
- Version: bao gồm 4 bit có chức năng xác định phiên bản của giao thức.
- Traffic Class: Gồm 8 bit được sử dụng nhằm xác định loại lưu lượng.
- Flow label: 20 bit cho mỗi giá của luồng dữ liệu
- Payload Length: 16 bit (số dương). Hỗ trợ xác định kích thước của phần tải theo sau Header IPv6.
- Next-Header: 8 bit giúp xác định Header tiếp theo của gói tin.
- Hop Limit: 8 bit (số dương). Giá trị này giảm đi một đơn vị qua mỗi Node (giảm xuống 0, gói tin bị loại bỏ).
- Source address Địa chỉ IPv6 nguồn của gói được mang theo 128 bit


## IV. CẤU TRÚC IPv6.

###     4.1. BIỂU DIỄN IP V6.

![hinh ](../images/1_cau_truc.png)

IP v6 gồm 128 bit được chia thành 8 HEXTET. mỗi HEXTET là 16 bit ngăn cách nhau bởi dấu ":".

**CÁCH THU GỌN ĐỊA CHỈ IP V6**:
 - Một chuuỗi số 0 liên tiếp có thể được lược bỏ. điều này chỉ có thể làm một lần

 - 4 số 0 trong một octet có thể viết bằng một con số 0

 - các số 0 đầu tiên trong một octet có thể được lược bỏ

 ví dụ:

 ![hinh](../images/2_vi_du.png)


### 4.2. THÀNH PHẦN IP V6.

IP V6 cũng giồm 3 phần: PREFIX, SUBNETID VÀ HOST.

![hinh ](../images/8_thanh_phan.png)

Site prefix: là số được gán đến website bằng một ISP. Theo đó, tất cả máy tính trong cùng một vị trí sẽ được chia sẻ cùng một site prefix. Site prefix hướng tới dùng chung khi nó nhận ra mạng của bạn và cho phép mạng có khả năng truy cập từ Internet.

Subnet ID: là thành phần ở bên trong trang web, được sử dụng với chức năng miêu tả cấu trúc trang của mạng. Một IPv6 subnet có cấu trúc tương đương với một nhánh mạng đơn như subnet của IPv4.


Interface ID: có cấu trúc tương tự ID trong IPv4. Số này nhận dạng duy nhất một host riêng trong mạng. Interface ID (thứ mà đôi khi được cho như là một thẻ) được cấu hình tự động điển hình dựa vào địa chỉ MAC của giao diện mạng. ID giao diện có thể được cấu hình bằng định dạng EUI-64.


#### 4.2.1. PHẦN NETID(LÀ SITE PREFIX+ SUBNETID).

phần net ID này do nhà mạng cấp, nhà mạng sẽ quy hoạch phần này như sau:

![hinh ](../images/4_quy-hoach.png)




#### 4.2.2. PHẦN HOST ID.

đây là cái hay nhất của IPV6 bởi IPv6 không có private IP, mà tất cả địa chỉ IPv6 đều là public IP.

đề làm được điều này, phần host id phải là duy nhất. IPv6 dùng một cơ chế EUI-64. cơ chế này sẽ chuyển đổi địa chỉ MAC của máy host thành chính địa chỉ HOST ID.

![hinh ](../images/5_host_id.png)

**CƠ CHẾ CHUYỂN ĐỔI ĐỊA CHỈ MAC THÀNH HOST ID**:

- 1. chia đôi địa chỉ MAC
- 2. chèn thêm FFFE vào giữa 2 phần chia đôi ( vì địa chỉ mac chỉ có 48 bit, mà host id cần 64 bít nên cần chèn vào để cho đủ 64 bit)
- 3. đảo giá trị bit thứ 7 trong host id (ví dụ bit thứ 7 là 0 sẽ đảo ngược lại thành 1)

ví dụ: 

![HINH ](../images/6_host_id.png)



Ví dụ: Với một địa chỉ IPv6 có cấu trúc như sau: 2001:0f68:0000:0000:0000:0000:1986:69af, sẽ bao gồm:

Site prefix: 2001:0f68:0000
Subnet ID: 0000
host ID: 0000:0000:1986:69af


#### 4.2.3. prefix-length.

Độ dài tiền tố là giá trị thập phân cho thấy số bit ngoài cùng bên trái của địa chỉ là phần mạng.

VÍ DỤ:  Hãy lấy 2001:aaaa:bbbb:cccc:0:0:0:10/64 làm ví dụ. Độ dài mặt nạ mạng là 64 có nghĩa là mạng con IPv6 là 2001:aaaa:bbbb:cccc::/64 và 2001:aaaa:bbbb:cccc::10 là một nút trong mạng con này. 


Thông thường trong IPv6, các kỹ sư chọn độ dài tiền tố là bội số của 4. Điều đó làm cho tiền tố dễ hiểu hơn mà không cần sử dụng máy tính mạng con.

![hinh ](../images/14_prefix.png)

![hinh ](../images/13_prefix.png)













## V. CÁC LOẠI ĐỊA CHỈ IPv6.





Có 3 loại địa chỉ IPv6:

- Unicast( truyền điểm điểm): là địa chỉ cho một giao tiếp. Một gói dữ liệu được gửi đến một địa chỉ Unicast sẽ được phân phối tới cổng giao tiếp được chỉ ra bởi địa chỉ đó.

- Anycast : là địa chỉ cho tập hợp các cổng giao tiếp. Các tập này thông thường thuộc về các node khác nhau. Một gói dữ liệu được gửi đến một địa chỉ anycast sẽ được phân phối đến cổng giao tiếp gần nhất hay đầu tiên trong nhóm anycast.

- Multicast ( truyền điểm- đa điểm): địa chỉ cho một tập hợp các cổng giao tiếp (thông thường thuộc về các node khác nhau). Khi một gói được gửi đến một địa chỉ multicast, tất cả các cổng giao tiếp sẽ nhận được gói dữ liệu này.

![hinh ](../images/9_cac_loai.png)


lưu ý: IPV6 không dùng địa chỉ broadcast và không dùng subnetmask.

### 5.1. ĐỊA CHỈ UNICAST

Địa chỉ Unicast gồm có các loại khác nhau :

**Global Unicast Address**: tương ứng với địa chỉ Public của IPv4, là loại địa chỉ được cho phép truy cập rộng rãi trên Internet, hỗ trợ việc định tuyến và đánh địa chỉ phân cấp. (do nhà mạng cấp)

**Link-Local Address**: địa chỉ này được cấu hình một cách tự động trên interface của thiết bị. Địa chỉ này luôn bắt đầu với FE80. 16 bit đầu tiên của địa chỉ liên kết cục bộ luôn được đặt là 1111 1110 1000 0000 (FE80). 48 bit tiếp theo thì được đặt thành 0, do đó nó chỉ sử dụng để liên lạc giữa các máy chủ IPv6 trên một liên kết (phân đoạn quảng bá). Các địa chỉ này không thể định tuyến. Vì vậy, bộ định tuyến không bao giờ chuyển tiếp các địa chỉ này bên ngoài liên kết.

**Site-Local Address**: tương tự như địa chỉ Private trong IPv4 (10.0.0.0/8,172.16.0.0/12 và 192.168.0.0/16), dùng trong nội bộ một site.

**Unique-Local Address**: được sử dụng trong phạm vi toàn cầu, dùng để thay thế cho địa chỉ site-local.

**Loopback address**: tương tự 127.0.0.1 trong ipv4. dùng để kiểm tra 


### 5.2. ĐỊA CHỈ MULTICAST.

CHỨC NĂNG TƯƠNG TỰ NHƯ DẢI MẠNG D CỦA BÊN IPV4 DẢI MÀ TỪ 224.0.0.0

-Luôn bắt đầu bằng FF.

-Cờ(Flag): trường này có 4 bít “0T00”

+Bit T=0: đây là địa chỉ multicast IPv6 vĩnh viễn được IANA quy định
+Bit T=1: đây là dạng địa chỉ multicast không vĩnh viễn.

-Phạm vi(Scope): trường này cũng gồm 4bit, dùng để xác định phạm vi của nhóm địa chỉ multicast, tùy thuộc vào giá trị mà phạm vi được xác định như sau:

+0001=1 : phạm vi Node

+0010=2 : phạm vi Link

+0101=5 : phạm vi Site

+1000=8 : phạm vi tổ chức(Organisation)

+1110=E : phạm vi toàn cầu(Global)





---
***SUMMARY***

![hinh ](../images/7_ipv6_category.png)

```
- Well-known Multicast.

     - Tất cả các địa chỉ multicast phổ biến đều bắt đầu bằng tiền tố ff00::/12.
     - Chúng có chức năng tương tự như 224.0.0.0/24 trong IPv4.

- Solicited-Node Multicast.

     - Mỗi địa chỉ unicast IPv6 có một địa chỉ multicast nút được yêu cầu tương ứng.
     - Cấu trúc bao gồm tiền tố cố định FF02::1:FF00:0/104 và 24 bit cuối cùng của địa chỉ IPv6 tương ứng.
     - Các nhóm multicast đặc biệt này được sử dụng để phân giải địa chỉ, phát hiện hàng xóm và phát hiện địa chỉ trùng lặp.

- Global Unicast

     - Hiện tại, IANA phân bổ các địa chỉ unicast toàn cầu bắt đầu bằng giá trị nhị phân 001 (2000::/3).
     - Cấu trúc của chúng bao gồm tiền tố định tuyến toàn cầu 48 bit và ID mạng con 16 bit còn được gọi là Bộ tổng hợp cấp độ trang web (SLA).
     - Cấu trúc của các địa chỉ này cho phép tổng hợp các mục định tuyến để đạt được bảng định tuyến IPv6 toàn cầu nhỏ hơn.


- Unique-local
     - Nó có một tiền tố duy nhất trên toàn cầu tương tự như các địa chỉ unicast toàn cầu.

     - Đây là không gian địa chỉ độc lập của Nhà cung cấp dịch vụ Internet

- Loopback
     - Địa chỉ loopback nổi tiếng trong IPv6 là ::1/128.
     - Khái niệm tương tự như 127.0.0.0/8 trong IPv4.
     - Thường được sử dụng để kiểm tra ngăn xếp giao thức TCP/IP trong hệ điều hành.

- Unspecified

     - Địa chỉ không xác định trong IPv6 là ::/128.
     - Khái niệm tương tự như 0.0.0.0 trong IPv4

- Link-local 

     - tiền tố FE80::/10.
     - Tự động được gán cho bất kỳ giao diện hỗ trợ IPv6 nào.
     - Tương tự như 169.254.0.0/16 trong IPv4.
     - Không thể định tuyến được. Chúng chỉ có giá trị trong phạm vi của một giao diện.
     - Được sử dụng để khám phá hàng xóm và tự động cấu hình không trạng thái.

- Embedded IPv4-in-IPv6

     - Địa chỉ IPv4 A.B.C.D (bằng chữ số hex) được nhúng trong IPv6 dưới dạng 0:0:0:0:0:0:A:B:C:D hoặc chỉ ::A:B:C:D.
     - Địa chỉ IPv6 được sử dụng trong các đường hầm tự động hỗ trợ cả IPv4 và IPv6.




```





---
*Danh mục tài liệu tham khảo*

[1] https://bkhost.vn/blog/ipv6/

[2] https://www.totolink.vn/article/75-cau-truc-ipv6-va-cac-loai-dia-chi-ipv6.html

[3] https://www.youtube.com/watch?v=1RrV4wHke18

[4] https://maychuviet.vn/cau-truc-ipv6/

[5] https://viblo.asia/p/tim-hieu-ve-ipv6-3P0lPyDG5ox

[6] https://www.networkacademy.io/ccna/ipv6/ipv6-address-types

[7] https://www.quora.com/What-is-the-range-of-global-unicast-address-in-ipv6
