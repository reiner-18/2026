# RAM 

RAM là gì một phần cứng trong máy tính, viết đầy đủ là Random Access Memory (Bộ nhớ truy cập ngẫu nhiên). Là một bộ nhớ tạm thời, tốc độ cao, dùng để lưu trữ dữ liệu và lệnh mà [[CPU]] cần xử lý ngay lập tức. 

> [!info] Hình ảnh về RAM
> ![[RAM_n.jpg]]

Chức năng chính của **RAM**

- Lưu trữ dữ liệu tạm thời: Giữ các tệp hệ điều hành, ứng dụng đang mở, dữ liệu game để CPU thao tác nhanh chóng.
- Đa nhiệm, Tăng tốc độ: Giúp CPU truy xuất thông tin nhanh hơn so với SSD/HDD, làm giảm thời gian chờ đợi, cho phép nhiều ứng dụng hoạt động cùng lúc mà không bị chậm, giật lag.

**Tính chất**

- **Tính tạm thời:** Dữ liệu trên RAM sẽ bị xóa khi mất điện hoặc tắt máy
- **Truy cập ngẫu nhiên:** CPU có thể truy cập bất kỳ ô nhớ nào một cách nhanh chóng, không cần tuần tự

## Lịch sử

Vào năm 1945, von Neumann đã giới thiệu ý tưởng lưu trữ dữ liệu và lệnh dưới dạng nhị phân trong một không gian bộ nhớ chung, có thể truy cập ngẫu nhiên thay vì tuần tự. Đây là một khái niệm mang tính cách mạng tại thời điểm đó, đặt nền móng cho máy tính hiện đại.

> [!info]- John von Neumann
> ![[JohnvonNeumann.jpg]]

Năm một 1946 đến 1948, ống Selectron được phát triển bởi RCA có khả năng lưu trữ từ 256 đến 4096 bit dữ liệu, làm cho nó trở thành một bước tiến đáng kể so với phương pháp lưu trữ trước đó là thẻ đục lỗ. Tuy nhiên, ống Selectron có chuy phí sản xuất đắt đỏ và tuổi thọ ngắn nên đã dẫn đến việc thay thế bằng các công nghệ mới

> [!info]- Ống Selectron
> ![[Selectron.png]]

Năm 1951, Jay Forrester tại MIT đã phát triển ra Bộ nhớ lõi từ, sử dụng các vòng từ nhỏ hoặc lõi, qua đó các dây được xâu vào thành một lưới. Bằng cách từ hóa các lõi này theo hướng khác nhau, dữ liệu có thể được lưu trữ và truy cập nhanh chóng. Bộ nhớ lõi từ là bộ nhớ không biến động, nó lưu trữ lại dữ liệu ngay cả khi tắt nguồn và phổ biến ở các máy tính như IBM 701.

> [!info]- Bộ nhớ lõi từ
> ![[bonholoitu.png]]

Vào năm 1960, quá trình chuyển đổi từ bộ nhớ lõi từ sang RAM bán dẫn cùng với sự phát triển của bộ nhớ SRAM. SRAM trở nên khả thi nhờ vào [[Transistor|transistor]] cực nối, cho phép thời gian truy cập nhanh hơn so với công nghệ trước đó.

Năm 1966, Robert Dennard của IBM phát minh ra bộ nhớ động (DRAM). DRAM sử dụng một transistor và một tụ điện cho mỗi bit, cho phép mật độ cao hơn nhiều so với SRAM. Intel 1103 là chip thương mại đầu tiên được giới thiệu vào năm 1970.

Thập kỉ 1980 và 1990 là sự phát triển mạnh mẽ của công nghệ DRAM với sự ra đời của EDO RAM và FPM RAM, dung lượng bộ nhớ liên tục cải tiến từ 16Kb lên 1Mb và hơn thế nữa. Đây cũng là giai đoạn phát triển mạnh của máy tính cá nhân, DRAM trở thành tiêu chuẩn của IBM PC.

Năm 1993, Bộ nhớ SDRAM đồng bộ được giới thiệu, đánh dấu sự thay đổi đáng kể trong công nghệ bộ nhớ. SDRAM đồng bộ hóa với xung nhịp [[CPU]], cho phép truyền dữ liệu hiệu quả hơn và hiệu suất hệ thống tổng thể tốt hơn. SDRAM dần thay thế FPM RAM và trở thành tiêu chuẩn cho các máy tính vào cuối thập niên 1980.

