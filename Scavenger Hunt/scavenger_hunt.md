# Solution

- Ở trang web chính, ta nhấn Ctrl + U để xem mã nguồn, trong source ta thấy part 1 của flag **picoCTF{t**
- Nhấn F12 để mở Developer Tools, chuyển sang tab **Nguồn** và tìm trong file .css, ta thấy part 2 **h4ts_4_l0**
- Bắt đầu từ đây, sử dụng tools **dirsearch** để tìm các file ẩn

```bash
dirsearch -u http://mercury.picoctf.net:55079/ -e * -t 50
```

- Sau khi quét xong, ta thấy được các file ẩn như `/robots.txt`, `/.htaccess`, `/.DS_Store`

- Vào `/robots.txt` ta lấy được part 3 **t_0f_pl4c**
- Vào `/.htaccess` ta lấy được part 4 **3s_2_lO0k**
- Vào `/.DS_Store` ta lấy được part 5 **\_74cceb07}**

# Flag

`picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_74cceb07}`
