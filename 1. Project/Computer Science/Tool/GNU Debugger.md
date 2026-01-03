# GDB

## Debug là gì ?

## Cách sử dụng

Điều kiện: luôn biên dịch mã với `-g` 

### Flow Control 

- break <vị trí>: Đặt điểm dừng
- run: chạy chương trình cho đến khi gặp điểm dừng
- next: chạy dòng lệnh tiếp theo. Step over các lời gọi hàm
- step: chạy dòng lệnh tiếp theo. Step into các lời gọi hàm
- continue: tiếp tục thực thi đến breakpoint tiếp theo hoặc hết chương trình
- finish: chạy nhanh cho đến khi hàm hiện tại kết thúc và dừng lại ở lệnh tiếp theo
- info b: hiển thị danh sách các breakpoint