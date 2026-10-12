# Java Spring Boot API - CI/CD với Gradle & GitHub Actions Artifacts

Dự án mẫu Java Spring Boot REST API tích hợp quy trình CI/CD hoàn chỉnh sử dụng **Gradle** và **GitHub Actions**.

## Tính năng dự án
- Framework: Spring Boot 3.2.5 (Java 17)
- Build tool: Gradle Wrapper
- Các endpoint REST API mẫu:
  - `GET /api/hello`: Thông điệp chào mừng
  - `GET /api/health`: Health check service
- Unit test với Spring Boot Test & JUnit 5
- GitHub Actions CI Pipeline:
  - Tự động checkout và thiết lập môi trường JDK 17
  - Thực thi kiểm thử tự động (`./gradlew test`)
  - Biên dịch và đóng gói ứng dụng `.jar` (`./gradlew bootJar`)
  - Tải lên và lưu trữ thành phẩm bản build (`build/libs/*.jar`) lên GitHub Actions Artifacts với tên `app-jar`.

## Cấu trúc thư mục
```
bai2/
├── .github/
│   └── workflows/
│       └── ci.yml               # Workflow chính của GitHub Actions
├── gradle/
│   └── wrapper/
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── homework/
│   └── session_11/
│       └── ex2/
│           ├── ci.yml           # Bản sao tệp ci.yml phục vụ nộp bài
│           └── README.md        # Báo cáo chi tiết và hướng dẫn kiểm tra
├── src/                         # Mã nguồn ứng dụng và Unit tests
├── build.gradle                 # Cấu hình Gradle build
├── settings.gradle              # Tên dự án
├── gradlew                      # Gradle Wrapper script (Linux/macOS)
├── gradlew.bat                  # Gradle Wrapper script (Windows)
└── README.md
```
