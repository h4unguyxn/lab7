# API Testing with Thunder Client

## 1. Thông tin bài thực hành

- **Họ và tên:** Nguyễn Xuân Hậu
- **Môn học:** Software Testing
- **Chủ đề:** API Testing
- **Công cụ:** Thunder Client
- **Môi trường:** Visual Studio Code

## 2. Giới thiệu

Thunder Client là một extension trên Visual Studio Code hỗ trợ gửi HTTP Request và kiểm thử API trực tiếp trong môi trường lập trình.

Trong bài thực hành này, em sử dụng Thunder Client để thực hiện các thao tác kiểm thử API cơ bản.

Các nội dung đã thực hiện:

- GET Request
- POST Request
- PATCH Request
- DELETE Request
- Query Parameters
- Headers
- JSON Body
- API Testing
- Kiểm tra HTTP Status Code
- Kiểm tra dữ liệu Response

## 3. Mục tiêu

Mục tiêu của bài thực hành:

1. Hiểu cách hoạt động của HTTP Request và Response.
2. Biết sử dụng công cụ để kiểm thử API.
3. Thực hiện các phương thức HTTP phổ biến.
4. Biết gửi dữ liệu JSON đến API.
5. Biết kiểm tra HTTP Status Code.
6. Biết viết Test để kiểm tra kết quả trả về.
7. Ghi nhận và đánh giá kết quả kiểm thử.

## 4. Công cụ và môi trường

| Thành phần | Thông tin |
|---|---|
| Operating System | Windows |
| IDE | Visual Studio Code |
| API Testing Tool | Thunder Client |
| Protocol | HTTP/HTTPS |
| Data Format | JSON |
| Test Script | JavaScript |

## 5. Thực hành API

### 5.1. GET Request

GET được sử dụng để lấy dữ liệu từ server.

**Request:**

    GET https://postman-echo.com/get

API trả về HTTP Status Code `200 OK`.

**Hình ảnh minh họa:**

![GET Request](screenshots/01-test.png)

### 5.2. POST Request

POST được sử dụng để gửi dữ liệu đến server.

**Request:**

    POST https://postman-echo.com/post

**Request Body:**

    {
        "name": "Nguyen Xuan Hau",
        "student_id": "123456"
    }

API trả về HTTP Status Code `200 OK`.

**Hình ảnh minh họa:**

![POST Request](screenshots/02-test.png)

### 5.3. PATCH Request

PATCH được sử dụng để cập nhật một phần dữ liệu.

**Request:**

    PATCH https://postman-echo.com/patch

**Request Body:**

    {
        "name": "Nguyen Xuan Hau Updated"
    }

API trả về HTTP Status Code `200 OK`.

**Hình ảnh minh họa:**

![PATCH Request](screenshots/03-test.png)

### 5.4. DELETE Request

DELETE được sử dụng để gửi yêu cầu xóa dữ liệu.

**Request:**

    DELETE https://postman-echo.com/delete

API trả về HTTP Status Code `200 OK`.

**Hình ảnh minh họa:**

![DELETE Request](screenshots/04-test.png)

## 6. Query Parameters

Query Parameters được sử dụng để truyền thêm dữ liệu thông qua URL.

Ví dụ:

    GET https://postman-echo.com/get?name=Hau&age=21

Các tham số:

| Parameter | Value |
|---|---|
| name | Hau |
| age | 21 |

Server nhận được các tham số được truyền trong URL.

**Hình ảnh minh họa:**

![Query Parameters](screenshots/01-test.png)

## 7. Headers

HTTP Headers được sử dụng để truyền các thông tin bổ sung trong request.

Ví dụ:

    Content-Type: application/json

Header này cho server biết dữ liệu gửi lên có định dạng JSON.

## 8. JSON Body

Đối với POST và PATCH Request, dữ liệu được gửi dưới dạng JSON.

Ví dụ:

    {
        "name": "Nguyen Xuan Hau",
        "student_id": "123456"
    }

JSON giúp dữ liệu giữa client và server có cấu trúc rõ ràng và dễ xử lý.

## 9. API Testing

Sau khi gửi request, em thực hiện kiểm thử response bằng Test Script.

### 9.1. Kiểm tra Status Code

Test được sử dụng:

    expect(response.status).to.equal(200);

Mục đích là kiểm tra API có trả về HTTP Status Code `200` hay không.

### 9.2. Kiểm tra Response Body

Test được sử dụng:

    expect(response.body).to.not.be.null;

Mục đích là kiểm tra API có trả về dữ liệu trong Response Body.

### 9.3. Kiểm tra thuộc tính JSON

Test được sử dụng:

    expect(response.body).to.have.property("args");

Mục đích là kiểm tra Response Body có chứa thuộc tính `args`.

**Kết quả Test:**

![API Testing](screenshots/05-test.png)

## 10. Kết quả thực hành

| Nội dung | Kết quả |
|---|---|
| GET Request | PASS |
| POST Request | PASS |
| PATCH Request | PASS |
| DELETE Request | PASS |
| Query Parameters | PASS |
| Headers | PASS |
| JSON Body | PASS |
| Status Code Testing | PASS |
| Response Body Testing | PASS |

## 11. Nhận xét

Thông qua bài thực hành, em đã hiểu được cách sử dụng Thunder Client để gửi HTTP Request và kiểm tra HTTP Response.

Em đã thực hiện được các phương thức HTTP cơ bản gồm GET, POST, PATCH và DELETE. Ngoài ra, em cũng tìm hiểu cách sử dụng Query Parameters, Headers và JSON Body.

Việc sử dụng Test Script giúp quá trình kiểm thử API rõ ràng hơn, đặc biệt trong việc kiểm tra Status Code và dữ liệu trả về.

## 12. Kết luận

Thunder Client là một công cụ thuận tiện để thực hiện kiểm thử API trực tiếp trong Visual Studio Code.

Qua bài thực hành, em đã có kiến thức cơ bản về API Testing và có thể sử dụng các HTTP Request phổ biến để kiểm tra hoạt động của API.

## 13. Tài liệu tham khảo

1. Postman Learning Center  
   https://www.postman.com/learn/

2. Postman Documentation  
   https://learning.postman.com/docs/

3. Video hướng dẫn Postman được cung cấp trong bài tập  
   https://www.youtube.com/watch?v=MFxk5BZulVU

4. Thunder Client  
   https://www.thunderclient.com/
