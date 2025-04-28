<!--
Meta Description: # Swift 中的枚舉 (Enum) 使用指南 ## 概述 在 Swift 中，枚舉（Enum）是一種強大的數據類型，用於定義一組相關的值。它不僅可以用來表示單一類型的多個可能值，還可以附加額外的資訊，並提供更強的類型安全性和可讀性。 ## 文件說明 枚舉在 Swift 中的主要目的是為了更清晰地...
Meta Keywords: case, swift, enum, int, sunny
-->

# Swift 中的枚舉 (Enum) 使用指南

## 概述
在 Swift 中，枚舉（Enum）是一種強大的數據類型，用於定義一組相關的值。它不僅可以用來表示單一類型的多個可能值，還可以附加額外的資訊，並提供更強的類型安全性和可讀性。

## 文件說明
枚舉在 Swift 中的主要目的是為了更清晰地表示一組相關的選項。與其他語言中的枚舉相比，Swift 的枚舉更加靈活，支持方法、計算屬性及原始值等功能。枚舉可以用於控制流、選擇不同的行為或簡化代碼的可讀性。

### 使用方式
在 Swift 中，您可以通過 `enum` 關鍵字來定義一個枚舉。基本語法如下：

```swift
enum EnumName {
    case caseName1
    case caseName2
    // 可以有多個 case
}
```

### 詳細說明
- **定義枚舉**：使用 `enum` 關鍵字，並跟隨一個名稱，然後是一系列的 `case`。
- **原始值**：枚舉可以為每個 case 指定一個原始值，例如整數或字符串。
- **關聯值**：您還可以為枚舉的 case 指定關聯值，這使得每個 case 可以存儲不同類型的數據。
- **方法**：枚舉可以擁有方法，這樣可以對其 case 執行相關操作。
- **計算屬性**：枚舉也可以添加計算屬性，以便根據其當前狀態返回不同的值。

```swift
enum Direction {
    case north, south, east, west
}

enum Planet: Int {
    case mercury = 1, venus, earth, mars
}

enum Barcode {
    case upc(Int, Int, Int, Int)
    case qrCode(String)
}
```

## 範例
以下是一些基本的使用範例，展示如何在 Swift 中定義和使用枚舉：

```swift
enum Weather {
    case sunny
    case rainy
    case cloudy
}

let todayWeather = Weather.sunny

switch todayWeather {
case .sunny:
    print("今天是晴天")
case .rainy:
    print("今天是雨天")
case .cloudy:
    print("今天是陰天")
}
```

## 解釋
在使用枚舉時，有一些常見的陷阱和注意事項：
- **未處理的 case**：在使用 `switch` 語句時，確保處理所有的 case，否則編譯器會報錯。如果未處理某些 case，您可以使用 `default` 來捕獲。
- **選擇適合的原始值類型**：原始值的類型應該符合需求，且需要保持一致性。
- **避免複雜的枚舉**：過於複雜的枚舉可能會導致代碼難以理解，建議保持簡潔。

## 單句總結
Swift 中的枚舉是一種強大的數據類型，用於表示一組相關值，並提供了靈活的功能以提高代碼的可讀性和安全性。