Cùng thời gian đó, bộ nhớ Rambus DRAM được phát triển như một giải pháp bộ nhớ hiệu suất cao cho các ứng dụng như đồ họa và game. Tuy nhiên RDRAM phải đối mặt với sức ép từ thị trường do chi phí sản xuất quá cao và yêu cầu cấp phép phức tạp. RDRAM thất bại trước các lựa chọn hiệu quả hơn như DDR SDRAM.

Thế kỉ 21 là kỷ nguyên của Double Data Data SDRAM, tăng gấp đôi tốc độ truyền dữ liệu của SDRAM truyền thống bằng cách truyền dữ liệu trên cả cạnh lên và cạnh xuống của tín hiệu xung nhịp. DDR SDRAM được giới thiệu vào năm 2000 và ảnh hưởng mạnh đến tính toán, cho phép tốc độ xử lý nhanh hơn và hiệu quả hơn. Các thế hệ tiếp theo bao gồm DDR2, DDR3, DDR4 và DDR5 tiếp tục cải tiến dựa trên cơ sở này và hiệu quả ngày càng vượt trội.

## Các nhà sản xuất RAM nổi tiếng 

Big Three trong ngành công nghiệp chip nhớ DRAM. không chỉ cung cấp các thanh ram mà còn cung cấp chip cho các nhà sản xuất điện thoại thông minh, máy chủ và data centre.

1. **Samsung Electronics**: Người khổng lồ, dẫn đầu về công nghệ. Thị phần ước tính 40% - 45%n
2. **SK Hynix**: Đối thủ của Samsung và là nhà sản xuất lớn thứ 2. Là công ty tiên phong trong công nghệ HBM, một loại bộ nhớ rất quan trọng cho các ứng dụng trí tuệ nhân tạo và data centre hiệu năng cao. Thị phần ước tính 25% - 30%
3. **Micron Technology**: Là nhà sản xuất DRAM lớn duy nhất của Hoa Kỳ. Micron sản xuất dưới thương hiệu riêng như Crucial và cũng cung cấp chip cho các nhà sản xuất khác. Thị phần khoảng 20% đến 25%.

> [!hint] Lưu ý
> Khi mua một thanh RAM như **Kingston, Corsair, G.Skill hay Crucial**, ta đang mua sản phẩm của các nhà sản xuất module và nhà đóng gói.
> - Các công ty này không tự sản xuất chip DRAM
> - Họ mua chip thô rồi sau đó láp ráp chúng lên bản mạch in (PCB), gắn tản nhiệt và bán ra thị trường với chế độ bảo hành riêng.
> 
> > Thị phần được nói ở trên là thị phần chip nhớ, không phải bán lẻ

## Phân loại RAM

RAM được chia làm hai loại chính: [[SRAM|RAM Tĩnh]] và [[DRAM|RAM Động]], trong đó DRAM phổ biến hơn và được chia thành nhiều thế hệ như DDR, DDR2, DDR3, DDR4, DDR5 với tốc độ và hiệu năng thăng tiến, trong khi SRAM dùng trong bộ nhớ cache có tốc độ cao.

Ngoài ra, còn có các loại RAM khác như VRAM, sử dụng trong việc xử lý hình ảnh, video tốc độ cao và Flash Memory là loại bộ nhớ không bay hơi (non-volatile) dùng trong USB, SSD.

LPDDR là RAM dành cho thiết bị di động, nó được thiết ké để tối ưu hóa cho ứng dụng di động, cải thiện hiệu quả năng lượng mà không ảnh hưởng đến hiệu suất.

GDDR được phát triển cho các đơn vị xử lý đồ họa cho GPU, đòi hỏi bộ nhớ tốc độ cao để xử lý các như cầu dữ liệu lớn của render hình ảnh và video. GDDR đã được phát triển cùng với GPU và được phát triển lên các phiên bản kế tiếp mạnh mẽ hơn như GDDR3, GDDR5 và GDDR6 (xem thêm về kiến trúc GPU của NVIDIA)

Trong đời đống thường ngày, người ta gọi RAM là nói về DRAM. Nhưng trong kĩ thuật, ta nên gọi tên rõ DRAM hoặc SRAM vì RAM gọi chung sẽ không rõ đang nói về cái gì, vì mặt bằng chung chúng đều là bộ nhớ truy cập ngẫu nhiên.

