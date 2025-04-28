<!--
Meta Description: # Khởi tạo trong Swift: Tìm Hiểu về Lệnh `init` ## Tóm tắt Trong Swift, `init` là từ khóa được sử dụng để định nghĩa các hàm khởi tạo cho các lớp và c...
Meta Keywords: tạo, khởi, hàm, một, lớp
-->

# Khởi tạo trong Swift: Tìm Hiểu về Lệnh `init`

## Tóm tắt
Trong Swift, `init` là từ khóa được sử dụng để định nghĩa các hàm khởi tạo cho các lớp và cấu trúc. Hàm khởi tạo cho phép bạn thiết lập trạng thái ban đầu cho một đối tượng khi nó được tạo ra.

## Tài liệu
### Mục đích
Hàm khởi tạo (`init`) trong Swift được sử dụng để thiết lập giá trị khởi tạo cho các thuộc tính của một lớp hoặc cấu trúc. Mỗi lớp hoặc cấu trúc phải có ít nhất một hàm khởi tạo, trừ khi tất cả các thuộc tính có giá trị mặc định.

### Cách sử dụng
Hàm khởi tạo có thể có tham số và có thể trả về giá trị. Bạn có thể định nghĩa nhiều hàm khởi tạo cho cùng một lớp hoặc cấu trúc, cho phép tạo đối tượng với các trạng thái khác nhau. Dưới đây là cú pháp cơ bản:

```swift
init(parameter1: Type1, parameter2: Type2) {
    // Khởi tạo các thuộc tính
}
```

### Chi tiết
- **Tham số**: Hàm khởi tạo có thể có nhiều tham số để nhận giá trị và thiết lập cho các thuộc tính.
- **Hàm khởi tạo mặc định**: Nếu không định nghĩa hàm khởi tạo nào, Swift sẽ tự động tạo một hàm khởi tạo mặc định.
- **Hàm khởi tạo ủy quyền**: Một hàm khởi tạo có thể gọi một hàm khởi tạo khác trong cùng một lớp, giúp giảm thiểu mã lặp lại.

## Ví dụ
Dưới đây là một ví dụ đơn giản về cách sử dụng `init` trong một lớp:

```swift
class Dog {
    var name: String
    var age: Int

    // Hàm khởi tạo
    init(name: String, age: Int) {
        self.name = name
        self.age = age
    }
}

// Tạo một đối tượng Dog
let myDog = Dog(name: "Buddy", age: 3)
print("Tên: \(myDog.name), Tuổi: \(myDog.age)")
```

## Giải thích
- **Lỗi phổ biến**: Một số lập trình viên có thể quên gọi `self` khi thiết lập các thuộc tính trong hàm khởi tạo, dẫn đến lỗi biên dịch.
- **Hàm khởi tạo không trả về giá trị**: Hàm khởi tạo không có kiểu trả về; bạn chỉ cần sử dụng từ khóa `init`.
- **Không thể khởi tạo trong một lớp con nếu không gọi hàm khởi tạo của lớp cha**: Khi kế thừa, lớp con cần gọi hàm khởi tạo của lớp cha nếu lớp cha không có hàm khởi tạo mặc định.

## Tóm tắt một dòng
Hàm khởi tạo `init` trong Swift là công cụ thiết lập giá trị ban đầu cho các thuộc tính của lớp hoặc cấu trúc khi đối tượng được tạo ra.