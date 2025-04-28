<!--
Meta Description: # Câu Lệnh "while" Trong Swift: Cách Sử Dụng và Ví Dụ Cụ Thể ## Tóm Tắt Câu lệnh "while" trong Swift cho phép lặp lại một đoạn mã miễn là điều kiện đư...
Meta Keywords: lệnh, điều, kiện, while, câu
-->

# Câu Lệnh "while" Trong Swift: Cách Sử Dụng và Ví Dụ Cụ Thể

## Tóm Tắt
Câu lệnh "while" trong Swift cho phép lặp lại một đoạn mã miễn là điều kiện được chỉ định là đúng. Đây là một trong những cấu trúc điều khiển quan trọng giúp quản lý luồng điều kiện trong lập trình.

## Tài Liệu
Câu lệnh "while" được sử dụng để thực hiện một khối lệnh nhiều lần cho đến khi điều kiện kiểm tra trở thành sai. Cú pháp cơ bản của câu lệnh "while" như sau:

```swift
while điều_kiện {
    // Khối lệnh sẽ được lặp lại
}
```

### Mục Đích
Câu lệnh "while" giúp lập trình viên kiểm soát luồng chương trình và thực hiện lặp đi lặp lại một khối mã cho đến khi điều kiện không còn đúng.

### Cách Sử Dụng
- **Điều kiện**: Là một biểu thức boolean; khi điều kiện này là đúng, khối lệnh bên trong sẽ được thực thi.
- **Khối lệnh**: Các lệnh bên trong dấu ngoặc nhọn sẽ được thực thi cho đến khi điều kiện trở thành sai.

## Ví Dụ
### Ví Dụ Cơ Bản
```swift
var số = 0

while số < 5 {
    print("Số hiện tại là \(số)")
    số += 1
}
```
**Kết quả**:
```
Số hiện tại là 0
Số hiện tại là 1
Số hiện tại là 2
Số hiện tại là 3
Số hiện tại là 4
```

### Ví Dụ Với Mảng
```swift
let mảng = [1, 2, 3, 4, 5]
var chỉ số = 0

while chỉ số < mảng.count {
    print("Phần tử tại chỉ số \(chỉ số) là \(mảng[chỉ số])")
    chỉ số += 1
}
```

## Giải Thích
### Những Cạm Bẫy Thường Gặp
- **Vòng Lặp Vô Hạn**: Nếu điều kiện trong câu lệnh "while" không bao giờ trở thành sai, chương trình sẽ rơi vào vòng lặp vô hạn. Điều này có thể gây treo ứng dụng hoặc tiêu tốn tài nguyên.
- **Thay Đổi Điều Kiện**: Đảm bảo rằng điều kiện sẽ thay đổi trong khối lệnh để tránh vòng lặp vô hạn.
- **Kiểm Tra Điều Kiện**: Có thể sử dụng câu lệnh "repeat-while" để kiểm tra điều kiện sau khi thực thi khối lệnh ít nhất một lần.

## Tóm Tắt Một Câu
Câu lệnh "while" trong Swift cho phép lập trình viên lặp lại một khối mã miễn là điều kiện kiểm tra là đúng, giúp kiểm soát luồng chương trình hiệu quả.