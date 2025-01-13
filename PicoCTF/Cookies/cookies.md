# Solution

- Mở Burp Suite
- Gửi request đến /check rồi dùng Burp Suite bắt request rồi đưa vào **Intruder**
- Tô đen giá trị của cookie và chọn **Add §**. Ví dụ `(Cookie: name=§2§)`
- Trong phần **Payloads**, chọn Payload type là Numbers, Start 1, End 30, Step 1
- Qua phần **Settings**, trong Grep - Match, và nhập vào `picoCTF{` để tìm kiếm flag
- Nhấn Start attack
- Done

# Flag

`picoCTF{3v3ry1_l0v3s_c00k135_96cdadfd}`
