<!--
Meta Description: # Từ Khóa "let" trong Swift: Cách Khai Báo Hằng Số ## Tóm tắt Trong Swift, từ khóa `let` được sử dụng để khai báo hằng số. Một hằng số là một biến khô...
Meta Keywords: let, hằng, swift, khai, báo
-->

# Từ Khóa "let" trong Swift: Cách Khai Báo Hằng Số

## Tóm tắt
Trong Swift, từ khóa `let` được sử dụng để khai báo hằng số. Một hằng số là một biến không thể thay đổi sau khi được gán giá trị ban đầu, giúp đảm bảo tính nhất quán và an toàn trong mã nguồn.

## Tài liệu
Từ khóa `let` là một phần quan trọng trong việc khai báo biến trong Swift. Được sử dụng để định nghĩa một hằng số, `let` cho phép lập trình viên tạo ra các giá trị không thay đổi, điều này giúp tránh được những sai lầm không mong muốn do việc thay đổi giá trị của biến.

### Mục đích
- Đảm bảo rằng một giá trị không thay đổi trong suốt vòng đời của một đối tượng.
- Cải thiện tính an toàn và rõ ràng của mã nguồn.

### Cách Sử Dụng
Để khai báo một hằng số bằng từ khóa `let`, bạn chỉ cần sử dụng cú pháp sau:
```swift
let tênBiến = giáTrị
```
Trong đó:
- `tênBiến` là tên của hằng số bạn muốn khai báo.
- `giáTrị` là giá trị bạn muốn gán cho hằng số đó.

## Ví dụ
Dưới đây là một số ví dụ cơ bản về cách sử dụng `let` trong Swift:

### Ví dụ 1: Khai báo hằng số số nguyên
```swift
let soNguyen: Int = 10
```
### Ví dụ 2: Khai báo hằng số chuỗi
```swift
let ten: String = "Nguyễn Văn A"
```
### Ví dụ 3: Khai báo hằng số mảng
```swift
let danhSachSo: [Int] = [1, 2, 3, 4, 5]
```

## Giải thích
Mặc dù việc sử dụng `let` rất đơn giản, nhưng có một số điểm cần lưu ý:
- Nếu bạn cố gắng thay đổi giá trị của một hằng số đã khai báo bằng `let`, bạn sẽ gặp lỗi biên dịch. Điều này giúp bảo vệ mã nguồn khỏi những thay đổi không mong muốn.
- Bạn có thể khai báo hằng số mà không cần chỉ định kiểu. Swift sẽ tự động suy diễn kiểu dữ liệu dựa trên giá trị được gán:
  ```swift
  let soThuc = 3.14 // Swift tự động suy diễn là Double
  ```

## Tóm tắt một dòng
Từ khóa `let` trong Swift được sử dụng để khai báo hằng số, giúp đảm bảo rằng giá trị không thể bị thay đổi sau khi được gán.