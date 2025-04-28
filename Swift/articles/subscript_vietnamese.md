<!--
Meta Description: # Subscript trong Swift: Cách sử dụng và ví dụ ## Tóm tắt Subscript trong Swift cho phép bạn truy cập vào phần tử của một tập hợp, như mảng, từ điển h...
Meta Keywords: subscript, một, các, bạn, cập
-->

# Subscript trong Swift: Cách sử dụng và ví dụ

## Tóm tắt
Subscript trong Swift cho phép bạn truy cập vào phần tử của một tập hợp, như mảng, từ điển hoặc các kiểu dữ liệu tùy chỉnh, một cách thuận tiện và dễ hiểu. Nó giúp đơn giản hóa việc truy xuất và cập nhật giá trị trong các cấu trúc dữ liệu.

## Tài liệu
Subscript là một tính năng mạnh mẽ trong Swift, cho phép bạn định nghĩa cách thức truy cập các giá trị của một kiểu dữ liệu. Bạn có thể sử dụng subscript cho các kiểu dữ liệu như mảng, từ điển, hoặc thậm chí là các kiểu dữ liệu tùy chỉnh mà bạn tự định nghĩa.

### Mục đích
Subscript giúp bạn truy cập vào các phần tử của một kiểu dữ liệu mà không cần phải gọi một phương thức riêng biệt.

### Cách sử dụng
Để định nghĩa một subscript, bạn sử dụng từ khóa `subscript` theo sau là danh sách tham số và kiểu trả về. Dưới đây là cú pháp chung cho một subscript:

```swift
subscript(index: Int) -> T {
    get {
        // Trả về giá trị
    }
    set(newValue) {
        // Cập nhật giá trị
    }
}
```

Bạn có thể định nghĩa subscript với nhiều tham số hoặc với các kiểu dữ liệu khác nhau.

## Ví dụ
### Ví dụ cơ bản với mảng

```swift
struct MyArray {
    var items: [Int]
    
    subscript(index: Int) -> Int {
        get {
            return items[index]
        }
        set(newValue) {
            items[index] = newValue
        }
    }
}

var array = MyArray(items: [1, 2, 3])
print(array[0]) // Kết quả: 1
array[0] = 10
print(array[0]) // Kết quả: 10
```

### Ví dụ với từ điển

```swift
struct MyDictionary {
    var items: [String: Int]
    
    subscript(key: String) -> Int? {
        get {
            return items[key]
        }
        set(newValue) {
            items[key] = newValue
        }
    }
}

var dictionary = MyDictionary(items: ["A": 1, "B": 2])
print(dictionary["A"]) // Kết quả: Optional(1)
dictionary["A"] = 10
print(dictionary["A"]) // Kết quả: Optional(10)
```

## Giải thích
Khi sử dụng subscript, có một số điều cần lưu ý:

- **Kiểm tra giới hạn**: Khi truy cập vào các phần tử của mảng, bạn nên đảm bảo chỉ số không vượt quá giới hạn của mảng để tránh lỗi runtime.
- **Cài đặt cho subscript**: Bạn có thể chỉ định subscript chỉ với getter hoặc setter, tùy thuộc vào nhu cầu sử dụng.
- **Nhiều tham số**: Subscript có thể nhận nhiều tham số để cho phép truy cập đến các phần tử phức tạp hơn, như một mảng hai chiều.

## Tóm tắt một dòng
Subscript trong Swift cho phép bạn truy cập và cập nhật các giá trị trong các kiểu dữ liệu một cách dễ dàng và thuận tiện.