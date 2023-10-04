# 3 CHẾ ĐỘ VMNET TRÊN VMWARE


## I. NAT.

### 1.1. KHÁI NIỆM

Trong chế độ này, card mạng của máy ảo sẽ được kết nối thông qua một card mạng ảo trên máy chủ VMware, và máy chủ VMware sẽ hoạt động như một bộ định tuyến NAT. Card mạng ảo trên máy chủ VMware sẽ cung cấp địa chỉ IP cho máy ảo và chuyển tiếp các gói tin giữa máy ảo và mạng bên ngoài. Máy ảo có thể truy cập vào Internet và các nguồn tài nguyên bên ngoài, nhưng không thể trực tiếp truy cập vào các máy tính khác trong mạng.

### 1.2. PING RA INTERNET

Kiểm tra ip máy ảo:

![hinh ](../images/1_host_only.png)

Ping ra ngoài intenet:

![hinh ](../images/1_nat.png)






## II. HOST ONLY

### 2.1. KHÁI NIỆM

Trong chế độ này, card mạng của máy ảo chỉ được kết nối với một mạng ảo riêng trên máy chủ VMware. Máy ảo có thể giao tiếp với máy chủ VMware và các máy ảo khác trong cùng mạng ảo, nhưng không thể truy cập vào mạng bên ngoài hoặc các máy tính khác trong mạng vật lý. Chế độ Host-Only thường được sử dụng để tạo ra một mạng riêng trong môi trường phát triển hoặc kiểm thử mà không cần kết nối với mạng bên ngoài.

### 2.2. PING VITRUAL MACHINE CARD NETWORK HOST ONLY TO VITRUAL MACHINE

kiểm tra ip máy ảo: ip addr

Máy ảo 1:

![hinh ](../images/1_host_only.png)

Máy ảo 2:

![hinh ](../images/2_host_only.png)

Ping máy ảo 2 sang máy ảo 1:

![hinh ](../images/3_host_only.png)







## III. BRIDGED

### 3.1. KHÁI NIỆM

 Trong chế độ này, card mạng của máy ảo sẽ được kết nối trực tiếp với mạng vật lý bên ngoài thông qua một card mạng vật lý trên máy chủ VMware hoặc máy tính chủ. Máy ảo sẽ có địa chỉ IP duy nhất trên mạng vật lý và có thể truy cập vào các thiết bị và nguồn tài nguyên trong mạng bên ngoài. Chế độ Bridge cho phép máy ảo tham gia vào mạng như một máy tính riêng biệt và có thể giao tiếp với các máy tính khác trong mạng.




### 3.2. PING VITRUAL MACHINE CARD NETWORK BRIDGED TO PHYSICAL MACHINE.

kiểm tra ip máy ảo: ip addr


![hinh ](../images/1_bridged.png)

kiểm tra ip máy vật lý: ipconfig

![hinh ](../images/2_bridged.png)


ping máy ảo sang máy thật.


![hinh ](../images/3_bridged.png)









