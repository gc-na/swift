<!--
Meta Description: # Hiểu Về Từ Khóa "self" Trong Swift ## Tóm Tắt Từ khóa "self" trong Swift được sử dụng để tham chiếu đến đối tượng hiện tại của lớp hoặc cấu trúc, gi...
Meta Keywords: self, trong, dụng, các, đối
-->

# Hiểu Về Từ Khóa "self" Trong Swift

## Tóm Tắt
Từ khóa "self" trong Swift được sử dụng để tham chiếu đến đối tượng hiện tại của lớp hoặc cấu trúc, giúp phân biệt giữa các thuộc tính và phương thức của đối tượng với các biến và tham số khác.

## Tài Liệu
Từ khóa "self" trong Swift là một phần quan trọng trong lập trình hướng đối tượng. Nó được sử dụng trong các phương thức của lớp hoặc cấu trúc để chỉ rõ rằng bạn đang làm việc với các thuộc tính hoặc phương thức của đối tượng hiện tại.

### Mục Đích
- **Phân Biệt**: "self" giúp phân biệt giữa các tham số của phương thức và các thuộc tính của đối tượng khi chúng có tên giống nhau.
- **Truy Cập**: Nó cho phép bạn truy cập các thuộc tính và phương thức của đối tượng hiện tại từ bên trong phương thức.

### Cách Sử Dụng
- Trong một phương thức, bạn có thể sử dụng "self" để gọi các thuộc tính hoặc phương thức của đối tượng.
- "self" có thể được sử dụng trong các khối mã, như closures, để giữ tham chiếu đến đối tượng.

## Ví Dụ
### Ví Dụ 1: Sử Dụng "self" Trong Phương Thức
```swift
class Người {
    var tên: String
    
    init(tên: String) {
        self.tên = tên // Sử dụng self để phân biệt giữa tham số và thuộc tính
    }
    
    func chào() {
        print("Xin chào, \(self.tên)") // self không bắt buộc nhưng giúp rõ ràng hơn
    }
}

let người = Người(tên: "An")
người.chào() // Kết quả: Xin chào, An
```

### Ví Dụ 2: Sử Dụng "self" Trong Closure
```swift
class Bảng {
    var số: Int = 0
    
    lazy var tăngSố: () -> Void = {
        self.số += 1 // self được sử dụng để truy cập thuộc tính của đối tượng
    }
}

let bảng = Bảng()
bảng.tăngSố()
print(bảng.số) // Kết quả: 1
```

## Giải Thích
### Những Lỗi Thường Gặp
- **Thiếu "self"**: Khi bạn có một tham số có cùng tên với thuộc tính, nếu không sử dụng "self", bạn sẽ gặp lỗi biên dịch do không rõ ràng.
- **Sử Dụng Không Cần Thiết**: Trong một số trường hợp, sử dụng "self" là không cần thiết, nhưng nó có thể làm cho mã của bạn dễ hiểu hơn. Tốt nhất là sử dụng "self" khi cần làm rõ.

### Ghi Chú Bổ Sung
- Trong các phương thức tĩnh (static methods), "self" sẽ tham chiếu đến lớp, không phải đến một đối tượng cụ thể.
- "self" cũng có thể được sử dụng trong các hàm khởi tạo và các phương thức mở rộng (extension methods).

## Tóm Tắt Một Dòng
Từ khóa "self" trong Swift cho phép bạn tham chiếu đến đối tượng hiện tại, giúp phân biệt giữa các thuộc tính và tham số, đồng thời tăng tính rõ ràng trong mã nguồn.