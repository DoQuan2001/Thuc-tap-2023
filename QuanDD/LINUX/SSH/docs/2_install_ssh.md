# CÀI ĐẶT SSH 

## I. CÀI ĐẶT SSH.

### 1.1. CENTOS7

#### Bước 1: Cài đặt OpenSSH Server
 Mở terminal trên CentOS 7 và sử dụng lệnh sau để cài đặt OpenSSH Server:
`sudo yum install openssh-server`: cài đặt OpenSSH Server.
#### Bước 2: Khởi động dịch vụ SSH và thiết lập tự động khởi động
Sau khi cài đặt xong, bạn cần khởi động dịch vụ SSH và đặt nó để tự động khởi động cùng hệ thống. Sử dụng các lệnh sau:


`sudo systemctl start sshd`: lệnh khởi động
`sudo systemctl enable sshd`: lệnh khởi động dịch vụ ssh cùng hệ thống
#### Bước 3: Kiểm tra trạng thái của dịch vụ SSH
Đảm bảo rằng dịch vụ SSH đang chạy bằng cách sử dụng lệnh:

`sudo systemctl status sshd`: kiểm tra trạng thái
Nếu mọi thứ diễn ra đúng, bạn sẽ thấy thông báo về trạng thái hoạt động của dịch vụ.


#### 1.2. UBUNTU 

#### Bước 1: Cài đặt OpenSSH Server
 Mở terminal trên CentOS 7 và sử dụng lệnh sau để cài đặt OpenSSH Server
`sudo apt-get update`: Update server Ubuntu 
`sudo apt-get install openssh-server`: cài ssh server.

#### Bước 2: Khởi động dịch vụ SSH và thiết lập tự động khởi động
Sau khi cài đặt xong, bạn cần khởi động dịch vụ SSH và đặt nó để tự động khởi động cùng hệ thống. Sử dụng các lệnh sau:

`sudo systemctl start sshd`: lệnh khởi động
`sudo systemctl enable sshd`: lệnh khởi động dịch vụ ssh cùng hệ thống
#### Bước 3: Kiểm tra trạng thái của dịch vụ SSH
Đảm bảo rằng dịch vụ SSH đang chạy bằng cách sử dụng lệnh:

`sudo systemctl status sshd`: kiểm tra trạng thái
Nếu mọi thứ diễn ra đúng, bạn sẽ thấy thông báo về trạng thái hoạt động của dịch vụ.





