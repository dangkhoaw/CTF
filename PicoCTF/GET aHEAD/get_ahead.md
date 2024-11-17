# Solution

- Tên challenge là `GET aHEAD`, đề bài cho ta biết là phải sử dụng `HEAD` request để lấy flag
- Đầu tiên, ta sẽ sử dụng `GET` request để lấy thông tin về trang web
- Sử dụng **Burp Suite** bắt request và thay đổi method từ `GET` thành `HEAD`
- Flag sẽ hiện ra trong response

# Flag

`picoCTF{r3j3ct_th3_du4l1ty_775f2530}`
