# DRAM

Là một loại bộ nhớ truy cập ngẫu nhiên lưu mỗi bit dữ liệu trong một tụ điện riêng biệt trên một mạch tích hợp. Vì các tụ điện bị rò điện tích nên thông tin sẽ bị mất dần trừ khi dữ liệu được nạp lại đều đặn. 

> [!info]- Khuôn của mạch tích hợp Micron Technology MT4C1024 DRAM (1994)
> ![[DRAM.jpg]]
> Nó có dung lượng 1 megabit tương đương với $2^20$ bits hoặc 128 KiB

Cấu trúc ô nhớ DRAM bao gồm một transitor và một tụ điện, cả hai đều dựa trên công nghệ bán dẫn oxit kim loại (MOS) %%Công nghệ bán dẫn (TSMC)%% 

%%Cần tìm hiểu thêm wiki tiêng anh%% 
## Lịch sử DRAM

## Nguyên tắc hoạt động

### Các thao tác đọc bit dữ liệu từ ô nhớ DRAM

### Ghi vào bộ nhớ

### Tốc độ làm mới

### Thời gian làm mới

## Thiết kế ô nhớ

### Thiết kế tụ điện

%% Phần này giữ lại để xem thêm
## Cấu tạo vật lý

> [!note] Ngoại hình sơ bộ
> ![[VietTai-RAM.png]]

**Thông tin RAM:** 16GB 2Rx8 PC4-2666V-SE1-11

- 16GB: Thanh RAM có tổng dung lượng bộ nhớ là 16 GB
- 2R: Dual Rank, chip nhớ xuất hiện ở cả hai mặt, mỗi mặt đóng vai trò là một hàng địa chỉ dữ liệu riêng
- x8: Chiều rộng dữ liệu, mỗi chip nhớ DRAM trên thanh RAM có thể xử lý 8 bit dữ liệu tại một thời điểm. Đây là cấu hình phổ biến (Mỗi Rank dùng 8 chip x 8 bit = 64 bit).
- PC4: Thế hệ RAM DDR4
- 2666V: Tốc độ dữ liệu, tốc độ lý thuyết là 2666 MT/s (Meta Transfers per second). Đây là tốc độ BUS ổn.
- -S: Loại module SO-DIMM, đây là loại RAM dùng cho Laptop
- -E1: Loại bộ nhớ ECC
- -11: Timing/CAS Latency, trong trường hợp này là CL19 (Độ trễ chính thức của PC4 - 2666V).
### Chip SDP

Là một con chip nhớ nhỏ (thường là chip EEPROM) được đặt trên bo mạch của RAM, có chức năng lưu trữ thông tin kỹ thuật chi tiết về thanh RAM đó, bao gồm:

- Loại bộ nhớ
- Dung lượng
- Tốc độ xung nhịp
- Độ trễ hay thời gian truy cập
- Điệp áp hoạt động tiêu chuẩn

### Tụ điện

Lọc nhiễu và ổn định áp

- Lọc nhiễu: Hấp thụ và làm giảm thiểu nhiễu điện cao tầng xuất hiện trên đường cấp nguồn
- Ổn định nguồn: Cung cấp một nguồn điện dự trữ nhỏ và nhanh cho toàn bộ thanh RAM
### Điện trở

Điều chỉnh tín hiệu và giảm phản xạ

- Điện trở kết thúc: Giảm phản xạ tín hiệu và cải thiện chất lượng tín hiệu
- Điện trở cầu chì và giới hạn dòng: Đôi khi được sử dụng để giới hạn dòng điện đi vào một số mạch nhạy cảm hoặc một dạng bảo vệ cơ bản. Chúng giúp phân phối và điều chỉnh mức điện áp hoặc dòng điện đến vị trí cụ thể trên thanh RAM.

### Chíp nhớ

Memory Chip hay còn gọi là DRAM IC là thành phần cốt lõi quan trọng nhất của RAM. Chúng là nơi lưu trữ dữ liệu tạm thời cho hệ thống máy tính.

