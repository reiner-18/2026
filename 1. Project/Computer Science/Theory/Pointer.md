# Pointer

Con trỏ là một biến lưu địa chỉ ô nhớ.

## Các loại con trỏ

- Con trỏ dữ liệu cơ bản (Object Pointers)
- `void*` con trỏ "chưa biết kiểu"
- `char*` / `unsigned char*` con trỏ byte
- Con trỏ hàm (Function Pointer)
- Con trỏ mảng (Array-related Pointers)
	- `T*` trỏ tới phần tử đầu tiên của mảng
	- `T (*)[N]` - con trỏ tới cả mảng
- Con trỏ nhiều cấp (Multi-level pointers)
- Con trỏ hằng (Const-qualified pointers)
- Con trỏ cố định
	- `const T* p` 
	- `T* const p` - con trỏ cố định
	- `const T* const P`
	- Con trỏ tới struct / union
- Con trỏ thông minh

## Trạng thái con trỏ

- Con trỏ NULL
- Dangling pointer
- Wild pointer