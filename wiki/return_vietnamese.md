<!--
Meta Description: # Lệnh "return" trong Swift: Cách sử dụng và ứng dụng ## Tóm tắt Lệnh `return` trong Swift được sử dụng để kết thúc một hàm và trả về giá trị từ hàm đ...
Meta Keywords: hàm, return, giá, trị, trả
-->

# Lệnh "return" trong Swift: Cách sử dụng và ứng dụng

## Tóm tắt
Lệnh `return` trong Swift được sử dụng để kết thúc một hàm và trả về giá trị từ hàm đó. Đây là một phần quan trọng trong việc xử lý các giá trị trả về và điều khiển luồng thực thi trong chương trình.

## Tài liệu
Lệnh `return` trong Swift có mục đích chính là trả về giá trị từ một hàm hoặc kết thúc hàm mà không trả giá trị nào. Khi hàm được gọi, lệnh `return` cho phép chương trình biết rằng hàm đã hoàn thành công việc và có thể gửi giá trị trở lại cho phần mã đang gọi hàm.

### Cách sử dụng
- **Trả về giá trị**: Nếu hàm được định nghĩa để trả về một kiểu dữ liệu cụ thể, bạn cần sử dụng `return` để trả về giá trị tương ứng.
- **Kết thúc hàm**: Nếu bạn chỉ muốn kết thúc hàm mà không cần trả về giá trị, bạn có thể sử dụng `return` mà không có giá trị đi kèm.

### Chi tiết
- Lệnh `return` phải được đặt trong thân hàm.
- Nếu hàm không yêu cầu trả về giá trị (kiểu `Void`), bạn có thể sử dụng `return` mà không cần giá trị.
- Bạn có thể có nhiều lệnh `return` trong một hàm, cho phép kiểm soát luồng thực thi.

## Ví dụ
### Ví dụ 1: Trả về giá trị
```swift
func tinhTong(a: Int, b: Int) -> Int {
    return a + b
}

let ketQua = tinhTong(a: 5, b: 10)
print(ketQua) // Kết quả: 15
```

### Ví dụ 2: Kết thúc hàm
```swift
func kiemTraSoDuong(a: Int) {
    if a < 0 {
        return // Kết thúc hàm nếu a không phải là số dương
    }
    print("\(a) là số dương.")
}

kiemTraSoDuong(a: -5) // Không in gì ra
kiemTraSoDuong(a: 5)  // Kết quả: 5 là số dương.
```

## Giải thích
Một số vấn đề thường gặp với lệnh `return`:
- **Thiếu giá trị trả về**: Nếu hàm yêu cầu một giá trị trả về nhưng không có lệnh `return` hợp lệ, bạn sẽ nhận được lỗi biên dịch.
- **Sử dụng `return` sai vị trí**: Đảm bảo rằng lệnh `return` nằm trong thân hàm. Nếu nó nằm ngoài, Swift sẽ báo lỗi.
- **Nhiều lệnh `return`**: Mặc dù có thể có nhiều lệnh `return` trong một hàm, nhưng cần chú ý để không làm cho mã trở nên khó đọc.

## Tóm tắt một dòng
Lệnh `return` trong Swift là cách để kết thúc hàm và trả về giá trị, giúp kiểm soát luồng thực thi trong chương trình.