# ĐỔI PORT SSH.

TA THỰC HIỆN THEO NHỮNG BƯỚC SAU:

### BƯỚC 1: CHỈNH SỬA PORT TRONG FILE CONFIG SHH.
`vi /etc/ssh/sshd_config`: chỉnh sửa file config ssh.

![hinh ](../images/2.png)

### BƯỚC 2: RESTART DỊCH VỤ SSH.

`systemctl restart sshd`: câu lệnh restart.

### BƯỚC 3: RESTART DỊCH VỤU FIREWALLL.

`firewall-cmd --permanent --add-port=new_porrt/tcp`:Thêm quy tắc tường lửa để mở cổng port ssh mới.

`systemctl restart firewalld`: restart dịch vụ firewwall.



SCRIPT VIẾT CHO TIỆN.

(nhớ cấp quyền chạy nha rồi khi chạy nhớ cho port mới vào nha)


```

#!/bin/bash

# Kiểm tra xem script có được chạy với quyền root không
if [ "$EUID" -ne 0 ]; then
  echo "Hãy chạy script này với quyền root (sudo)."
  exit 1
fi

# Biến cổng SSH mới
NEW_SSH_PORT=${1:-"22"} // tạo biến mặc định nhỡ quên nó tự đổi về 22.

# Tạo bản sao lưu của tệp cấu hình SSH
cp /etc/ssh/sshd_config /etc/ssh/sshd_config.bak

# Thay đổi cổng SSH thành biến NEW_SSH_PORT trong tệp cấu hình
sed -i "s/^Port 22$/Port $NEW_SSH_PORT/" /etc/ssh/sshd_config

# Khởi động lại dịch vụ SSH để áp dụng thay đổi
systemctl restart sshd

# Cập nhật quy tắc tường lửa (nếu sử dụng firewalld)
firewall-cmd --zone=public --add-port=$NEW_SSH_PORT/tcp --permanent
firewall-cmd --reload

echo "Đã thay đổi cổng SSH thành $NEW_SSH_PORT. 

```