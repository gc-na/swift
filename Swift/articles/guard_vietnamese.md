<!--
Meta Description: # Từ Khóa "guard" trong Swift: Cách Sử Dụng và Ý Nghĩa ## Tóm tắt Từ khóa `guard` trong Swift được sử dụng để kiểm tra điều kiện và đảm bảo rằng các đ...
Meta Keywords: guard, điều, kiện, trong, không
-->

# Từ Khóa "guard" trong Swift: Cách Sử Dụng và Ý Nghĩa

## Tóm tắt
Từ khóa `guard` trong Swift được sử dụng để kiểm tra điều kiện và đảm bảo rằng các điều kiện đó được thoả mãn trước khi tiếp tục thực hiện đoạn mã. Nếu điều kiện không được thoả mãn, khối lệnh `guard` sẽ buộc phải thoát khỏi phạm vi hiện tại.

## Tài liệu
`guard` là một từ khóa quan trọng trong Swift, giúp cải thiện khả năng đọc và tính rõ ràng của mã nguồn. Nó cho phép lập trình viên thực hiện các kiểm tra điều kiện ngay lập tức và xử lý các trường hợp không hợp lệ chỉ trong một lần. 

### Mục đích
Mục đích chính của `guard` là để kiểm tra các điều kiện mà nếu không đạt sẽ dẫn đến việc mã không thể tiếp tục. Nói cách khác, `guard` giúp bảo đảm rằng mọi thứ đều hợp lệ trước khi tiếp tục xử lý.

### Cách sử dụng
Cú pháp cơ bản của `guard` như sau:

```swift
guard điều_kiện else {
    // Xử lý khi điều kiện không đạt
    return // hoặc throw, break tùy theo ngữ cảnh
}
```

Các điều kiện có thể là bất kỳ biểu thức nào trả về giá trị boolean. Nếu điều kiện là `false`, đoạn mã trong khối `else` sẽ được thực thi và chương trình sẽ rời khỏi phạm vi hiện tại.

## Ví dụ
Dưới đây là một số ví dụ cơ bản về cách sử dụng `guard` trong Swift.

### Ví dụ 1: Kiểm tra giá trị không nil

```swift
func printName(name: String?) {
    guard let unwrappedName = name else {
        print("Tên không hợp lệ")
        return
    }
    print("Tên là: \(unwrappedName)")
}
```

### Ví dụ 2: Kiểm tra số lượng phần tử trong mảng

```swift
func processArray(arr: [Int]) {
    guard arr.count > 0 else {
        print("Mảng rỗng")
        return
    }
    print("Mảng có \(arr.count) phần tử.")
}
```

## Giải thích
Mặc dù `guard` rất hữu ích, có một số điểm cần lưu ý:

1. **Phạm vi của biến**: Biến được khai báo trong khối `guard let` sẽ có phạm vi tồn tại từ khối lệnh `guard` trở đi. Điều này có nghĩa là bạn có thể sử dụng biến đó ở mọi nơi sau `guard`.

2. **Khối lệnh `else` là bắt buộc**: Mỗi câu lệnh `guard` phải có khối lệnh `else`. Nếu không, trình biên dịch sẽ báo lỗi.

3. **Không sử dụng `guard` cho các điều kiện đơn giản**: Một số lập trình viên có thể sử dụng `guard` cho các kiểm tra không cần thiết. Trong trường hợp này, `if` có thể là lựa chọn hợp lý hơn.

## Tóm tắt một câu
Từ khóa `guard` trong Swift giúp kiểm tra điều kiện một cách hiệu quả và cải thiện khả năng đọc mã nguồn bằng cách đảm bảo các điều kiện cần thiết được thoả mãn trước khi tiếp tục thực hiện các lệnh.