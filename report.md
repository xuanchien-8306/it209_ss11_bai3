# Báo cáo Bài 3: Gradle Dependency Caching

## 1. Mục tiêu

Cấu hình Gradle Dependency Caching trong GitHub Actions để giảm thời gian tải thư viện khi chạy CI.

## 2. Cấu hình

Sử dụng `actions/setup-java@v5` với cấu hình:

- Java version: 17
- Distribution: Temurin
- Cache: gradle

## 3. Kết quả thực nghiệm
   Nội dung	Lần 1	Lần 2
   Thời gian chạy Job	58 giây	34 giây
   Thời gian bước test	55 giây	30 giây
   Trạng thái workflow	Success	Success
   Trạng thái cache	Chạy lần đầu	Đã cấu hình cache Gradle
    
## 4. Kết luận

Đã cấu hình Gradle Dependency Caching trong GitHub Actions. Cache giúp tái sử dụng các thư viện Gradle giữa các lần chạy phù hợp, hạn chế tải lại thư viện từ Internet và có thể giảm thời gian thực thi CI.