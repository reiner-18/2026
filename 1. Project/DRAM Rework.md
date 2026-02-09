# DRAM

Là một loại bộ nhớ truy cập ngẫu nhiên lưu mỗi bit dữ liệu trong một tụ điện riêng biệt trên một mạch tích hợp. Vì các tụ điện bị rò điện tích nên thông tin sẽ bị mất dần trừ khi dữ liệu được nạp lại đều đặn.

> [!info]- Khuôn của mạch tích hợp Micron Technology MT4C1024 DRAM (1994)
> ![[DRAM.jpg]]
> Nó có dung lượng 1 megabit tương đương với $2^20$ bits hoặc 128 KiB

Cấu trúc ô nhớ DRAM bao gồm một transitor và một tụ điện, cả hai đều dựa trên công nghệ bán dẫn oxit kim loại (MOS) %%Công nghệ bán dẫn (TSMC)%% 

Trong khi hầu hết DRAM sử dụng tụ điện và bóng bán dẫn, một số sử dụng hai bóng bán dẫn. Trong các thiết kế tụ điện, tụ điện có thể được tích điện hoặc phóng điện, nó có hai trạng thái đại diện cho hai giá trị của một bit, thường được gọi là 0 và 1. Điện tích trên tụ điện sẽ dần dần bị rò rỉ và nếu không có sự can thiệp thì dữ liệu trên tụ điện sẽ bị mất.

Để ngăn chặn điều này, DRAM yêu cầu một mạch làm mới bộ nhớ ngoài để ghi lại dữ liệu trong các tụ điện theo định kì, khôi phục chúng về mức sạc ban đầu. Đây cũng là đặc điểm khác biệt so với [[SRAM]] - không yêu cầu làm mới dữ liệu. Không giống như bộ [[Flash Memory|flash memory]], DRAM là bộ nhớ dễ thay đổi vì nó sẽ mất dữ liệu nhanh khi bị mất điện. Tuy nhiên, DRAM vẫn còn mặt hạn chế là [[Data Remanence|data remanence]].

DRAM thường có dạng chip tích [[integrated circuit|mạch tích hợp]], có thể mang tới hàng chục, hàng tỉ ô nhớ DRAM. Chip DRAM sử dụng hầu hết trên các thiết bị điện tử, nơi chúng cần dung lượng bộ nhớ cao, chi phí thấp.

Một trong những ứng dụng lớn nhất của DRAM là [[main memory|bộ nhớ chính]] (hay còn gọi là RAM) ở máy tính hiện đại và [[Graphics Card|graphics card]] trong đó RAM được gọi là bộ nhớ đồ họa. Nó cũng được sử dụng nhiều trong thiết bị di động và máy chơi game. Ngược lại, SRAM nhanh hơn và đắt hơn DRAM thường được sử dụng khi tốc độ được quan tâm nhiều hơn là kích thước, chẳng hạn như bộ nhớ đệm trong bộ xử lý.
## Lịch sử DRAM

## Nguyên tắc hoạt động

### Các thao tác đọc bit dữ liệu từ ô nhớ DRAM

### Ghi vào bộ nhớ

### Tốc độ làm mới

### Thời gian làm mới

## Thiết kế ô nhớ

### Thiết kế tụ điện

### Đề xuất thiết kế ô nhớ

## Cấu trúc mảng

### Kiến trúc bitline

#### Mảng bitline mở

#### Mảng bitline gấp

#### Kiến trúc mảng tương lai

### Hàng dự phòng và cột

## Phát hiện lỗi và sửa lỗi

## Bảo mật

### Dữ liệu còn sót lại

### Hỏng dữ liệu bộ nhớ