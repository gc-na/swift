<!--
Meta Description: # Từ Khóa "throw" Trong Swift: Cách Xử Lý Lỗi Hiệu Quả ## Tóm Tắt Từ khóa `throw` trong Swift được sử dụng để ném ra một lỗi, cho phép lập trình viên ...
Meta Keywords: lỗi, ném, một, dụng, bạn
-->

# Từ Khóa "throw" Trong Swift: Cách Xử Lý Lỗi Hiệu Quả

## Tóm Tắt
Từ khóa `throw` trong Swift được sử dụng để ném ra một lỗi, cho phép lập trình viên xử lý các tình huống lỗi trong chương trình một cách rõ ràng và hiệu quả.

## Tài Liệu
### Mục Đích
`throw` là một phần quan trọng trong hệ thống xử lý lỗi của Swift. Nó cho phép bạn ném ra các lỗi khi có sự cố xảy ra, từ đó giúp chương trình không bị dừng lại mà có thể xử lý lỗi một cách an toàn.

### Cách Sử Dụng
Để sử dụng `throw`, bạn cần định nghĩa một enum hoặc struct tuân theo giao thức `Error`. Sau đó, bạn có thể ném lỗi trong các hàm hoặc phương thức mà được khai báo là có thể ném lỗi bằng cách sử dụng từ khóa `throws`.

#### Cú Pháp
```swift
enum MyError: Error {
    case invalidInput
    case calculationError
}

func performCalculation(input: Int) throws -> Int {
    guard input >= 0 else {
        throw MyError.invalidInput
    }
    // Thực hiện tính toán
    return input * 2
}
```

### Chi Tiết
- **Khai Báo Hàm Ném Lỗi**: Khi khai báo một hàm có khả năng ném lỗi, bạn cần thêm từ khóa `throws` vào phần khai báo hàm.
- **Ném Lỗi**: Sử dụng từ khóa `throw` theo sau là tên lỗi mà bạn muốn ném ra.
- **Xử Lý Lỗi**: Để gọi một hàm ném lỗi, bạn cần sử dụng `try`, và có thể sử dụng `do-catch` để xử lý các lỗi được ném ra.

## Ví Dụ
### Ví Dụ Cơ Bản
```swift
enum FileError: Error {
    case fileNotFound
}

func readFile(named fileName: String) throws {
    let files = ["document.txt", "image.png"]
    guard files.contains(fileName) else {
        throw FileError.fileNotFound
    }
    // Đọc file
    print("Đọc file: \(fileName)")
}

do {
    try readFile(named: "document.txt")
    try readFile(named: "missing.txt")
} catch FileError.fileNotFound {
    print("File không tồn tại.")
}
```

## Giải Thích
### Các Lỗi Thường Gặp
- **Không Sử Dụng `do-catch`**: Nếu bạn gọi một hàm ném lỗi mà không sử dụng `try`, trình biên dịch sẽ báo lỗi.
- **Ném Lỗi Không Được Xử Lý**: Nếu bạn không xử lý lỗi ném ra, chương trình sẽ dừng lại. Do đó, luôn đảm bảo rằng bạn có cơ chế xử lý lỗi.

### Ghi Chú Bổ Sung
- Bạn có thể ném nhiều loại lỗi khác nhau từ cùng một hàm.
- Sử dụng `try?` và `try!` để quản lý lỗi một cách linh hoạt hơn, nhưng hãy cẩn thận với `try!` vì nó có thể gây ra lỗi runtime nếu lỗi xảy ra.

## Tóm Tắt Một Dòng
Từ khóa `throw` trong Swift cho phép lập trình viên ném ra các lỗi để xử lý trong các tình huống bất ngờ, giúp tăng cường tính ổn định và an toàn cho chương trình.