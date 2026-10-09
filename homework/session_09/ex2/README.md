<img width="554" height="333" alt="ex2_ss09" src="https://github.com/user-attachments/assets/620059d0-a23d-49ca-bcca-4bbeb4e9dabd" />
# Bài 2: Khởi chạy Web Server Nginx với Port Mapping

## 1. Mục tiêu
Khởi chạy Nginx bằng Docker container, ánh xạ cổng 8080:80, kiểm tra phản hồi và dọn dẹp container sau khi thử nghiệm.

## 2. Khởi chạy container

```bash
docker run -d -p 8080:80 --name my-web nginx:alpine
```

- `-d`: Chạy container ở chế độ ngầm.
- `-p 8080:80`: Ánh xạ cổng 8080 của máy tính tới cổng 80 của container.
- `--name my-web`: Đặt tên container là `my-web`.
- `nginx:alpine`: Sử dụng image Nginx phiên bản Alpine nhẹ.

## 3. Kiểm tra phản hồi

Thực hiện lệnh:

```bash
curl http://localhost:8080
```

**Kết quả:** Thành công, trả về mã HTML có nội dung `Welcome to nginx!`.

## 4. Dừng và xóa container

Thực hiện lệnh:

```bash
docker stop my-web && docker rm my-web
```

**Kết quả:** Container `my-web` đã được dừng và xóa thành công.

## 5. Kết luận

Đã hoàn thành việc khởi chạy Web Server Nginx bằng Docker, ánh xạ cổng 8080:80, kiểm tra truy cập thành công và dọn dẹp container sau khi thử nghiệm.
