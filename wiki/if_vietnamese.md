<!--
Meta Description: # Câu lệnh "if" trong Swift: Hướng dẫn và Ví dụ ## Tóm tắt Câu lệnh "if" trong Swift cho phép lập trình viên thực hiện các lệnh điều kiện dựa trên việ...
Meta Keywords: lệnh, câu, điều, swift, kiện
-->

# Câu lệnh "if" trong Swift: Hướng dẫn và Ví dụ

## Tóm tắt
Câu lệnh "if" trong Swift cho phép lập trình viên thực hiện các lệnh điều kiện dựa trên việc kiểm tra một biểu thức boolean. Đây là một trong những cấu trúc điều khiển cơ bản nhất, giúp kiểm soát luồng thực thi của chương trình.

## Tài liệu
Câu lệnh "if" là một công cụ quan trọng trong Swift, cho phép bạn thực hiện các khối mã chỉ khi một điều kiện nhất định được thỏa mãn. Cú pháp cơ bản của câu lệnh "if" như sau:

```swift
if điều_kiện {
    // Khối mã thực thi nếu điều kiện đúng
}
```

### Mục đích
Câu lệnh "if" được sử dụng để kiểm tra liệu một điều kiện có đúng hay không và thực thi mã liên quan nếu điều kiện đó đúng.

### Cách sử dụng
- Bạn có thể sử dụng câu lệnh "if" với một hoặc nhiều điều kiện.
- Swift hỗ trợ việc sử dụng "else if" và "else" để kiểm tra nhiều điều kiện khác nhau.

Cú pháp mở rộng:

```swift
if điều_kiện1 {
    // Khối mã nếu điều kiện1 đúng
} else if điều_kiện2 {
    // Khối mã nếu điều kiện2 đúng
} else {
    // Khối mã nếu tất cả các điều kiện trên đều sai
}
```

## Ví dụ
Dưới đây là một vài ví dụ đơn giản về cách sử dụng câu lệnh "if":

### Ví dụ 1: Câu lệnh "if" cơ bản
```swift
let số = 10

if số > 5 {
    print("Số lớn hơn 5")
}
```

### Ví dụ 2: Câu lệnh "if-else"
```swift
let số = 3

if số % 2 == 0 {
    print("Số chẵn")
} else {
    print("Số lẻ")
}
```

### Ví dụ 3: Câu lệnh "if-else if-else"
```swift
let điểm = 85

if điểm >= 90 {
    print("Xuất sắc")
} else if điểm >= 75 {
    print("Khá")
} else {
    print("Cần cải thiện")
}
```

## Giải thích
Một số điểm cần lưu ý khi sử dụng câu lệnh "if" trong Swift:

- **Kiểu dữ liệu**: Điều kiện trong câu lệnh "if" phải trả về giá trị boolean (true hoặc false).
- **Phép so sánh**: Hãy chắc chắn sử dụng đúng phép so sánh (==, !=, >, <, >=, <=) để tránh lỗi logic.
- **Nesting**: Bạn có thể lồng câu lệnh "if" bên trong các câu lệnh "if" khác, nhưng hãy cẩn thận để không làm cho mã trở nên khó đọc.

## Tóm tắt một dòng
Câu lệnh "if" trong Swift cho phép thực hiện các khối mã điều kiện dựa trên việc kiểm tra một biểu thức boolean, giúp kiểm soát luồng thực thi của chương trình.