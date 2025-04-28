<!--
Meta Description: # Từ Khóa "private" trong Swift: Định Nghĩa và Cách Sử Dụng ## Tóm Tắt Từ khóa `private` trong Swift được sử dụng để chỉ định quyền truy cập cho các t...
Meta Keywords: private, trong, truy, cập, hoặc
-->

# Từ Khóa "private" trong Swift: Định Nghĩa và Cách Sử Dụng

## Tóm Tắt
Từ khóa `private` trong Swift được sử dụng để chỉ định quyền truy cập cho các thuộc tính và phương thức trong một lớp, cấu trúc hoặc mở rộng, giúp bảo vệ tính toàn vẹn của dữ liệu trong chương trình.

## Tài Liệu
### Mục Đích
Từ khóa `private` kiểm soát quyền truy cập của các thành phần bên trong lớp hoặc cấu trúc. Khi một thuộc tính hoặc phương thức được đánh dấu là `private`, nó chỉ có thể được truy cập từ bên trong cùng một đối tượng mà thôi.

### Cách Sử Dụng
Để sử dụng từ khóa `private`, bạn chỉ cần thêm nó trước khai báo của thuộc tính hoặc phương thức. Đây là cách để đảm bảo rằng các thành phần này không thể được truy cập từ bên ngoài lớp hoặc cấu trúc đó.

### Chi Tiết
- **Quyền truy cập**: `private` đảm bảo rằng thuộc tính hoặc phương thức chỉ có thể được truy cập từ bên trong lớp hoặc cấu trúc mà nó được định nghĩa.
- **Bảo mật**: Sử dụng `private` giúp bảo vệ trạng thái và hành vi của đối tượng, ngăn chặn việc truy cập trái phép từ bên ngoài.
- **Khả năng mở rộng**: Khi bạn sử dụng `private`, bạn có thể thay đổi cách mà lớp hoặc cấu trúc hoạt động mà không lo lắng về việc ảnh hưởng đến mã bên ngoài.

## Ví Dụ
```swift
class MyClass {
    private var secretNumber: Int = 42
    
    private func printSecret() {
        print("Secret number is \(secretNumber)")
    }
    
    func revealSecret() {
        printSecret() // Gọi phương thức private bên trong lớp
    }
}

let myObject = MyClass()
// myObject.secretNumber // Lỗi: 'secretNumber' là private
myObject.revealSecret() // In ra: Secret number is 42
```

## Giải Thích
- **Nguy cơ**: Nếu bạn quên đánh dấu một thuộc tính hoặc phương thức là `private`, có thể dẫn đến việc mã bên ngoài truy cập và thay đổi dữ liệu của bạn, gây ra lỗi hoặc hành vi không mong muốn.
- **Sự nhầm lẫn**: Một số lập trình viên mới có thể không hiểu rõ sự khác biệt giữa `private`, `fileprivate`, và `internal`. `private` chỉ cho phép truy cập từ cùng một lớp, trong khi `fileprivate` cho phép truy cập từ cùng một file và `internal` cho phép truy cập từ bất kỳ đâu trong module.

## Tóm Tắt Một Câu
Từ khóa `private` trong Swift giúp bảo vệ các thuộc tính và phương thức của lớp, đảm bảo rằng chúng chỉ có thể được truy cập từ bên trong lớp đó.