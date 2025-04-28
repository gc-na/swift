<!--
Meta Description: # Câu Lệnh "else" trong Swift: Hướng Dẫn và Ví Dụ Sử Dụng ## Tóm Tắt Câu lệnh "else" trong Swift được sử dụng để xử lý các trường hợp không khớp với đ...
Meta Keywords: else, câu, lệnh, điều, kiện
-->

# Câu Lệnh "else" trong Swift: Hướng Dẫn và Ví Dụ Sử Dụng

## Tóm Tắt
Câu lệnh "else" trong Swift được sử dụng để xử lý các trường hợp không khớp với điều kiện đã cho trong câu lệnh "if". Điều này cho phép lập trình viên xác định các hành động khác nhau dựa trên kết quả của điều kiện.

## Tài Liệu
Câu lệnh "else" là một phần của cấu trúc điều kiện trong Swift, cho phép bạn mở rộng câu lệnh "if" để xử lý các tình huống khác nhau. Câu lệnh "else" được sử dụng khi điều kiện trong câu lệnh "if" không được thỏa mãn, giúp bạn thực hiện một đoạn mã thay thế.

### Cú Pháp
Cú pháp cơ bản của câu lệnh "else" trong Swift như sau:

```swift
if điều_kiện {
    // Mã sẽ được thực hiện nếu điều kiện đúng
} else {
    // Mã sẽ được thực hiện nếu điều kiện sai
}
```

### Chi Tiết
- Bạn có thể kết hợp câu lệnh "else" với câu lệnh "if let" hoặc "guard" để xử lý các trường hợp optional.
- Swift cũng hỗ trợ câu lệnh "else if" để kiểm tra nhiều điều kiện khác nhau.
- Câu lệnh "else" không yêu cầu điều kiện đi kèm; nó sẽ tự động được thực hiện nếu không có điều kiện nào trước đó được thỏa mãn.

## Ví Dụ
### Ví Dụ Cơ Bản
```swift
let số = 10

if số > 0 {
    print("Số dương")
} else {
    print("Số không dương")
}
```
Kết quả: "Số dương"

### Ví Dụ Với "else if"
```swift
let điểm = 75

if điểm >= 90 {
    print("Xuất sắc")
} else if điểm >= 75 {
    print("Khá")
} else {
    print("Cần cải thiện")
}
```
Kết quả: "Khá"

## Giải Thích
Một số lỗi thường gặp khi sử dụng câu lệnh "else":
- **Bỏ qua dấu ngoặc nhọn**: Nếu bạn chỉ có một dòng mã bên trong câu lệnh "if" hoặc "else", bạn có thể bỏ qua dấu ngoặc nhọn, nhưng điều này có thể gây nhầm lẫn khi thêm mã sau này.
- **Quên kiểm tra điều kiện**: Đảm bảo rằng điều kiện trong câu lệnh "if" là chính xác để tránh những vấn đề logic không mong muốn.
- **Sử dụng "else" mà không cần thiết**: Đôi khi, việc không cần có "else" có thể làm cho mã trở nên rõ ràng hơn. Hãy cân nhắc khi nào nên sử dụng nó.

## Tóm Tắt Một Dòng
Câu lệnh "else" trong Swift cho phép lập trình viên xử lý các tình huống không thỏa mãn điều kiện đã cho trong câu lệnh "if", giúp tạo ra mã linh hoạt và dễ hiểu.