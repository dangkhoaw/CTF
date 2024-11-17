# Soluton

- Đây là hình ảnh đầu tiên khi vào trang challenge

![image](../src/Pizza%20Paradise/1.png)

- Khi mình nhấn thử các chức năng thì chẳng có gì đặc biệt

- Sau đó mình dùng tool dirsearch để tìm các file ẩn

```bash
dirsearch -u https://pizzaparadise.intigriti.io/ -t 50
```

- Sau khi quét mình thấy có 1 file `robots.txt` nên mình truy cập vài thử

![image](../src/Pizza%20Paradise/2.png)

- Trong file `robots.txt` có file `.html` nên mình truy cập thử

![image](../src/Pizza%20Paradise/3.png)

- Sau khi mình truy cập vào thì ra 1 trang login, và sau đó mình mở source ra xem

![image](../src/Pizza%20Paradise/4.png)

- Trong source mình thấy 1 file `auth.js` nên mình truy cập vào xem

![image](../src/Pizza%20Paradise/5.png)

- Trong file `auth.js` mình thấy username là `agent_1337` và password là `91a915...`. Password có ở dạng hash nên mình sẽ decode bằng web gì đó quên tên rồi :)) và nó ra `intel_...` (cái mật khẩu mình quên rồi)

- Sau khi mình đăng nhập bằng username `agent_1337` và password `intel_...` thì xuất hiện 1 trang mới. Trang này chỉ có chức năng dowload file ảnh (mình quên chụp ảnh trang này)

- Mở Burp Suite lên và bắt request khi mình download file ảnh

![image](../src/Pizza%20Paradise/6.png)

- Mình nghi bị path traversal nên mình thử

![image](../src/Pizza%20Paradise/7.png)
![image](../src/Pizza%20Paradise/8.png)
![image](../src/Pizza%20Paradise/9.png)

- Ồ, ở đây mình đã truy cập được file `/etc/passwd`

- Sau đó mình vào từng file trong source code của web để tìm flag

![image](../src/Pizza%20Paradise/10.png)

# Flag

`INTIGRITI{70p_53cr37_m15510n_c0mpl373}`
