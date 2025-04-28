<!--
Meta Description: # Enum trong Swift: Hướng Dẫn Chi Tiết và Ví Dụ Cụ Thể ## Tóm tắt Enum (liệt kê) trong Swift là một kiểu dữ liệu mạnh mẽ cho phép bạn định nghĩa một t...
Meta Keywords: enum, các, case, giá, trị
-->

# Enum trong Swift: Hướng Dẫn Chi Tiết và Ví Dụ Cụ Thể

## Tóm tắt
Enum (liệt kê) trong Swift là một kiểu dữ liệu mạnh mẽ cho phép bạn định nghĩa một tập hợp các giá trị có liên quan, giúp tổ chức và quản lý mã nguồn hiệu quả hơn.

## Tài liệu
Enum trong Swift được sử dụng để định nghĩa một tập hợp các giá trị có tên. Điều này rất hữu ích khi bạn muốn nhóm các giá trị lại với nhau, ví dụ như các trạng thái, loại sản phẩm hay các phương thức giao hàng. Enum có thể có các giá trị liên quan và có thể chứa các thuộc tính và phương thức liên quan đến các giá trị đó.

### Cách sử dụng
Để định nghĩa một enum, bạn sử dụng từ khóa `enum` theo cú pháp sau:

```swift
enum TênEnum {
    case giáTrị1
    case giáTrị2
    case giáTrị3
}
```

### Chi tiết
- **Tính năng của Enum:**
  - Enum có thể có nhiều trường hợp (cases) và có thể có giá trị liên quan đến từng trường hợp.
  - Enum hỗ trợ các giá trị kiểu dữ liệu khác nhau cho từng trường hợp, cho phép bạn lưu trữ thông tin liên quan.
  - Bạn có thể mở rộng enum với các phương thức và thuộc tính.

## Ví dụ
### Ví dụ cơ bản về Enum

```swift
enum Màu {
    case đỏ
    case xanh
    case vàng
}

let màuXe = Màu.red
```

### Enum với giá trị liên quan

```swift
enum PhươngTiệnGiaoThông {
    case ôtô(sốBánh: Int)
    case xeMáy(sốBánh: Int)
    case tàuThuyền
}

let phươngTiện = PhươngTiệnGiaoThông.ôTô(sốBánh: 4)
```

### Sử dụng switch với Enum

```swift
switch phươngTiện {
case .ôtô(let sốBánh):
    print("Đây là ôtô với \(sốBánh) bánh.")
case .xeMáy(let sốBánh):
    print("Đây là xe máy với \(sốBánh) bánh.")
case .tàuThuyền:
    print("Đây là tàu thuyền.")
}
```

## Giải thích
Một số lưu ý khi làm việc với enum trong Swift:
- Khi định nghĩa enum, bạn cần nhớ rằng mỗi trường hợp là duy nhất và không thể lặp lại.
- Enum không thể được khởi tạo với giá trị ngoài các trường hợp đã định nghĩa.
- Khi sử dụng switch, bạn cần xử lý tất cả các trường hợp của enum để biên dịch thành công, trừ khi bạn sử dụng `default`.

## Tóm tắt một dòng
Enum trong Swift là một cách hiệu quả để nhóm và quản lý các giá trị liên quan, hỗ trợ cấu trúc mã nguồn rõ ràng và mạnh mẽ.