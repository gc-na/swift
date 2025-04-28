<!--
Meta Description: # Mở Rộng (Extension) trong Swift: Tính Năng Quan Trọng cho Lập Trình Viên ## Tóm Tắt Mở rộng (extension) trong Swift cho phép bạn mở rộng chức năng c...
Meta Keywords: rộng, liệu, kiểu, thức, tính
-->

# Mở Rộng (Extension) trong Swift: Tính Năng Quan Trọng cho Lập Trình Viên

## Tóm Tắt
Mở rộng (extension) trong Swift cho phép bạn mở rộng chức năng của các kiểu dữ liệu hiện có mà không cần phải thay đổi mã nguồn gốc. Điều này giúp bạn thêm phương thức, thuộc tính, và thậm chí tuân thủ các giao thức cho các kiểu dữ liệu hiện có.

## Tài Liệu
### Mục Đích
Mở rộng được sử dụng để mở rộng chức năng của các kiểu dữ liệu, chẳng hạn như lớp, cấu trúc, enum, hoặc giao thức. Điều này rất hữu ích khi bạn muốn thêm các phương thức hoặc thuộc tính mà không muốn tạo lại kiểu dữ liệu hoặc thay đổi mã nguồn gốc.

### Cách Sử Dụng
Để tạo một mở rộng trong Swift, bạn sử dụng từ khóa `extension` theo sau là tên kiểu dữ liệu mà bạn muốn mở rộng. Dưới đây là cú pháp cơ bản:

```swift
extension TênKiểu {
    // Thêm thuộc tính hoặc phương thức tại đây
}
```

### Chi Tiết
- Mở rộng có thể thêm các thuộc tính tính toán, phương thức, và tuân thủ giao thức cho kiểu dữ liệu.
- Bạn không thể thêm thuộc tính lưu trữ mới cho kiểu dữ liệu.
- Mở rộng có thể được sử dụng với bất kỳ kiểu dữ liệu nào, bao gồm cả kiểu dữ liệu chuẩn của Swift và kiểu dữ liệu do người dùng định nghĩa.

## Ví dụ
### Ví Dụ 1: Thêm Phương Thức vào Một Kiểu Dữ Liệu
```swift
extension Int {
    func nhânHai() -> Int {
        return self * 2
    }
}

let số = 5
print(số.nhânHai()) // Kết quả: 10
```

### Ví Dụ 2: Thêm Thuộc Tính Tính Toán
```swift
extension String {
    var làChữHoa: Bool {
        return self == self.uppercased()
    }
}

let chuoi = "HELLO"
print(chuoi.làChữHoa) // Kết quả: true
```

### Ví Dụ 3: Tuân Thủ Giao Thức
```swift
protocol MôTả {
    var môTả: String { get }
}

extension Int: MôTả {
    var môTả: String {
        return "Số nguyên: \(self)"
    }
}

let sốNguyên = 10
print(sốNguyên.môTả) // Kết quả: Số nguyên: 10
```

## Giải Thích
- **Cái Bẫy Thường Gặp**: Một số lập trình viên có thể nhầm lẫn rằng mở rộng cho phép thêm thuộc tính lưu trữ, nhưng điều này là không đúng. Bạn chỉ có thể thêm thuộc tính tính toán.
- **Giao Thức**: Khi mở rộng một kiểu dữ liệu để tuân thủ một giao thức, hãy nhớ rằng bạn cần cung cấp tất cả các yêu cầu của giao thức đó.
- **Mở Rộng Lớp**: Nếu bạn mở rộng một lớp, bạn không thể ghi đè các phương thức đã có trong lớp đó thông qua mở rộng.

## Tóm Lại
Mở rộng (extension) trong Swift là một công cụ mạnh mẽ giúp bạn mở rộng chức năng của các kiểu dữ liệu mà không cần phải thay đổi mã nguồn gốc, mang lại sự linh hoạt và khả năng tổ chức tốt hơn trong lập trình.