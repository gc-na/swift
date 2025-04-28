<!--
Meta Description: # Lớp trong Swift: Tìm Hiểu về Khái Niệm và Cách Sử Dụng ## Tóm Tắt Trong Swift, lớp (class) là một cấu trúc cơ bản cho phép lập trình viên định nghĩa...
Meta Keywords: lớp, một, swift, trong, các
-->

# Lớp trong Swift: Tìm Hiểu về Khái Niệm và Cách Sử Dụng

## Tóm Tắt
Trong Swift, lớp (class) là một cấu trúc cơ bản cho phép lập trình viên định nghĩa các đối tượng với thuộc tính và phương thức, giúp tổ chức và quản lý mã hiệu quả hơn.

## Tài Liệu
### Mục Đích
Lớp trong Swift được sử dụng để tạo ra các đối tượng có thể chứa dữ liệu và chức năng. Mỗi lớp có thể có các thuộc tính (properties) để lưu trữ trạng thái và phương thức (methods) để thực hiện các hành động.

### Cách Sử Dụng
Để định nghĩa một lớp trong Swift, bạn sử dụng từ khóa `class`, theo sau là tên lớp và một khối mã chứa các thuộc tính và phương thức. Ví dụ:

```swift
class Người {
    var tên: String
    var tuổi: Int
    
    init(tên: String, tuổi: Int) {
        self.tên = tên
        self.tuổi = tuổi
    }
    
    func giớiThiệu() -> String {
        return "Xin chào, tôi là \(tên) và tôi \(tuổi) tuổi."
    }
}
```

### Chi Tiết
- **Khởi tạo**: Mỗi lớp có thể có một hoặc nhiều hàm khởi tạo (initializer) để thiết lập trạng thái ban đầu cho đối tượng.
- **Kế thừa**: Swift hỗ trợ kế thừa lớp, cho phép bạn tạo ra một lớp mới từ một lớp đã tồn tại, kế thừa thuộc tính và phương thức.
- **Phạm vi truy cập**: Swift cung cấp các mức độ truy cập khác nhau (public, internal, fileprivate, private) cho các lớp và thành phần của chúng, giúp kiểm soát khả năng truy cập.

## Ví Dụ
### Định Nghĩa và Sử Dụng Lớp
```swift
class XeHơi {
    var màu: String
    var tốcĐộ: Int
    
    init(màu: String, tốcĐộ: Int) {
        self.màu = màu
        self.tốcĐộ = tốcĐộ
    }
    
    func giaTăngTốcĐộ(mứcTăng: Int) {
        tốcĐộ += mứcTăng
    }
}

let xe1 = XeHơi(màu: "Đỏ", tốcĐộ: 0)
xe1.giaTăngTốcĐộ(mứcTăng: 50)
print("Tốc độ hiện tại: \(xe1.tốcĐộ) km/h")
```

## Giải Thích
- **Khó khăn phổ biến**: Một số lập trình viên mới có thể gặp khó khăn trong việc hiểu sự khác biệt giữa lớp và cấu trúc (struct). Một điểm khác biệt lớn là lớp hỗ trợ kế thừa, trong khi cấu trúc không.
- **Tham chiếu và giá trị**: Lớp được truyền theo tham chiếu, nghĩa là khi bạn gán một đối tượng lớp cho một biến khác, cả hai biến đều tham chiếu đến cùng một đối tượng trong bộ nhớ.
- **Xử lý bộ nhớ**: Swift sử dụng quản lý bộ nhớ tự động (ARC - Automatic Reference Counting) để theo dõi và quản lý bộ nhớ sử dụng cho các đối tượng lớp.

## Tóm Tắt Một Câu
Lớp trong Swift là một công cụ mạnh mẽ cho phép lập trình viên định nghĩa đối tượng với thuộc tính và phương thức, hỗ trợ việc tổ chức mã dễ dàng hơn.