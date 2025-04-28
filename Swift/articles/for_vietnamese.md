<!--
Meta Description: # Câu Lệnh "for" trong Swift: Cách Sử Dụng và Ví Dụ ## Tóm Tắt Câu lệnh "for" trong Swift cho phép lập trình viên lặp qua các phần tử của một dãy hoặc...
Meta Keywords: một, lệnh, swift, câu, trong
-->

# Câu Lệnh "for" trong Swift: Cách Sử Dụng và Ví Dụ

## Tóm Tắt
Câu lệnh "for" trong Swift cho phép lập trình viên lặp qua các phần tử của một dãy hoặc một khoảng số, giúp tối ưu hóa quá trình xử lý và quản lý dữ liệu.

## Tài Liệu
Câu lệnh "for" trong Swift được sử dụng để duyệt qua các phần tử trong một tập hợp, như mảng, từ điển, hoặc một khoảng số. Cú pháp cơ bản của câu lệnh "for" có thể được chia thành hai dạng chính: "for-in" và "for-where".

### Cú Pháp
1. **Duyệt qua dãy (Array)**:
   ```swift
   for item in array {
       // thực hiện hành động với item
   }
   ```

2. **Duyệt qua khoảng số (Range)**:
   ```swift
   for index in 1...5 {
       // thực hiện hành động với index
   }
   ```

3. **Sử dụng "where"**:
   ```swift
   for index in 1...10 where index % 2 == 0 {
       // chỉ thực hiện với các số chẵn
   }
   ```

### Mục Đích
Câu lệnh "for" giúp thực hiện các thao tác lặp lại một cách dễ dàng, cho phép làm việc với các tập hợp dữ liệu một cách hiệu quả, giảm thiểu mã lệnh cần viết.

## Ví Dụ
### Ví dụ 1: Duyệt qua một mảng
```swift
let fruits = ["Táo", "Cam", "Chuối"]
for fruit in fruits {
    print("Tôi thích \(fruit)")
}
```

### Ví dụ 2: Duyệt qua một khoảng số
```swift
for number in 1...5 {
    print("Số hiện tại là \(number)")
}
```

### Ví dụ 3: Sử dụng "where"
```swift
for number in 1...10 where number % 2 == 0 {
    print("Số chẵn: \(number)")
}
```

## Giải Thích
Khi sử dụng câu lệnh "for", lập trình viên cần lưu ý một số điểm quan trọng:
- **Biến tạm**: Biến được sử dụng trong câu lệnh "for" chỉ có thể được sử dụng trong phạm vi của câu lệnh đó.
- **Thay đổi dãy**: Nếu dãy thay đổi trong quá trình lặp, điều này có thể dẫn đến lỗi hoặc hành vi không mong muốn.
- **Kết thúc vòng lặp**: Đảm bảo rằng điều kiện kết thúc vòng lặp được xác định rõ ràng để tránh việc lặp vô hạn.

## Tóm Tắt Một Dòng
Câu lệnh "for" trong Swift cung cấp cách thức mạnh mẽ để lặp qua các tập hợp và khoảng số, giúp lập trình viên thao tác với dữ liệu một cách tối ưu.