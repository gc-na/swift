<!--
Meta Description: # Tìm Hiểu Về Hàm `func` Trong Swift ## Tóm Tắt Hàm `func` trong Swift là một cấu trúc cơ bản cho phép lập trình viên định nghĩa các khối mã có thể đư...
Meta Keywords: hàm, swift, func, thể, dụng
-->

# Tìm Hiểu Về Hàm `func` Trong Swift

## Tóm Tắt
Hàm `func` trong Swift là một cấu trúc cơ bản cho phép lập trình viên định nghĩa các khối mã có thể được gọi để thực hiện các tác vụ cụ thể. Việc sử dụng hàm giúp mã nguồn trở nên rõ ràng và dễ bảo trì hơn.

## Tài Liệu
Hàm (`func`) trong Swift được sử dụng để định nghĩa một khối mã có thể được thực thi nhiều lần. Mỗi hàm có thể nhận tham số đầu vào và trả về một giá trị. Cú pháp cơ bản của hàm trong Swift như sau:

```swift
func tênHàm(thamSố1: Kiểu1, thamSố2: Kiểu2) -> KiểuTrảVề {
    // Khối mã thực thi
}
```

### Mục Đích
- **Tổ chức mã:** Giúp chia nhỏ mã nguồn thành các phần dễ quản lý.
- **Tái sử dụng:** Có thể gọi lại nhiều lần mà không cần viết lại mã.
- **Chia sẻ chức năng:** Có thể sử dụng trong nhiều phần khác nhau của ứng dụng.

### Cách Sử Dụng
Để sử dụng hàm, bạn chỉ cần gọi tên hàm và truyền các tham số cần thiết. Ví dụ:

```swift
func tinhTong(a: Int, b: Int) -> Int {
    return a + b
}

let ketQua = tinhTong(a: 5, b: 10) // ketQua sẽ là 15
```

## Ví Dụ
Dưới đây là một số ví dụ cơ bản về cách định nghĩa và gọi hàm trong Swift:

### Ví Dụ 1: Hàm không có tham số và không trả về giá trị
```swift
func chao() {
    print("Xin chào!")
}

chao() // Kết quả: Xin chào!
```

### Ví Dụ 2: Hàm có tham số và trả về giá trị
```swift
func tinhHieu(a: Int, b: Int) -> Int {
    return a - b
}

let hieu = tinhHieu(a: 20, b: 5) // hieu sẽ là 15
```

### Ví Dụ 3: Hàm có tham số mặc định
```swift
func chaoTen(ten: String = "Bạn") {
    print("Xin chào, \(ten)!")
}

chaoTen() // Kết quả: Xin chào, Bạn!
chaoTen(ten: "Nam") // Kết quả: Xin chào, Nam!
```

## Giải Thích
Khi làm việc với hàm trong Swift, có một số điểm cần lưu ý:

- **Tham số và Kiểu trả về:** Đảm bảo rằng bạn định nghĩa đúng kiểu dữ liệu cho các tham số và giá trị trả về. Swift là ngôn ngữ kiểu tĩnh, do đó, việc không đúng kiểu có thể gây lỗi biên dịch.
- **Hàm không trả về giá trị:** Nếu một hàm không trả về giá trị, bạn có thể bỏ qua phần `-> KiểuTrảVề`.
- **Tham số mặc định:** Sử dụng tham số mặc định có thể giúp bạn tạo ra các hàm linh hoạt hơn.

## Tóm Tắt Một Dòng
Hàm `func` trong Swift là công cụ thiết yếu để định nghĩa và tổ chức mã, cho phép tái sử dụng và thực hiện các tác vụ một cách hiệu quả.