- Cấu tạo: Chíp nhớ DRAM là các hình khối chữ nhật màu đen, được hàn thành hàng trên bo mạch PCB của thanh RAM.
- Chức năng: 
	- Lưu trữ dữ liệu: Mỗi chíp nhớ chứa hàng tỉ ô nhớ DRAM, mỗi ô nhớ là một cặp [[Transistor]] và tụ điện lưu trữ một bit dữ liệu
	- Tổ chức: Các ô nhớ này được tổ chức thành các Banks, sau đó là hàng và cột, cho phép điều khiển bộ nhớ try cập dữ liệu theo địa chỉ cụ thể một cách nhanh chóng.
	- Đầu ra dữ liệu (Data Width): Chíp nhớ thường được định danh theo chiều rộng dữ liệu mà chúng có thể xử lý tại một thời điểm (x4, x8 hoặc x 16).
		- Thanh RAM tiêu chuẩn (Non-ECC) có tổng chiều rộng dữ liệu là 64 bit
		- Để đạt được 64 bit, thanh RAM thường cần 8 chíp nhớ (8 chip * 8 bit/chip = 64 bit).
	- Phân loại theo hàng
		- Single Rank (1R): chỉ có một hàng dữ liệu, CPU chỉ tốn mất 1 chu kỳ để truy cập.
		- Dual Rank (2R): Có hai hàng địa chỉ dữ liêu độc lập.
		- Quad Rank (4R): Có 4 hàng dữ liệu
		
> [!danger] Ghi chú
Chíp nhớ ở hai mặt của thanh RAM không có nghĩa là nó Dual Rank, điều đó tùy thuộc vào cách chíp nó đó được kết nối với bộ điều khiển bộ nhớ. Tuy nhiên, đa số trường hợp RAM máy tính cá nhân hiện đại thường tương ứng với Dual Rank.

### Thanh kết nối

Chân cắm (Edge Connector) là lớp kim loại được mạ vàng để đảm bảo khả năng dẫn điện và chống ăn mòn.

Mỗi chân cắm (pin) trên thanh kết nối có một nhiệm vụ cụ thể và quan trọng:

Đường truyền Dữ liệu (Data Lines):
  
  - Mang dữ liệu thực tế (các bit 0 và 1) giữa các chip nhớ DRAM trên thanh RAM và Bộ điều khiển Bộ nhớ (Memory Controller) trên CPU/Chipset.   
  - Chuẩn RAM máy tính cá nhân hiện đại có chiều rộng bus dữ liệu là **64 bit**.
  
Đường truyền Địa chỉ (Address Lines):
 
- Cho phép Memory Controller xác định **vị trí (địa chỉ)** cụ thể trong chip nhớ DRAM mà nó muốn đọc hoặc ghi dữ liệu.
 
Đường truyền Điều khiển (Control Lines):
  
- Truyền các lệnh điều khiển như **Read (Đọc)**, **Write (Ghi)**, **Refresh (Làm mới)**, và **Activate (Kích hoạt)** giữa Memory Controller và thanh RAM.

Đường cấp Nguồn (Power Lines):

  - Cung cấp điện áp hoạt động cần thiết cho thanh RAM (ví dụ: 1.2V cho DDR4, 1.1V cho DDR5).

Đường Đất (Ground Lines):
 
- Hoàn thành mạch điện và duy trì điện áp tham chiếu ổn định.
### Đường mạch

Là những đường dẫn bằng đồng mỏng được in chìm hoặc khắc trên bo mạch in (PCB), có nhiệm vụ mang dữ liệu, tín hiệu điều khiển và nguồn điện giữa các linh kiện.

 Kết nối Điện tử:
