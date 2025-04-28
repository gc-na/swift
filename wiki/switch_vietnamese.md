<!--
Meta Description: # Câu lệnh switch trong Swift: Hướng Dẫn Chi Tiết và Ví Dụ Cụ Thể ## Tóm tắt Câu lệnh `switch` trong Swift là một công cụ mạnh mẽ cho phép kiểm tra mộ...
Meta Keywords: case, switch, bạn, print, swift
-->

# Câu lệnh switch trong Swift: Hướng Dẫn Chi Tiết và Ví Dụ Cụ Thể

## Tóm tắt
Câu lệnh `switch` trong Swift là một công cụ mạnh mẽ cho phép kiểm tra một giá trị và thực hiện các hành động khác nhau dựa trên giá trị đó. Nó hỗ trợ nhiều kiểu so sánh và cho phép xử lý các trường hợp phức tạp một cách dễ dàng.

## Tài liệu
Câu lệnh `switch` trong Swift được sử dụng để so sánh một giá trị với nhiều trường hợp (case). Đặc biệt, `switch` trong Swift có một số tính năng nổi bật như:

- **Không yêu cầu break**: Mỗi case trong `switch` tự động kết thúc, vì vậy không cần phải sử dụng từ khóa `break` như trong nhiều ngôn ngữ khác.
- **Hỗ trợ nhiều kiểu dữ liệu**: `switch` có thể kiểm tra các giá trị kiểu số nguyên, chuỗi, và thậm chí các kiểu dữ liệu tùy chỉnh.
- **Phạm vi và điều kiện**: Bạn có thể sử dụng các thuật toán để kiểm tra các phạm vi giá trị hoặc điều kiện phức tạp trong các case.

### Cú pháp cơ bản
```swift
switch value {
case pattern1:
    // Thực hiện hành động cho pattern1
case pattern2:
    // Thực hiện hành động cho pattern2
default:
    // Hành động mặc định nếu không khớp với bất kỳ pattern nào
}
```

## Ví dụ
### Ví dụ 1: So sánh số nguyên
```swift
let number = 3

switch number {
case 1:
    print("Số một")
case 2:
    print("Số hai")
case 3:
    print("Số ba")
default:
    print("Số khác")
}
```

### Ví dụ 2: Sử dụng điều kiện
```swift
let age = 20

switch age {
case 0..<18:
    print("Bạn là trẻ em.")
case 18..<65:
    print("Bạn là người trưởng thành.")
default:
    print("Bạn là người cao tuổi.")
}
```

### Ví dụ 3: So sánh chuỗi
```swift
let fruit = "Táo"

switch fruit {
case "Cam":
    print("Bạn thích cam.")
case "Táo":
    print("Bạn thích táo.")
default:
    print("Bạn thích trái cây khác.")
}
```

## Giải thích
- **Tránh nhầm lẫn với `if`**: Mặc dù bạn có thể sử dụng `if` để thực hiện các so sánh, nhưng `switch` thường dễ đọc hơn khi có nhiều case khác nhau.
- **Không kiểm tra giá trị mặc định**: Nếu bạn không cung cấp case `default`, chương trình sẽ báo lỗi khi không có case nào khớp với giá trị được kiểm tra.
- **Hỗ trợ chứa nhiều case**: Bạn có thể nhóm nhiều giá trị trong một case bằng cách sử dụng dấu phẩy.
  
```swift
let grade = "B"

switch grade {
case "A", "B":
    print("Bạn đã đỗ.")
case "C":
    print("Bạn cần cải thiện.")
default:
    print("Bạn đã không đỗ.")
}
```

## Tóm tắt một dòng
Câu lệnh `switch` trong Swift cung cấp một cách dễ dàng và hiệu quả để kiểm tra và xử lý nhiều trường hợp khác nhau dựa trên giá trị đầu vào.