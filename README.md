Minimal APIs Test

Mô tả

Chương trình Minimal APIs này cung cấp một API REST đơn giản để quản lý danh sách công việc cần làm (To-Do Items). API hỗ trợ các thao tác CRUD cơ bản: tạo, đọc, cập nhật và xóa mục công việc.

Mục tiêu 
- Xây dựng API tối thiểu bằng ASP.NET Core.
- Sử dụng controllers
- Test các ENDPOINTS

ENDPOINTS API

 ![image](https://github.com/user-attachments/assets/3a893e93-c4f4-4a5e-b01e-64747a2f7386)


Kết quả đạt được

1. Thêm một mục công việc mới

Phương thức: POST

Endpoint: /todoitems

Body (JSON):

{
  "name": "walk dog energy",
  "isComplete": true
}
![post_method](https://github.com/user-attachments/assets/075845c9-8bd4-4370-a422-f08e2c29041e)

Kết quả mong đợi:

Trả về một đối tượng JSON với thông tin mục công việc vừa được tạo, bao gồm id.

2. Lấy danh sách tất cả công việc

Phương thức: GET

Endpoint: /todoitems

![getall_method](https://github.com/user-attachments/assets/eeccddf9-d74d-48aa-b484-dbe5001b8420)


Kết quả mong đợi:

Trả về danh sách tất cả mục công việc dưới dạng JSON.

3. Lấy thông tin chi tiết một công việc theo ID

Phương thức: GET

Endpoint: /todoitems/{id}

![getone_method](https://github.com/user-attachments/assets/3a4ac9f5-d1a6-48fb-bc32-ddf66a85d18b)


Kết quả mong đợi:

Nếu ID hợp lệ, trả về thông tin chi tiết của công việc.

Nếu không tìm thấy ID, trả về lỗi 404 Not Found.

4. Lấy danh sách các công việc đã hoàn thành

Phương thức: GET

Endpoint: /todoitems/complete
![getcomplete_method](https://github.com/user-attachments/assets/9f099b48-ceb2-43f3-ad69-bd6a537287d0)

Kết quả mong đợi:

Trả về danh sách công việc có trạng thái isComplete: true.

5. Cập nhật một công việc theo ID

Phương thức: PUT

Endpoint: /todoitems/{id}

Body (JSON, ví dụ cập nhật tên công việc):

{
  "name": "updated task name",
  "isComplete": false
}
![put_method](https://github.com/user-attachments/assets/897140d8-2d10-4abd-ac3e-e71a4ae78b39)

Kết quả mong đợi:

Nếu ID hợp lệ, cập nhật thành công công việc.

Nếu không tìm thấy ID, trả về lỗi 404 Not Found.

6. Xóa một công việc theo ID

Phương thức: DELETE

Endpoint: /todoitems/{id}
![delete_method](https://github.com/user-attachments/assets/d03cab74-c74f-43d1-92fa-08efc6d84ad0)

Kết quả mong đợi:

Nếu ID hợp lệ, công việc bị xóa.

Nếu không tìm thấy ID, trả về lỗi 404 Not Found.