- **Kết nối các Chip nhớ:** Nối các chân của chip nhớ DRAM với nhau và với các linh kiện hỗ trợ (như tụ điện, điện trở). 
- **Kết nối với Chân cắm:** Nối các chân cắm mạ vàng (Edge Connector) với tất cả các mạch trên bo mạch, truyền tải tín hiệu ra ngoài tới Bộ điều khiển Bộ nhớ (Memory Controller) của CPU.
        
Truyền tải Tín hiệu và Nguồn:
    
- Phân chia thành các nhóm chính: **Đường dữ liệu (Data Lines)**, **Đường địa chỉ (Address Lines)**, **Đường điều khiển (Control Lines)**, và **Đường nguồn/Đất (Power/Ground Lines)**.

Thiết kế tối ưu: Với tốc độ xung nhịp cực cao của RAM hiện đại (hàng GHz), thiết kế đường mạch không chỉ đơn thuần là việc nối dây. Nó là một bài toán phức tạp trong kỹ thuật điện tử để đảm bảo **Tính Toàn vẹn Tín hiệu (Signal Integrity)**.

- **Chiều dài Đồng nhất (Length Matching):** Các đường mạch mang cùng một loại tín hiệu (ví dụ: các đường dữ liệu 64 bit) phải có **chiều dài gần như nhau** (thường chênh lệch chỉ vài micrômet). 
	- **Mục đích:** Đảm bảo rằng tất cả các bit dữ liệu đến đích (ví dụ: chip nhớ DRAM) **cùng một lúc**. Nếu không, sự chênh lệch thời gian (Skew) sẽ gây ra lỗi đọc/ghi dữ liệu.
- **Đường cong serpentine (Serpentine Traces):** Bạn sẽ thấy các đường mạch uốn lượn như hình rắn bò.
  - **Mục đích:** Đây là kỹ thuật để **kéo dài** một đường mạch ngắn hơn để nó bằng với chiều dài của các đường mạch dài hơn, duy trì nguyên tắc chiều dài đồng nhất.  
- **Tham chiếu (Reference Planes):** Các đường mạch thường được đặt gần một lớp đồng rộng (thường là lớp Đất - Ground) trong các lớp bên trong của PCB.
  - **Mục đích:** Cung cấp đường dẫn trở về ổn định và giúp kiểm soát **trở kháng** (Impedance) của đường truyền, chống lại nhiễu điện từ.
### Rãnh khóa

- Trên mỗi thế hệ RAM (DDR3, DDR4, DDR5), vị trí của **rãnh khóa** (một vết cắt nhỏ ở giữa thanh kết nối) là **duy nhất** và khác nhau.
- **Chức năng:** Đảm bảo rằng thanh RAM chỉ có thể được cắm vào khe cắm tương ứng trên bo mạch chủ, **ngăn chặn** việc cắm sai chuẩn (ví dụ: cắm DDR4 vào khe DDR3) có thể gây hỏng hóc vật lý và điện tử.
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

### Công nghệ XMP/EXPO

