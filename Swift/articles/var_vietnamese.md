<!--
Meta Description: # Từ khóa "var" trong Swift: Khai báo Biến Linh Hoạt ## Tóm tắt Từ khóa `var` trong Swift được sử dụng để khai báo biến có thể thay đổi giá trị trong ...
Meta Keywords: biến, giá, trị, khai, báo
-->

# Từ khóa "var" trong Swift: Khai báo Biến Linh Hoạt

## Tóm tắt
Từ khóa `var` trong Swift được sử dụng để khai báo biến có thể thay đổi giá trị trong thời gian thực thi của chương trình. Đây là một trong những thành phần cơ bản nhất trong ngôn ngữ lập trình Swift, giúp lập trình viên quản lý và thao tác với dữ liệu một cách linh hoạt.

## Tài liệu
### Mục đích
`var` cho phép bạn khai báo biến mà giá trị của nó có thể thay đổi sau khi đã được khởi tạo. Điều này rất quan trọng trong lập trình, vì nhiều tình huống yêu cầu giá trị của biến có thể thay đổi theo thời gian.

### Cách sử dụng
Để sử dụng `var`, bạn chỉ cần viết từ khóa `var`, theo sau là tên của biến và kiểu dữ liệu (nếu cần). Cú pháp cơ bản là:

```swift
var tenBien: KieuDuLieu = giaTriKhoiTao
```

- **tenBien**: Tên của biến mà bạn muốn khai báo.
- **KieuDuLieu**: (Tùy chọn) Kiểu dữ liệu của biến như `Int`, `String`, `Double`, v.v.
- **giaTriKhoiTao**: Giá trị khởi tạo cho biến.

### Chi tiết
- Biến được khai báo bằng `var` có thể thay đổi giá trị bằng cách gán giá trị mới cho nó.
- Swift có khả năng suy diễn kiểu dữ liệu, vì vậy bạn không cần phải chỉ định kiểu dữ liệu nếu giá trị khởi tạo rõ ràng.

## Ví dụ
```swift
// Khai báo biến mà không chỉ định kiểu
var ten: String = "Nguyễn Văn A"
print(ten) // Kết quả: Nguyễn Văn A

// Thay đổi giá trị của biến
ten = "Trần Thị B"
print(ten) // Kết quả: Trần Thị B

// Khai báo biến số nguyên
var tuoi: Int = 25
print(tuoi) // Kết quả: 25

// Thay đổi giá trị
tuoi = 30
print(tuoi) // Kết quả: 30
```

## Giải thích
- **Lưu ý về phạm vi**: Biến được khai báo với `var` có phạm vi tồn tại trong khối mã nơi nó được khai báo. Nếu bạn khai báo biến trong một hàm, nó sẽ không thể truy cập bên ngoài hàm đó.
- **Không thể khởi tạo biến không có giá trị**: Bạn không thể khai báo một biến mà không gán giá trị khởi đầu, bởi vì Swift yêu cầu tất cả các biến phải có giá trị khởi tạo trước khi sử dụng.
- **Tránh xung đột tên**: Đảm bảo rằng tên biến là duy nhất trong phạm vi của nó để tránh xung đột.

## Tóm tắt một dòng
Từ khóa `var` trong Swift cho phép bạn khai báo biến có thể thay đổi giá trị, hỗ trợ lập trình viên trong việc quản lý dữ liệu linh hoạt.