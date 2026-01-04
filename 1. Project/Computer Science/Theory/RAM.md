# RAM 

**RAM** (viết tắt của **Random Access Memory)** là một loại bộ nhớ khả biến cho phép truy xuất read-write ngẫu nhiên đến bất kì vị trí nào trong bộ nhớ dựa vào địa chỉ ô nhớ. Thông tin lưu trên RAM là tạm thời, chúng sẽ bị mất đi khi không có nguồn điện cung cấp

**RAM** có một đặc tính là thời gian thực hiện thao tác đọc ghi đối với mỗi ô nhớ là như nhau, cho dù đang ở bất kỳ vị trí nào trong ô nhớ. Mỗi ô nhớ của RAM đều có một địa chỉ. Mỗi ô nhớ là 8 bit, tuy nhiên hệ thống lại có thể đọc ghi vào nhiều byte (2, 4, 8 byte) cùng một lúc. (Cơ chế này liên quan mật thiết với Structure Padding).

> [!info] Một số loại ram.
> Từ trên xuống: [^1]DIP, SIPP, [^2]SIMM 30 chân, SIMM 72 chân, [^3]DIMM (16 chân), DDR DIMM (184-chân)
> 
  ![[RAM_n.jpg]]

> [!abstract]- Mục lục
> - [[#Lịch sử|Lịch sử]]
> - [[#Các nhà sản xuất RAM nổi tiếng|Các nhà sản xuất RAM nổi tiếng]]
> - [[#Phân loại RAM|Phân loại RAM]]
> 	- [[#Phân loại RAM#RAM Tĩnh|RAM Tĩnh]]
> 	- [[#Phân loại RAM#RAM động|RAM động]]

## Lịch sử

- DRAM Intel 1103, ra đời năm 1970, là sản phẩm DRAM đầu tiên
- SDR và SDRAM cuối thập niên 90, thế hệ RAM đầu tiên được tích hợp trên laptop. Tốc độ chậm và bộ nhớ ít.
- [^4]DDR và [^5]SDRAM cuối 2003 đến cuối 2009. Tốc độ nhanh hơn và dung lượng lớn hơn (lên đến 4GB). Tiết kiệm năng lượng hơn so với DDR1. Phổ biến cùng thời điểm với Windows XP (2003).
- DDR3 và SDRAM ra mắt 2007, phổ biến cuối 2009 Tốc độ rất nhanh và dung lượng lớn (lên đến 16GB/thanh). Tiết kiệm năng lượng hơn 30% so với DDR2.
- DDR3L Ra mắt cùng với DDR3 (hợp tác với Kingston/Intel) Phiên bản Low-Power của DDR3, sử dụng điện thế 1.35V thay vì 1.5V. Thiết kế cho laptop cao cấp và máy chủ.
- DDR4 và SDRAM ra mắt sau 8 năm DDR3. Giảm điện năng tiêu thụ hơn, tăng số tùy chọn xng nhịp và chu kỳ (timing). Giới hạn xung nhịp lý thuyết vượt qua 2133 MHz của DDR3
- DDR5 và SDRAM Module 16GB đầu tiên vào tháng 11/2018. Tốc độ cao hơn và băng thông lớn hơn so với DDR4

> [!caution] Lưu ý
> - DIPP, SIMM, DIMM: mô tả hình thức vật lý của RAM. DIMM là chuẩn hiện đại.
> - DDR, DDR2, DDR3, etc: Mô tả công nghệ chip bên trong.

## Các nhà sản xuất RAM nổi tiếng

Big Three trong ngành công nghiệp chip nhớ DRAM. không chỉ cung cấp các thanh ram mà còn cung cấp chip cho các nhà sản xuất điện thoại thông minh, máy chủ và data centre.

1. **Samsung Electronics**: Người khổng lồ, dẫn đầu về công nghệ. Thị phần ước tính 40% - 45%n
2. **SK Hynix**: Đối thủ của Samsung và là nhà sản xuất lớn thứ 2. Là công ty tiên phong trong công nghệ HBM, một loại bộ nhớ rất quan trọng cho các ứng dụng trí tuệ hân tạo và data centre hiệu năng cao. Thị phần ước tính 25% - 30%
3. **Micron Technology**: Là nhà sản xuất DRAM lớn duy nhất của Hoa Kỳ. Micron sản xuất dưới thương hiệu riêng như Crucial và cũng cung cấp chip cho các nhà sản xuất khác. Thị phần khoảng 20% đến 25%.

> [!hint] Lưu ý
> Khi mua một thanh RAM như **Kingston, Corsair, G.Skill hay Crucial**, ta đang mua sản phẩm của các nhà sản xuất module và nhà đóng gói.
> - Các công ty này không tự sản xuất chip DRAM
> - Họ mua chip thô rồi sau đó láp ráp chúng lên bản mạch in (PCB), gắn tản nhiệt và bán ra thị trường với chế độ bảo hành riêng.
> 
> > Thị phần được nói ở trên là thị phần chip nhớ, không phải bán lẻ

## Phân loại RAM

Tùy theo công nghệ chế tạo của các nước trên thế giới, được chia làm hai loại

### RAM Tĩnh

RAM tĩnh hay là SRAM, là một loại bộ nhớ sử dụng công nghệ bán dẫn. Tĩnh nghĩa là bộ nhớ vẫn lưu dữ liệu nếu có điện, không như RAM động, cần được nạp lại thường xuyên.

![[6t-SRAM-cell.png]]

RAM tĩnh được chế tạo theo công nghệ theo công nghệ ECL (dùng trong CMOS VÀ BiCMOS). Mỗi bit nhớ gồm có các cổng Logic với 6 [[Transistor|bóng bán dẫn]] MOS SRAM là bộ nhớ nhanh, việc đọc không làm hủy nội dung của ô nhớ và thời gian thâm nhập bằng chu kỳ của bộ nhớ. Nhưng SRAM là một nơi lưu trữ các tập tin CMOS dùng cho việc khởi động máy.

| SRAM chủ yếu làm CPU Cache
### RAM động

Là một loại bộ nhớ truy cập ngẫu nhiên lưu mỗi bit dữ liệu trong một tụ điện riêng biệt trên một mạch tích hợp. Vì các tụ điện bị rò điện tích nên thông tin sẽ bị mất dần trừ khi dữ liệu được nạp lại đều đặn. 

![[Dram_zelle.png|1000]]

Ưu điểm của DRAM là có cấu trúc đơn giản: chỉ cần có transistor và một tụ điện cho mỗi bit trong khi cần 6 transistor với SRAM. Điều này cho phép DRAM lưu trữ với mật độ cao. Vì DRAM mất dữ liệu khi không có điện nên nó thuộc loại thiết bị nhớ tạm thời.

Bộ nhớ DRAM chậm hơn rẻ tiền hơn SRAM

| DRAM được dùng làm bộ nhớ chính (RAM

> [!note] So sánh
> - SRAM: Nhanh hơn DRAM khoảng 10 lần, không cần làm mới dữ liệu và không nhạy cảm với nhiễu điện, nhưng đắt đỏ
> - DRAM: Chậm hơn do cấu tạo dựa trên tụ điện, phải làm mới dữ liệu sau mỗi 10 đến 100 mili giây để tránh mất dữ liệu, bù lại có giá thành rẻ hơn và mật độ lưu trữ cao.
### Các loại DRAM

- **SDR DRAM (Single Data Rate)**: Loại cũ, không còn phổ biến, tốc độ thấp
- **DDR SDRAM (Double Data Rate)**: Cải tiến từ SDR, truyền tải dữ liệu hai lần mỗi chu kỳ xung nhịp. Gồm các thế hệ:
	- **DDR1, DDR2, DDR3, DDR4, DDR5, DDR6** (Đang trong giai đoạn phát triển)
- **LPDDR (Low Power DDR)**: Thiết kế tiết kiệm điện năng tối đa, dùng cho điện thoại, máy tính bảng.
- **GDDR (Graphics DDR)**: Tối ưu cho card đồ họa, xử lý dữ liệu đồ họa nhanh, gồm GDDR5, GDDR6
- **HBM (High Bandwidth Memory)**: Băng thông cực cao, dùng cho các ứng dụng đòi hỏi hiệu suất đỉnh cao (AI, máy chủ).

### Phân loại theo ứng dụng và công nghệ

- **DRAM thông thường:** Dùng trong máy tính, PC, Laptop (DDR4, DDR5)
- ECC DRAM (Error-Correcting Code): Có khả năng tự sửa lỗi, dùng cho các ứng dụng đòi hỏi hiệu suất cao.

## Các thông số của RAM

Được phân loại theo chuẩn JEDEC.

### Dung lượng

Dung lượng RAM được tính bằng MB và GB, thông thường RAM được thiết kế với các dung lượng 256 MB, 512 MB, 1GB, 2 GB, 3GB, 4 GB, 6 GB, 8 GB, 16 GB, 32 GB, ... Dung lượng của RAM càng lớn càng tốt cho hệ thống, tuy nhiên không phải tất cả hệ thống phần cứng và hệ điều hành đều hỗ trợ các loại RAM dung lượng lớn.
### BUS

BUS là thông số đại diện cho "độ rộng và tốc độ của đường truyền dữ liệu".

**Phân loại**

Có hai loại BUS: BUS Speed và BUS Width.

- BUS Speed chính là BUS RAM, là tốc độ được xử lý trong một giây
- BUS Width là chiều rộng của bộ nhớ, các loại RAM DDR, DDR2, DDR3, DDR4, DDR5 hiện nay đều có BUS Width cố định là 64

Công thức tính bằng thông (bandwidth) từ BUS Speed và BUS Width:

> **Bandwidth = (Bus Speed x Bus Width) / 8**

Bandwidth là tốc độ tối đa RAM có thể đọc được trong một giây. Bandwidth được ghi trên RAM là con số tối đa theo lý thuyết. Trên thực tế, bandwidth thường thấp hơn và không thể vượt quá được con số lý thuyết.

### Độ trễ (Latency)

Latency hay còn gọi là **thời gian truy cập**, đóng vai trò cực kỳ quan trọng trong hiệu suất tổng thể của hệ thống vì nó quyết định tốc độ dữ liệu được cung cấp cho bộ vi xử lý.

#### 1. RAM trong hệ thống phân cấp độ trễ

Trong hệ thống lưu trữ, các thiết bị nằm càng gần CPU thì càng nhanh và có độ trễ càng thấp. RAM (bộ nhớ chính) có độ trễ lớn hơn nhiều so với các tầng ở phía trên nó:

- **Thanh ghi CPU (Registers):** Độ trễ bằng 0 chu kỳ (truy cập ngay lập tức trong quá trình thực thi lệnh)
- **Bộ nhớ đệm (Cache L1-L3):** Mất khoảng 4 đến 75 chu kỳ CPU
- **Bộ nhớ chính (RAM):** Tốn tới hàng trăm chu kỳ CPU
- **Đĩa cứng (Disk):** Chậm nhất với độ trễ lên đến hàng triệu chu kỳ

#### 2. Khoảng cách hiệu suất (Processor-Memory Gap)

Một thực trạng đáng chú ý là **tốc độ CPU đang twang nhanh hơn nhiều so với tốc độ của RAM**. Kể từ năm 1985, thời gian truy cập của SRAM (dùng cho cache) đã giảm khoảng 100 lần, nhưng thời gian truy cập của DRAM chỉ giảm khoảng 10 lần. Điều này tạo ra một khoảng cách hiệu suất ngày càng lớn, khiến cho bộ nhớ chính trở thành nút thắc cổ chai buộc CPU phải chờ đợi dữ liệu lâu hơn.

#### 3. "Hình phạt" khi lỡ nhịp bộ nhớ (Miss Penalty)

Khi dữ liệu không có sẵn trong các tầng bộ nhớ đệm, hệ thống phải truy vấn xuống tầng thấp hơn, gây ra khoảng thời giờ gọi là **miss penalty**.

- Nếu CPU không tìm thấy dữ liệu ở L1 và phải lấy từ L2: mất khoảng 10 chu kỳ
- Nếu phải lấy từ L3: mất khoảng 50 chu kỳ
- Nếu phải lấy trực tiếp từ RAM chính: hệ thống phải mất 200 chu kỳ

## Phân tính hình ảnh thực tế từ RAM

![[VietTai-RAM.png]]
--- 
[^1]: Dual In-line Package
	- **Thời kỳ**: 1970 - 1980
	- **Đặc điểm**: Không phải là một thanh RAM theo nghĩa hiện đại, mà là các **chip RAM riêng lẻ**  (individual chip) được hàn trực tiếp hoặc cắm và các ổ cắm trên bo mạch chủ.
	- **Cấu trúc:** Chip có hai hàng chân cắm song song.


[^2]: Single In-line Memory Module
    - **Thời kỳ:** Thập niên 1980 - Giữa 1990
	- **Đặc điểm:** Là module đầu tiên kết hợp nhiều chip RAM thành một thanh duy nhất, dễ dàng cắm và tháo ra.
	- **Cấu trúc:** Các chân cắm (pins) ở hai mặt trước và sau của thanh RAM được kết nối với nhau
	- **Phân loại:** 
		- 30-chân: Tiêu chuẩn cũ hơn, thường yêu cầu 4 hoặc 8 thanh cắm cùng lúc để đạt đủ chiều rộng bus dữ liệu
		- 72-chân: Phổ biến hơn, cho phép truyền tải 32-bit dữ liệu.

[^3]: Dual In-line Memory Module
	- **Thời kỳ**: Từ giữa thập niên 1990 đến nay.
	- **Đặc điểm:** Đây là tiêu chuẩn module thống trị cho hầu hết máy tính để bàn và máy chủ hiện đại
	- **Cấu trúc:** CÁc chân cắm ở mặt trước và mặt sau của thanh RAM độc lập với nhau (tạo thành hai đường tín hiệu riêng biệt).
	- **Phân loại theo số chân cắm)
		- 168-chân: Dùng cho SDR và DDR1
		- 184-chân: Dùng cho DDR1
		- 240-chân: Dùng cho DDR2 và DDR3
		- 288-chân: Dùng cho DDR4 và DDR5
	- SO-DIMM (Small Outline DIMM):** Phiên bản nhỏ hơn của DIMM, được sử dụng cho Laptop và các hệ thống nhỏ gọn
[^4]: **Double Data Rate**: Cải tiến lớn nhất là truyền tải dữ liệu hai lần trên mỗi chu kỳ xung nhịp (cạnh lên và cạnh xuống), điều này làm tăng gấp đôi hiệu suất truyền tải mà không cần tăng số lượng xung nhịp quá nhiều.

[^5]: **Synchronous DRAM**: RAM đồng bộ với xung nhịp hệ thống (Trước đó là Asynchronous RAM)


