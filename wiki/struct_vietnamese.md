<!--
Meta Description: # Struct trong Swift: Cấu trúc Dữ liệu Linh hoạt và Hiệu quả ## Tóm Tắt Trong ngôn ngữ lập trình Swift, `struct` là một loại cấu trúc dữ liệu mạnh mẽ ...
Meta Keywords: struct, một, trong, liệu, thức
-->

# Struct trong Swift: Cấu trúc Dữ liệu Linh hoạt và Hiệu quả

## Tóm Tắt
Trong ngôn ngữ lập trình Swift, `struct` là một loại cấu trúc dữ liệu mạnh mẽ cho phép bạn định nghĩa kiểu dữ liệu tùy chỉnh với các thuộc tính và phương thức riêng. `struct` được sử dụng rộng rãi trong Swift để tổ chức mã và quản lý dữ liệu một cách hiệu quả.

## Tài Liệu
### Mục Đích
`struct` trong Swift được thiết kế để tạo ra các kiểu dữ liệu tùy chỉnh mà có thể chứa các thuộc tính (biến) và phương thức (hàm). Chúng cung cấp một cách tiếp cận mạnh mẽ và an toàn để làm việc với dữ liệu, cho phép bạn tạo ra các đối tượng phức tạp một cách đơn giản.

### Cách Sử Dụng
Để định nghĩa một `struct`, bạn sử dụng từ khóa `struct`, sau đó là tên của cấu trúc, và bên trong là các thuộc tính và phương thức mà bạn muốn định nghĩa. Dưới đây là cú pháp cơ bản:

```swift
struct TênCấuTrúc {
    var thuộcTính1: Kiểu
    var thuộcTính2: Kiểu

    func phươngThức() {
        // Thực hiện một hành động
    }
}
```

### Chi Tiết
- `struct` có tính chất giá trị, điều này có nghĩa là khi bạn sao chép một `struct`, một bản sao hoàn toàn mới sẽ được tạo ra.
- `struct` có thể có các phương thức, khởi tạo, và có thể tuân theo các giao thức (protocol).
- Bạn có thể sử dụng `mutating` để thay đổi thuộc tính trong phương thức của `struct`.

## Ví Dụ
### Ví dụ cơ bản về `struct`

```swift
struct HinhTron {
    var banKinh: Double

    var dienTich: Double {
        return Double.pi * banKinh * banKinh
    }

    mutating func thayDoiBanKinh(moiBanKinh: Double) {
        banKinh = moiBanKinh
    }
}

// Sử dụng cấu trúc HinhTron
var hinhTron = HinhTron(banKinh: 5)
print(hinhTron.dienTich) // In ra diện tích

hinhTron.thayDoiBanKinh(moiBanKinh: 10)
print(hinhTron.dienTich) // In ra diện tích mới
```

## Giải Thích
- **Cấu trúc giá trị**: Do `struct` là kiểu giá trị, việc thay đổi một bản sao của `struct` sẽ không ảnh hưởng đến bản gốc, điều này có thể gây ra sự nhầm lẫn nếu không hiểu rõ.
- **Phương thức `mutating`**: Phương thức có từ khóa `mutating` là cần thiết khi bạn muốn thay đổi thuộc tính của `struct` từ bên trong phương thức.
- **So sánh với `class`**: Khác với `class`, `struct` không hỗ trợ kế thừa, nhưng chúng có ưu điểm là an toàn hơn trong việc xử lý dữ liệu.

## Tóm Tắt Một Câu
`struct` trong Swift là một cách mạnh mẽ và linh hoạt để định nghĩa các kiểu dữ liệu tùy chỉnh, hỗ trợ tính chất giá trị và cung cấp một cách tiếp cận an toàn để quản lý dữ liệu trong ứng dụng.