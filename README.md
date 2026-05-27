# Lab 7 — Postman

Bài lab tìm hiểu và sử dụng **Postman** để kiểm thử API. Postman hỗ trợ gửi các HTTP request (`GET`, `POST`, `PUT`, `DELETE`) tới server và xem phản hồi từ API.

---

## 1. Giới thiệu

Trong bài lab này, bạn sẽ làm quen với Postman — công cụ phổ biến khi phát triển và kiểm thử các hệ thống dùng REST API.

## 2. Mục tiêu

- Hiểu cách dùng Postman để kiểm thử API
- Gửi các request `GET`, `POST`, `PUT`, `DELETE`
- Quan sát **status code** và dữ liệu phản hồi từ server
- Chụp ảnh minh họa kết quả thực hiện
- Nộp sản phẩm qua **GitHub Repository**

## 3. Công cụ & API mẫu

| Công cụ | Ghi chú |
| --- | --- |
| Postman | Gửi request và xem response |
| GitHub | Nộp bài lab |
| JSONPlaceholder | API mẫu dùng trong lab |

**Base URL:** `https://jsonplaceholder.typicode.com`

---

## 4. Các bước thực hiện

### 4.1. GET — Lấy danh sách bài viết

```http
GET https://jsonplaceholder.typicode.com/posts
```
    
| --- | --- |
| **Mục đích** | Lấy danh sách các bài viết từ API |
| **Kết quả** | Server trả về danh sách bài viết dạng JSON |

### 4.2. GET — Lấy chi tiết một bài viết

```http
GET https://jsonplaceholder.typicode.com/posts/1
```

| --- | --- |
| **Mục đích** | Lấy thông tin chi tiết bài viết có `id = 1` |
| **Kết quả** | Server trả về thông tin một bài viết |

### 4.3. POST — Tạo mới bài viết

```http
POST https://jsonplaceholder.typicode.com/posts
```

**Body (JSON):**

```json
{
  "title": "Lab 7 Postman",
  "body": "Thuc hanh kiem thu API bang Postman",
  "userId": 1
}
```

| --- | --- |
| **Mục đích** | Gửi dữ liệu lên server để tạo bài viết mới |
| **Kết quả** | Server trả về bài viết vừa tạo kèm `id` |

### 4.4. PUT — Cập nhật bài viết

```http
PUT https://jsonplaceholder.typicode.com/posts/1
```

**Body (JSON):**

```json
{
  "id": 1,
  "title": "Cap nhat Lab 7 Postman",
  "body": "Noi dung da duoc cap nhat bang PUT request",
  "userId": 1
}
```

| --- | --- |
| **Mục đích** | Cập nhật bài viết có `id = 1` |
| **Kết quả** | Server trả về dữ liệu sau khi cập nhật |

### 4.5. DELETE — Xóa bài viết

```http
DELETE https://jsonplaceholder.typicode.com/posts/1
```

| --- | --- |
| **Mục đích** | Gửi yêu cầu xóa bài viết có `id = 1` |
| **Kết quả** | Server trả về phản hồi thành công |

---

## 5. Tổng hợp kết quả

| STT | Method | URL | Mục đích | Kết quả |
| --- | --- | --- | --- | --- |
| 1 | `GET` | `/posts` | Lấy danh sách bài viết | Thành công |
| 2 | `GET` | `/posts/1` | Lấy chi tiết bài viết | Thành công |
| 3 | `POST` | `/posts` | Tạo mới bài viết | Thành công |
| 4 | `PUT` | `/posts/1` | Cập nhật bài viết | Thành công |
| 5 | `DELETE` | `/posts/1` | Xóa bài viết | Thành công |

---

## 6. Kết luận

Sau khi hoàn thành bài lab, em đã nắm được cách dùng Postman để kiểm thử API: gửi các request `GET`, `POST`, `PUT`, `DELETE`, nhập JSON trong phần **Body**, xem **status code** và kiểm tra dữ liệu phản hồi từ server.

Postman là công cụ hữu ích trong phát triển và kiểm thử phần mềm, đặc biệt khi làm việc với hệ thống sử dụng API.
