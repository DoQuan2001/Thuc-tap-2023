# MARKDOWN.

## Mục lục.

[1. Markdown là gì?](#1-markdown-là-gì)

[2. Cách sử dụng markdown.](#2-cách-sử-dụng-markdown)

[3.Syntax.](#3-syntax)


- [ 3.1. bảng.](#31-bảng)

- [3.2 hiển thị hình.](#32-hiển-thị-hình)

- [3.3. Danh sách](#33-danh-sách)

- [3.4. Đánh dấu cú pháp. ](#34-đánh-dấu-cú-pháp)

- [3.5. liên kết. ](#35-liên-kết)

- [3.6 in đậm.](#36-in-đậm)

- [ 3.7. gạch ngang.](#37-gạch-ngang)


## 1. Markdown là gì?.

Markdown là một ngôn ngữ đánh dấu với cú pháp văn bản thô (plant-text), được thiết kế để có thể dễ dàng chuyển thành HTML và nhiều định dạng khác sử dụng một công cụ cùng tên. Nó thường được dùng để tạo các tập tin readme, viết tin nhắn trên các diễn đàn, và tạo văn bản có định dạng bằng một trình biên tập văn bản thô (như notepad chẳng hạn).

## 2. Cách sử dụng markdown.

Với markdown, văn bản sẽ được tự động chuyển sang thành các đoạn văn bản (paragraphs) được phân cách bởi một dòng. Và không cần phải thêm thẻ xuống dòng như <br>, Các đoạn văn bản được chuyển sang như sử dụng các thẻ <p> thực sự. Ví dụ như sau:







## 3. Syntax.

### 3.1. bảng.


**MARDOWN**

```
| Cột 1 Hàng 1 | Cột 2 | Cột 3| Cột 4 |
|--------------|-------|------|-------|
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 | 2 x 4 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 | 3 x 4 |
| Hàng 4 | 4 x 1 | 4 x 2 | 4 x 3 | 4 x 4 |
```

**OUT**

| Cột 1 Hàng 1 | Cột 2 | Cột 3| Cột 4 |
|--------------|-------|------|-------|
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 | 2 x 4 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 | 3 x 4 |
| Hàng 4 | 4 x 1 | 4 x 2 | 4 x 3 | 4 x 4 |



### 3.2 hiển thị hình.


**MARDOWN**


```
![hình 1](/markdown/images/Screenshot_1.png)

```
**OUT**




![hình 1](/markdown/images/1_minh_hoa.png)


### 3.3. Danh sách

**MARDOWN**
```
{
1. First item
2. Second item
3. Third item
4. Fourth item
}
```
**HTML**
```
<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
  <li>Fourth item</li>
</ol>

```
**OUTPUT**
```
1. Mục đầu tiên
2. mục thứ hai
3. mục thứ ba
4. mục thứ tư

```







### 3.4. Đánh dấu cú pháp. 

Nhiều bộ xử lý Markdown hỗ trợ đánh dấu cú pháp cho các khối mã có hàng rào. Tính năng này cho phép bạn thêm đánh dấu màu cho bất kỳ ngôn ngữ nào mà mã của bạn được viết bằng. Để thêm đánh dấu cú pháp, hãy chỉ định một ngôn ngữ bên cạnh dấu gạch ngược trước khối mã có hàng rào.

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```


### 3.5. liên kết. 

**MARDOWN**
```
{

[Do Duc Quan](https://www.facebook.com/profile.php?id=100012014024197).



<https://www.facebook.com/profile.php?id=100012014024197>



http://www.example.com

}
```
**OUTPUT**

 [Do Duc Quan](https://www.facebook.com/profile.php?id=100012014024197).



<https://www.facebook.com/profile.php?id=100012014024197>



http://www.example.com

### 3.6 in đậm.

**MARDOWN**
```
This is really***very***important text.

```
**OUTPUT**

This is really***very***important text.

### 3.7. gạch ngang.

**MARDOWN**
```
~~The world is flat.~~ We now know that the world is round.

```
**OUTPUT**

~~The world is flat.~~ We now know that the world is round.




---
*danh mục tham khảo* 

[1] https://viblo.asia/p/markdown-for-newbie-n157G5wlRAje

[2] https://www.markdownguide.org/extended-syntax/
</p>








