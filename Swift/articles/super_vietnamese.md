<!--
Meta Description: # Từ Khóa "super" Trong Swift: Hiểu Rõ về Khả Năng Kế Thừa ## Tóm Tắt Từ khóa "super" trong Swift được sử dụng để tham chiếu đến lớp cha (superclass) ...
Meta Keywords: lớp, cha, super, của, phương
-->

# Từ Khóa "super" Trong Swift: Hiểu Rõ về Khả Năng Kế Thừa

## Tóm Tắt
Từ khóa "super" trong Swift được sử dụng để tham chiếu đến lớp cha (superclass) của lớp hiện tại, cho phép truy cập vào các thuộc tính và phương thức của lớp cha.

## Tài Liệu
### Mục Đích
Từ khóa "super" giúp lập trình viên có thể tương tác với lớp cha trong cấu trúc kế thừa, cho phép gọi các phương thức và thuộc tính đã được định nghĩa trong lớp cha.

### Cách Sử Dụng
- **Gọi phương thức của lớp cha**: Bạn có thể sử dụng "super" để gọi các phương thức của lớp cha từ lớp con.
- **Truy cập thuộc tính của lớp cha**: "super" cũng có thể được sử dụng để truy cập các thuộc tính của lớp cha.

### Chi Tiết
Khi bạn định nghĩa một lớp con, đôi khi bạn muốn gọi phương thức hoặc truy cập thuộc tính từ lớp cha. Từ khóa "super" rất hữu ích trong trường hợp này. Sử dụng "super" trước tên phương thức hoặc thuộc tính để chỉ rõ rằng bạn đang muốn thực hiện hành động đó trên lớp cha.

```swift
class Animal {
    func makeSound() {
        print("Some sound")
    }
}

class Dog: Animal {
    override func makeSound() {
        super.makeSound() // Gọi phương thức makeSound của lớp Animal
        print("Bark")
    }
}
```

Trong ví dụ trên, lớp `Dog` kế thừa từ lớp `Animal` và gọi phương thức `makeSound` của lớp cha trước khi in ra âm thanh "Bark".

## Ví Dụ
### Ví dụ 1: Gọi phương thức của lớp cha
```swift
class Vehicle {
    func start() {
        print("Vehicle is starting")
    }
}

class Car: Vehicle {
    override func start() {
        super.start() // Gọi phương thức start của lớp Vehicle
        print("Car is ready to go")
    }
}

let myCar = Car()
myCar.start()
// Kết quả: 
// Vehicle is starting
// Car is ready to go
```

### Ví dụ 2: Truy cập thuộc tính của lớp cha
```swift
class Person {
    var name: String = "Unknown"
}

class Employee: Person {
    var employeeID: Int = 0
    
    func printInfo() {
        print("Name: \(super.name), ID: \(employeeID)")
    }
}

let employee = Employee()
employee.name = "John Doe"
employee.employeeID = 123
employee.printInfo()
// Kết quả: Name: John Doe, ID: 123
```

## Giải Thích
### Cạm Bẫy Thường Gặp
- **Quên gọi "super"**: Khi ghi đè một phương thức trong lớp con, nếu bạn không gọi "super", bạn có thể bỏ lỡ logic quan trọng từ lớp cha.
- **Sử dụng sai ngữ cảnh**: Đảm bảo rằng "super" chỉ được sử dụng trong các lớp con để truy cập các thành phần của lớp cha.

### Ghi Chú Thêm
- "super" chỉ có thể được sử dụng trong ngữ cảnh của một lớp con.
- Việc sử dụng "super" phát huy hiệu quả tốt nhất trong các trường hợp kế thừa phức tạp, nơi mà các phương thức của lớp cha cần được duy trì.

## Tóm Tắt Một Câu
Từ khóa "super" trong Swift cho phép bạn truy cập và gọi các phương thức và thuộc tính từ lớp cha trong mô hình kế thừa.