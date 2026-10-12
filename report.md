# Báo cáo Bài 3: Gradle Dependency Caching

## 1. Mục tiêu

Cấu hình Gradle Dependency Caching trong GitHub Actions để giảm thời gian tải thư viện khi chạy CI.

## 2. Cấu hình

Sử dụng `actions/setup-java@v5` với cấu hình:

- Java version: 17
- Distribution: Temurin
- Cache: gradle

## 3. Kết quả thực nghiệm

| Nội dung | Lần 1 (chưa có cache) | Lần 2 (có cache) |
|---|---|---|
| Thời gian chạy Job | ... | ... |
| Thời gian bước test | ... | ... |
| Trạng thái cache | Tạo cache | ... |

## 4. Kết luận

Đã cấu hình Gradle Dependency Caching trong GitHub Actions. Cache giúp tái sử dụng các thư viện Gradle giữa các lần chạy phù hợp, hạn chế tải lại thư viện từ Internet và có thể giảm thời gian thực thi CI.