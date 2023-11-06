# CẤU HÌNH IP STATIC CHO CENTOS 7.

## MỤC LỤC 

[I. SỬ DỤNG GIAO DIỆN.](#i-sử-dụng-giao-diện)
- [1.1. CONFIG LUÔN LÚC SETUP.](#11-cách-1-config-luôn-lúc-setup)
- [1.2. CONFIG BẰNG FILE CARD CẤU HÌNH MẠNG..](#12-cách-2-config-bằng-file-card-cấu-hình-mạng)

[II. SỬ DỤNG CÂU LỆNH.](#ii-sử-dụng-câu-lệnh)






## I. SỬ DỤNG GIAO DIỆN.

### 1.1. CÁCH 1: CONFIG LUÔN LÚC SETUP.

![hinh ](../images/4_config.png)
![hinh ](../images/5_config.png)
![hinh ](../images/7_config.png)


## 1.2. CÁCH 2: CONFIG BẰNG FILE CARD CẤU HÌNH MẠNG..

`nmtui edit +tên cạc mạng`: dùng để truy cập file config card mạng.

![hinh ](../images/6_config.png)





## II. SỬ DỤNG CÂU LỆNH.
## _BƯỚC 1_: KIỂM TRA CARD MẠNG ĐANG SỬ DỤNG LÀ CÁI NÀO.

dùng một trong số các lệnh sau:

- *ip addr*


![hinh ](../images/1_ipaddr.png)

=> card mạng đang dùng là ens33

## _BƯỚC 2_: KIỂM TRA GETWAY

lệnh : *ip route*

##  _BƯỚC 3_: TRUY CẬP FILE SCRIP CỦA CẠC MẠNG ENS33

*vi /etc/sysconfig/network-scripts/ifcfg-tên cạc mạng*: điền cái tên cạc mạng thêm vào là ens33. ta sẽ đi tới file scrip card mạng. và ta sẽ thay đổi, viết thêm ở đây.

(lưu ý: ấn nút "i" để vào chế độ viết, ấn nút "Esc+:wq" để lưu thay đổi)


 ![](../images/2_script_card_network.png)

 ## _BƯỚC 4_: KHỞI ĐỘNG LẠI CẠC MẠNG

 *service network restart*: lệnh khởi dộng lại cạc mạng.



