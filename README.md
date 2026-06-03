# Báo cáo thực hành kiểm thử API với Postman

## Thông tin sinh viên

* Họ và tên: Bùi Minh Đức
* Môn học: Đánh giá và Kiểm định Chất lượng Phần mềm

---

# 1. Mục tiêu

Tìm hiểu và thực hành sử dụng công cụ Postman để kiểm thử API. Thông qua bài thực hành, sinh viên làm quen với việc gửi các HTTP Request, kiểm tra Response và viết các kịch bản kiểm thử tự động bằng Postman.

---

# 2. Giới thiệu Postman

Postman là công cụ hỗ trợ phát triển và kiểm thử API phổ biến hiện nay. Công cụ này cho phép người dùng gửi các HTTP Request, phân tích Response, quản lý Collection và tự động hóa quá trình kiểm thử thông qua các Test Script.

Một số chức năng chính của Postman:

* Gửi HTTP Request (GET, POST, PUT, DELETE)
* Kiểm tra Response
* Quản lý Collection
* Viết Test Script bằng JavaScript
* Tự động chạy kiểm thử bằng Collection Runner

---

# 3. Thực hiện kiểm thử

API sử dụng trong bài thực hành:

https://jsonplaceholder.typicode.com

## 3.1. Kiểm thử GET Request

### Endpoint

```http
GET https://jsonplaceholder.typicode.com/posts/1
```

### Mục đích

Lấy thông tin bài viết có id = 1.

### Kết quả

* Status Code: 200 OK
* Dữ liệu trả về ở định dạng JSON.

### Hình minh họa

![GET Request](Screenshot%202026-06-03%20172855.png)

---

## 3.2. Kiểm thử POST Request

### Endpoint

```http
POST https://jsonplaceholder.typicode.com/posts
```

### Request Body

```json
{
  "title": "Postman Test",
  "body": "Learning API Testing",
  "userId": 1
}
```

### Mục đích

Tạo mới một bài viết.

### Kết quả

* Status Code: 201 Created
* Hệ thống trả về dữ liệu vừa được tạo.

### Hình minh họa

![POST Request](Screenshot%202026-06-03%20173009.png)

---

## 3.3. Kiểm thử PUT Request

### Endpoint

```http
PUT https://jsonplaceholder.typicode.com/posts/1
```

### Request Body

```json
{
  "id": 1,
  "title": "Updated Title",
  "body": "Updated Content",
  "userId": 1
}
```

### Mục đích

Cập nhật thông tin bài viết.

### Kết quả

* Status Code: 200 OK
* Dữ liệu được cập nhật thành công.

### Hình minh họa

![PUT Request](Screenshot%202026-06-03%20173138.png)

---

## 3.4. Kiểm thử DELETE Request

### Endpoint

```http
DELETE https://jsonplaceholder.typicode.com/posts/1
```

### Mục đích

Xóa bài viết có id = 1.

### Kết quả

* Status Code: 200 OK
* Yêu cầu xóa được thực hiện thành công.

### Hình minh họa

![DELETE Request](Screenshot%202026-06-03%20173229.png)


---

# 4. Kết quả đạt được

| Request | Kết quả |
| ------- | ------- |
| GET     | PASS    |
| POST    | PASS    |
| PUT     | PASS    |
| DELETE  | PASS    |

Tổng số Request đã kiểm thử: 4

Tổng số Test Script thực hiện thành công: 100%

---

# 6. Nhận xét

### Ưu điểm

* Giao diện trực quan, dễ sử dụng.
* Hỗ trợ nhiều phương thức HTTP.
* Dễ dàng viết và thực thi các Test Script.
* Hỗ trợ quản lý API theo Collection.

### Nhược điểm

* Một số tính năng nâng cao yêu cầu tài khoản trả phí.
* Cần kiến thức JavaScript để viết các bài kiểm thử phức tạp.

---

# 7. Kết luận

Qua bài thực hành, sinh viên đã làm quen với công cụ Postman và thực hiện thành công các phương thức GET, POST, PUT và DELETE. Đồng thời biết cách xây dựng các Test Script cơ bản để kiểm tra kết quả trả về của API. Đây là công cụ hữu ích trong quá trình kiểm thử phần mềm và phát triển các hệ thống sử dụng RESTful API.
