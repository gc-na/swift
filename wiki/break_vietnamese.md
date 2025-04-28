<!--
Meta Description: # Câu Lệnh "break" Trong Swift: Cách Sử Dụng và Ví Dụ ## Tóm Tắt Câu lệnh "break" trong Swift được sử dụng để thoát khỏi các vòng lặp như `for`, `whil...
Meta Keywords: vòng, lặp, break, trong, swift
-->

# Câu Lệnh "break" Trong Swift: Cách Sử Dụng và Ví Dụ

## Tóm Tắt
Câu lệnh "break" trong Swift được sử dụng để thoát khỏi các vòng lặp như `for`, `while` hoặc `repeat-while`. Nó cho phép lập trình viên dừng một vòng lặp sớm dựa trên điều kiện cụ thể, giúp tối ưu hóa quá trình xử lý và cải thiện hiệu suất chương trình.

## Tài Liệu
Câu lệnh "break" là một phần quan trọng trong lập trình điều kiện và vòng lặp trong Swift. Nó có thể được sử dụng trong các cấu trúc vòng lặp khác nhau, cho phép bạn ngắt bỏ vòng lặp khi một điều kiện nhất định được đáp ứng. 

### Mục Đích
- Dừng vòng lặp khi không còn cần thiết.
- Cải thiện hiệu suất bằng cách tránh các vòng lặp không cần thiết.
  
### Cách Sử Dụng
Câu lệnh "break" có thể được sử dụng trong các vòng lặp như sau:

```swift
for number in 1...10 {
    if number == 5 {
        break
    }
    print(number)
}
```

Trong ví dụ trên, vòng lặp sẽ dừng lại ngay khi `number` bằng 5, và chỉ in ra các số từ 1 đến 4.

## Ví Dụ
### Ví Dụ Cơ Bản
```swift
var sum = 0
for i in 1...100 {
    if sum > 50 {
        break
    }
    sum += i
}
print(sum) // Kết quả sẽ là 51
```

### Ví Dụ Trong Vòng Lặp While
```swift
var count = 0
while true {
    if count == 3 {
        break
    }
    print(count)
    count += 1
}
// Kết quả sẽ là 0, 1, 2
```

## Giải Thích
### Những Lưu Ý Thường Gặp
- **Vòng lặp lồng nhau**: Nếu bạn sử dụng "break" trong một vòng lặp lồng nhau, nó chỉ dừng vòng lặp hiện tại, không phải vòng lặp bên ngoài.
  
```swift
for i in 1...5 {
    for j in 1...5 {
        if j == 3 {
            break // chỉ dừng vòng lặp j
        }
        print("i: \(i), j: \(j)")
    }
}
// Kết quả sẽ là i: 1, j: 1; i: 1, j: 2; i: 2, j: 1; i: 2, j: 2; ...
```

- **Không sử dụng break trong switch case**:  Trong Swift, bạn không cần sử dụng "break" để thoát khỏi mỗi case trong khối switch vì Swift tự động dừng tại mỗi case.

### Ghi Chú
Mặc dù "break" hữu ích, bạn nên sử dụng nó một cách cẩn thận để tránh làm cho mã trở nên khó đọc hoặc khó theo dõi. Việc lạm dụng "break" trong các vòng lặp có thể dẫn đến các lỗi logic.

## Tóm Tắt Một Dòng
Câu lệnh "break" trong Swift cho phép lập trình viên dừng một vòng lặp khi một điều kiện nhất định được đáp ứng, giúp tối ưu hóa quá trình thực thi mã.