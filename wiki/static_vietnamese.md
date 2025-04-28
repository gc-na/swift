<!--
Meta Description: # Tìm hiểu về từ khóa "static" trong Swift ## Tóm tắt Từ khóa `static` trong Swift được sử dụng để định nghĩa các thuộc tính và phương thức có thể đượ...
Meta Keywords: một, static, swift, thuộc, tính
-->

# Tìm hiểu về từ khóa "static" trong Swift

## Tóm tắt
Từ khóa `static` trong Swift được sử dụng để định nghĩa các thuộc tính và phương thức có thể được truy cập mà không cần khởi tạo một thể hiện của lớp hoặc cấu trúc.

## Tài liệu
Từ khóa `static` là một phần quan trọng trong Swift, cho phép lập trình viên tạo ra các thuộc tính và phương thức của lớp hoặc cấu trúc mà không cần phải tạo ra một đối tượng. Điều này giúp tiết kiệm bộ nhớ và làm cho mã trở nên gọn gàng hơn. 

### Mục đích
- Để định nghĩa thuộc tính và phương thức chung cho tất cả các thể hiện của một lớp hoặc cấu trúc.
- Giúp tối ưu hóa hiệu suất bằng cách loại bỏ nhu cầu khởi tạo đối tượng.

### Cách sử dụng
- Để định nghĩa một thuộc tính tĩnh, bạn sử dụng cú pháp: 
  ```swift
  static var propertyName: Type
  ```

- Để định nghĩa một phương thức tĩnh, bạn sử dụng cú pháp:
  ```swift
  static func methodName() {
  }
  ```

## Ví dụ
Dưới đây là một số ví dụ về cách sử dụng từ khóa `static` trong Swift:

### Ví dụ 1: Thuộc tính tĩnh
```swift
class Math {
    static let pi = 3.14159
}

print(Math.pi) // Kết quả: 3.14159
```

### Ví dụ 2: Phương thức tĩnh
```swift
class Calculator {
    static func add(a: Int, b: Int) -> Int {
        return a + b
    }
}

let result = Calculator.add(a: 5, b: 10) // Kết quả: 15
```

## Giải thích
### Cạm bẫy thường gặp
- Phương thức tĩnh không thể truy cập vào các thuộc tính không tĩnh. Điều này có thể gây nhầm lẫn cho những lập trình viên mới khi họ cố gắng sử dụng thuộc tính của một thể hiện trong một phương thức tĩnh.

### Lưu ý thêm
- Bạn có thể sử dụng từ khóa `static` với các cấu trúc (struct) cũng như lớp (class).
- Nếu bạn cần một thuộc tính hoặc phương thức mà có thể được ghi đè trong các lớp con, hãy sử dụng từ khóa `class` thay vì `static`.

## Tóm tắt một dòng
Từ khóa `static` trong Swift cho phép định nghĩa thuộc tính và phương thức chung cho tất cả các thể hiện mà không cần khởi tạo một đối tượng.