Là công nghệ cực kỳ quan trọng đối với người dùng muốn khai thác tối đa hiệu suất của RAM, đặc biệt là RAM hiệu năng cao (RAM Gaming

Theo chuẩn JEDEC, mọi thanh RAM bắt buộc phải khởi động ở cấu hình an toàn, ví dụ:

- DDR4: 2133 / 2400 / 2666 MHz
- DDR5: 4800 MHz

Tuy nhiên, BIOS không thể tự suy đoán timing/voltage và tần số [^6]OC này nên lưu sẵn cấu hình OC trong SDP của RAM

Các kit RAM “3200 MHz”, “3600 MHz”, “6000 MHz”… **không phải JEDEC**, mà là **overclock được nhà sản xuất kiểm nghiệm trước**.

**Mục đích** của XMP/EXPO là cho phép RAM hoạt động ở tốc độ **cao hơn nhiều** so với tốc độ tiêu chuẩn được thiết lập bởi JEDEC (tổ chức tiêu chuẩn công nghiệp) và cấu hình DRAM timing + voltage + clock ở mức phần cứng.

Kích hoạt: 

1. Khi người dùng cắm RAM vào máy tính, hệ thống mặc định chạy ở tốc độ JEDEC chậm nhất (4800MHz trên DDR5)
2. Người dùng phải truy cập vào BIOS/UEFI 
3. Tìm chọn kích hoạt XMP hoặc EXPO Profile
4. Khi kích hoạt, BIOS sẽ đọc thông số nâng cao từ chip SPD và áp dụng các giá trị Tốc độ, Độ trễ và Điện áp mới lên Bộ điều khiển Bộ nhớ (Memory Controller) của CPU.

Khi bật XMP BIOS sẽ:

1. Đọc profile từ SPD
2. Set memory controller + DRAM theo thông số

> Memory Overclock có kiểm soát

#### XMP

XMP (Extreme Memory Profile)

- Công nghệ của Intel
- Ra đời vào năm 2007
- Nền tảng: Z-series, B-series đời mới

#### EXPO

EXPO (Extended Profiles for Overclocking)

- **Chủ sở hữu**: AMD
- **Ra đời**: 2022 (cùng Ryzen 7000 / DDR5)
- **Mục tiêu**: Tối ưu cho **IMC + Infinity Fabric của AMD**

EXPO profile thường

- Chú trọng latency thực tế hơn MHz
- Tối ưu tỉ lệ MCLK : UCLK : FCLK
- Tránh các timing bất ổn trên Ryzen

> RAM DDR5 6000 EXPO ổn định hơn trên Ryzen 7000/8000 so với RAM chỉ có XMP
## Nguyên lý hoạt động nội tại (Cấu trúc phân tử)

**RAM** là một mảng cức lớn các transistor, mỗi linh kiện lưu 1 bit bằng điện tích, không phải logic 0 và 1

> 1 bit tương đương với có điện tích hoặc không có điện tích.

Đơn vị cơ bản: DRAM Cell (1T1C)

### Cấu trúc vật lý

Mỗi cell ram gồm hai thành phần: Transistor (ký hiệu là T) và Capacitor (Ký hiệu là C)

- [[Transistor]]: Hoạt động như một công tắc, quyết định khi nào đọc điện từ capacitor hay ghi điện vào capacitor
- Capacitor: Lưu trữ điện tích, có điện (1) hoặc không có điện (0)
### Bên trong DRAM Memory Cell

Ở mức vật liệu, T và C sẽ có các thành phần như sau

- Transistor: 
	- Silicon
	- Doping Boron / Phosphorus
	- Gate oxide $\text{SiO}_2$, $\text{HfO}_2$, ...
- Capacitor
	- Hai bản dẫn (electrode)
	- Giữa là dielectric siêu mỏng

> [!abstract] DDR hiệu đại dùng
> - High-k dielectric
> - Capacitor dạng trench hoặc stacked
> > Không có phần tử logic, chỉ có điện tích và vật liệu bán dẫn.

### Vì sao gọi là RAM động (DRAM)

Capacitor không giữ điện vĩnh viễn dẫn đến:

- Electron rò qua dielectric
- Nhiệt độ càng cao thì rò càng nhanh
- Công nghệ nhỏ thì rò càng nghiêm trọng

> Điều này dẫn đến hệ quả điện tích bị rò (leakage) và dữ liệu mất

Refresh: Mỗi cell phải được đọc ghi lại định kỳ mỗi 64ms (refresh cycle). Trong lúc refresh, RAM sẽ không phục vụ CPU dẫn đến latency nền.

Cơ chế đọc DRAM:

1. Transistor mở
2. Capacitor nối với bitline
3. Điện tích chia sẻ
4. Sence Aplifier đo sự chênh lệch

> [!warning] Vấn đề
> Điện tích bị xả một phần $\rightarrow$ bit bị phá hủy


DRAM Cycle: READ $\rightarrow$ AMPLIFY $\rightarrow$ WRITE BACK

%% Cần bổ sung %%
Pre-bank refresh & Fine-grain refresh 

### Tổ chức vật lý của DRAM

> [!info] Các cell được xếp thành ma trận
> ![[nternal-DRAM-organization-DRAM-is-organized-in-banks-each-of-which-contains-matrices-of.png]]

Khi kích hoạt 1 Row $\rightarrow$ Toàn bộ row được copy vào Row Buffer $\rightarrow$ CPU truy cập dữ liệu từ buffer, không trực tiếp từ cell

Điều này dẫn đến truy cập cùng row sẽ rất nhanh, còn khác row phải qua hai thao tác: đóng row cũ và mở row mới. Từ đó suy ra các timing

- tRCD
- tRP
- tRAS

#### Timing RAM 

Ví dụ:

```txt
DDR4-3200 CL16-18-18-36
```

| Thông số | Ý nghĩa                             |
| -------- | ----------------------------------- |
| CL       | Thời gian sense amplifier ổn định   |
| tRCD     | Kích hoạt row $\rightarrow$ đọc cột |
| tRP      | Đóng row                            |
| tRAS     | Thời gian row phải mở               |
> Đây là giới hạn vật lý của electron

#### DRAM Training

DRAM Training là IMC huấn luyện t
hực tế dựa trên XMP/EXPO cung cấp gợi ý

- IMC thử:
	- delay
	- voltage
	- drive strength
- Tìm điểm
	- Đọc đúng
	- Ghi đúng

IMC là lớp trung gian dịch lệch load/store thành activate/read/precharge

| $\Rightarrow$ Tối ưu RAM là tối ưu ở tầng vật lý

### Vấn của chip nhớ DRAM

Cell nằm sát nhau ở mức vật lý + C rất nhỏ và lượng electron cực ít $\rightarrow$ nhiễu điện là điều không thể tránh khỏi

### Hammering

RowHammer là lặp hàng trăm nghìn lần trong vài ms gọi là quá trình hammering

> Đây là sự vi phạm nguyên tắc cơ bản của vật lý bán dẫn, nơi nhiễu điện từ từ một linh kiện lân cận ảnh hưởng đến sự lưu trữ điện tích của tụ điện

Khi một row được activate

- Wordline của row được nâng điện áp
- Transistor của toàn bộ cell trên row mở
- Dòng điện lớn chạy qua: wordline $\rightarrow$ bitline $\rightarrow$ sense amplifier

Mỗi lần activate/precharge

- Điện trường thay đổi đột ngột, gây ra:
	- capacitive coupling
	- electromagnetic interference
- Các cell ở row kế bên không được activate nhưng vẫn bị ảnh hưởng bởi điện trường

## Bank, Bank Group & Memory-Level Parallelism

### DRAM Bank là gì ?

Một chip DRAM được chia thành nhiều Bank độc lập, mỗi Bank gồm:

- Hàng
- Cột
- Một Row Buffer riêng cho mỗi Bank

#### **Row Buffer** là gì ?

Là một vùng lưu trữ riêng biệt bên trong mỗi Bank Memory, đóng vai trò như một bộ nhớ đệm tạm thời cho toàn bộ một hàng dữ liệu

Quá trình đọc dữ liệu từ các ô nhớ DRAM gây mất điện tính trong tụ điện (đã nói ở phần [[#Vì sao gọi là RAM động (DRAM)|RAM động]]) nên dữ liệu phải chuyển vào Row Buffer.

**Các chức năng chính**

- Giảm độ trễ dữ liệu: Việc truy cập vào dữ liệu có sẵn gọi là row buffer hit nhanh đáng kể so với việc phải lấy dữ liệu trực tiếp từ mảng bộ nhớ (gọi là row buffer miss)
- Hỗ trợ đọc dữ liệu: Nó giữ dữ liệu trong quá trình khôi phục, đảm bảo thông tin không bị mất sau khi được truy cập
- Chọn lọc cột: mặc dù toàn bộ một hàng (thường từ 1KB đến 8KB) được chuyển vào bộ đệm, memory controller chỉ chọn 1 cột hoặc khối dữ liệu cụ thể đến CPU

**Vấn đề hiệu năng**

- Row Buffer Hit: Dữ liệu yêu cầu đã nằm sẵn trong bộ đệm từ lần truy cập trước $\rightarrow$ Độ trễ thấp nhất (Lệnh `READ`)
- Row Buffer Miss: Dữ liệu đang trống nên một hàng mới phải được kích hoạt $\rightarrow$ Độ trễ trung bình (Lệnh `ACTIVATE` $\rightarrow$ `READ`)
- Row Buffer Conflict: Một hàng khác đang nằm trong bộ đệm, nó phải được đóng lại trước khi hàng mới có thể mở ra $\rightarrow$ Độ trễ cao nhất (`PRECHARGE` $\rightarrow$ `ACTIVATE` $\rightarrow$ `READ`) gấp 2 lần so với miss và gấp 3 đến 4 lần so với hit

**Về thông số kĩ thuật***

Trong bộ nhớ DDR4 tiêu chuẩn, row buffer thường có độ rộng 8KB - 16KB, thực tế con số này tùy thuộc vào mật độ chip. Với các chip DDR4/DDR5 phổ thông hiện nay, mỗi Bank thường có một Row Buffer khoảng 1KB đến 2KB.

Chính sách quản lý

- Open-Page: Giữ cho buffer luôn mở sau khi truy cập, dự đoán rằng sẽ có thêm yêu cầu truy cập khác vào cùng hàng đó (Dùng trong PC/Server phổ thông)
- Closed-Page: Đóng hàng và nạp lại điện cho bộ nhớ ngay lập tức vì chúng các yêu cầu lần tiếp theo ít khi nằm chung một hàng, việc đóng hàng sớm giúp RAM luôn mở một hàng mới ở bất kỳ đâu mà không mất thêm thời gian chờ đóng hàng cũ (giảm thiểu Row Conflict) - Dùng trong hệ thống nhúng, Database.

**Vấn đề của DDR3**

DDR3 có nhiều Bank và tất cả các Bank nhưng lại bị giới hạn bởi kiến trúc nội tại của chip DRAM

Sơ bộ DDR3

- 8 hoặc 16 Bank mỗi chip
- Mỗi Bank có một Row Buffer riêng

$\Rightarrow$ Về mặt lý thuyết có thể xử lý nhiều request song song nhưng tất cả Bank lại dùng chung một internal data bus. (Bank có thể mở row song song nhưng chỉ cho phép truyền dữ liệu tại một thời điểm)

Ví dụ:

- Bank 0: ACTIVATE row A
- Bank 1: PRECHARGE
- Bank 2: ACTIVATE row B

Nhưng khi đến READ/WRITE thì tất cả xếp hàng trên một Bus nội bộ dẫn đến data bus bị serialize
%% Công việc sáng %%
### Memory-Level Parallelism 

## Prefetch & Brust Length

## Signal Integrity & Timing Margin

## Power Delivery & Noise

## Vì sao HBM gần như miễn nhiễm với RowHammer

%% Kết thúc bài viết %%
## Observable Effects

%% Kết thúc: chuyển sang note mới [[Memory Controller]] %%
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


[^6]: Overclocking Profiles là các tập hợp cài đặt tùy chỉnh (như tốc độ xung nhịp, điện áp, bộ nhớ) cho các linh kiện phần cứng (CPU, GPU, RAM) được lưu lại, cho phép người dùng áp dụng nhanh chóng các cấu hình ép xung hiệu năng cao khác nhau cho máy tính, thường thông qua phần mềm (như AI Overclocking của ASUS) hoặc BIOS/UEFI, để tối ưu hiệu suất cho từng tác vụ cụ (chơi game, render video), thay vì phải thiết lập thủ công mỗi lần.

%%