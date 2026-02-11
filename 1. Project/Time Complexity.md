# Time Complexity

Trong khoa học máy tính, độ phức tạp về thời gian là độ phức tạp tính toán mô tả lượng thời gian máy tính cần để chạy thuật toán. Độ phức tạp về thời gian thông thường được tính bằng số lượng thao tác của thuật toán.

Vì thời gian chạy của mỗi thuật toán có thể là khác nhau giữa các đầu vào khác nhau cùng kích thước nên người ta thường xem xét độ phức tạp không gian trong trường hợp xấu nhất, là lượng thời gian tối đa cần thiết cho các đầu vào có kích thước nhất định.

Trong từng trường hợp khác nhau của dữ liệu đầu vào, việc tính toán chính xác hàm $f(x)$ (với $x$ tổng quát) thường rất khó. Và ở đây, chúng ta sử dụng chúng ta sử dụng Big O notation để thay thế.



---


[^1]: **Big O Notation**: Ký hiệu **Big O** là ký hiệu toán học mô tả kích thước gần đúng của hàm trên một miền. Big O là thành viên được phát minh ra bởi các thành viên nhà toán học người Đức Paul Bachmann và Edmund Landau và được những người khác mở rộng. Gọi chung là **Bachmann-Landau notation**. Chữ O được Bachmann chọn là viết tắt của Ordnung, nghĩa là thứ tự xấp xỉ.
	
	Trong Khoa học máy tính, kí hiệu Big O lớn được sử dụng để phân loại thuật toán theo yêu cầu về không gian hoặc thời gian chạy của chúng tăng lên khi kích thước đầu vào tăng lên. Trong lý thuyết số giải tích, ký hiệu Big O lớn được dùng để biểu thị giới hạn tăng dần của hàm số toán học; Một trong những ví dụ nổi tiếng là số hạng còn lại trong định lý số nguyên tố. Trong phân tích toán học, bao gồm giải tích Big O thường được sử dụng để giới hạn lỗi khi cắt bớt chuỗi lũy thừa và để thể hiện chất lượng gần đúng của một hàm có giá trị thực hoặc phức bằng một hàm đơn giản hơn.
	
	Thông thường, ký hiệu Big O lớn mô tả các hàm theo tốc độ tăng trưởng khi biến trở nên lớn. Các hàm khác nhau có cùng tốc độ tăng trưởng tiệm cận có thể Ký hiệu **Big O** là ký hiệu toán học mô tả kích thước gần đúng của hàm trên một miền. Big O là thành viên được phát minh ra bởi các thành viên nhà toán học người Đức Paul Bachmann và Edmund Landau và được những người khác mở rộng. Gọi chung là **Bachmann-Landau notation**. Chữ O được Bachmann chọn là viết tắt của Ordnung, nghĩa là thứ tự xấp xỉ.
	
	Trong Khoa học máy tính, kí hiệu Big O lớn được sử dụng để phân loại thuật toán theo yêu cầu về không gian hoặc thời gian chạy của chúng tăng lên khi kích thước đầu vào tăng lên. Trong lý thuyết số giải tích, ký hiệu Big O lớn được dùng để biểu thị giới hạn tăng dần của hàm số toán học; Một trong những ví dụ nổi tiếng là số hạng còn lại trong định lý số nguyên tố. Trong phân tích toán học, bao gồm giải tích Big O thường được sử dụng để giới hạn lỗi khi cắt bớt chuỗi lũy thừa và để thể hiện chất lượng gần đúng của một hàm có giá trị thực hoặc phức bằng một hàm đơn giản hơn.
	
	Thông thường, ký hiệu Big O lớn mô tả các hàm theo tốc độ tăng trưởng khi biến trở nên lớn. Các hàm khác nhau có cùng tốc độ tăng trưởng tiệm cận có thể  được biểu dđược biểu diễn bằng cùng ký hiệu Big O.
