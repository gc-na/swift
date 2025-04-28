<!--
Meta Description: # Toán Tử trong Swift: Hướng Dẫn Chi Tiết và Ví Dụ Cụ Thể ## Tóm tắt Toán tử trong Swift là các ký hiệu và từ khóa dùng để thực hiện các phép toán trê...
Meta Keywords: toán, let, các, swift, trong
-->

# Toán Tử trong Swift: Hướng Dẫn Chi Tiết và Ví Dụ Cụ Thể

## Tóm tắt
Toán tử trong Swift là các ký hiệu và từ khóa dùng để thực hiện các phép toán trên các giá trị và biến. Swift hỗ trợ nhiều loại toán tử, bao gồm toán tử số học, toán tử so sánh, toán tử logic, và toán tử gán, giúp lập trình viên xử lý dữ liệu một cách linh hoạt và hiệu quả.

## Tài liệu
Toán tử là một phần quan trọng trong ngôn ngữ lập trình Swift, cho phép bạn thực hiện các phép toán và thao tác trên dữ liệu. Các loại toán tử trong Swift bao gồm:

1. **Toán tử số học**: Dùng để thực hiện các phép toán cộng (+), trừ (-), nhân (*), chia (/) và chia lấy dư (%).
2. **Toán tử so sánh**: Dùng để so sánh các giá trị, bao gồm bằng (==), khác (!=), lớn hơn (>), nhỏ hơn (<), lớn hơn hoặc bằng (>=), nhỏ hơn hoặc bằng (<=).
3. **Toán tử logic**: Dùng để thực hiện các phép toán logic, bao gồm và (&&), hoặc (||), không (!).
4. **Toán tử gán**: Dùng để gán giá trị cho biến, bao gồm gán đơn giản (=) và các toán tử gán kết hợp như +=, -=, *=, /=.
5. **Toán tử tùy chỉnh**: Swift cho phép bạn định nghĩa toán tử riêng để mở rộng khả năng của ngôn ngữ.

Mỗi loại toán tử có cú pháp và cách sử dụng riêng, giúp lập trình viên dễ dàng thao tác với dữ liệu.

## Ví dụ
Dưới đây là một số ví dụ cơ bản về cách sử dụng các toán tử trong Swift:

### Toán tử số học
```swift
let a = 10
let b = 5

let tong = a + b // 15
let hieu = a - b // 5
let tich = a * b // 50
let thuong = a / b // 2
let du = a % b // 0
```

### Toán tử so sánh
```swift
let x = 10
let y = 20

let laBang = (x == y) // false
let laKhac = (x != y) // true
let lonHon = (x > y) // false
```

### Toán tử logic
```swift
let isTrue = true
let isFalse = false

let resultAnd = isTrue && isFalse // false
let resultOr = isTrue || isFalse // true
let resultNot = !isTrue // false
```

### Toán tử gán
```swift
var number = 10
number += 5 // number now equals 15
```

## Giải thích
Khi sử dụng toán tử trong Swift, bạn cần chú ý đến thứ tự ưu tiên của các toán tử. Thứ tự ưu tiên xác định toán tử nào sẽ được thực hiện trước trong một biểu thức phức tạp. Ngoài ra, việc sử dụng toán tử so sánh và logic có thể dẫn đến một số kết quả không như mong đợi nếu bạn không kiểm tra kỹ các điều kiện.

Một điểm quan trọng là toán tử tùy chỉnh. Khi bạn định nghĩa toán tử riêng, bạn cần đảm bảo rằng nó không gây nhầm lẫn với các toán tử có sẵn và tuân theo các quy tắc cú pháp của Swift.

## Tóm tắt một dòng
Toán tử trong Swift là các ký hiệu và từ khóa cho phép thực hiện các phép toán và thao tác trên dữ liệu một cách hiệu quả.