## Hướng Dẫn Cài Đặt SSL Cho Website 

Bên gogetssl.com có cho đăng ký SSL trial 3 tháng. Thay vì mình dùng let's encrypt thì giờ dùng cái này nhé.

### Bước 1 - Generate Private Key và Public Key.

Cơ bản là bạn cần phải nhập thông tin như công ty, email website, bộ phận etc... để nó generate ra cho bạn 2 thứ đó chính là private key và public key dính liền với nhau. Ví dụ:

[Link generate GoGetSSL](https://www.gogetssl.com/online-csr-generator/) 

```markdown
Online CSR Generator
Your CSR for phancuong.ga
-----BEGIN CERTIFICATE REQUEST-----
MIICzTCCAbUCAQAwgYcxCzAJBgNVBAYTAkJCMQ4wDAYDVQQIDAUxMjMxMjESMBAG
A1UEBwwJMzEyMzEyMTIzMQ4wDAYDVQQKDAUxMjMxMjENMAsGA1UECwwEMzEyMzEV
MBMGA1UEAwwMcGhhbmN1b25nLmdhMR4wHAYJKoZIhvcNAQkBFg8zMTIzMTIzQGNh
LmNjb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDQm40VlaIfp2xL
2b7Fw7IoAh4VvQJZ5GGn/c72tn2ZEyB0OPTtIxbV7xllSz9HQqYEgLK5+vz1AjQr
WPdbLcT+OSlXtDqieYa1gUIerfVMfp7Jup+wVwSkllFNOiRtvi5VjGmwniRJlD2x
vY9uD2lU5bZdpdcEYVIQRntg+etEVRP0XcO7Y5xLEm7aNWrI/dx9k6tFUpzqgand
JzuZ8uTOJ8fwW+NbG795vgZWiz3ZVkaxDB02qryZo64zGamC6ehX5WuaIpB+0utg
iUHctfwL20ON9bRn4cUWGXeZ0l640Ex+4MCz9l2n5HV5zi06RKVvmPnHpnfD09fP
wFRT0sy7AgMBAAGgADANBgkqhkiG9w0BAQQFAAOCAQEAnSTlLdvu4YFPyiWTZ8M/
15iAF1yGLsXQf3NANyR4bTS53a4820MLQxZ70OnQscH/t6rKl+BHONafIfk0pXGS
WxRocsn6p0lzIpoJkIMJGIjQmJ1fxZlrSFKuN4KbNXw/6Dh4wjBTgEaU5eUaI4Ni
11RXjo5PzBRl4Rp+BA656MfltOTluOAXqO4Q2Gk6C+yB5D6CNI57/VldqR7r5lnI
paKe/GB4P9ImIPBwnRzeLSN+r+Kh7ZFxdN8gxjueya/V75kupSDi6i4lOHFDiZn8
pcc8lvv6Oyl0MCH7wQr5oxc3Y3CfgAu6iOZuFWeNK+kKy3IyaM/wmgO3xTO2gj2e
Rw==
-----END CERTIFICATE REQUEST-----
Your Private Server Key
-----BEGIN PRIVATE KEY-----
MIIEwAIBADANBgkqhkiG9w0BAQEFAASCBKowggSmAgEAAoIBAQDQm40VlaIfp2xL
2b7Fw7IoAh4VvQJZ5GGn/c72tn2ZEyB0OPTtIxbV7xllSz9HQqYEgLK5+vz1AjQr
WPdbLcT+OSlXtDqieYa1gUIerfVMfp7Jup+wVwSkllFNOiRtvi5VjGmwniRJlD2x
vY9uD2lU5bZdpdcEYVIQRntg+etEVRP0XcO7Y5xLEm7aNWrI/dx9k6tFUpzqgand
JzuZ8uTOJ8fwW+NbG795vgZWiz3ZVkaxDB02qryZo64zGamC6ehX5WuaIpB+0utg
iUHctfwL20ON9bRn4cUWGXeZ0l640Ex+4MCz9l2n5HV5zi06RKVvmPnHpnfD09fP
wFRT0sy7AgMBAAECggEBAJPMceRGFQy6UUdYagqyQWqJPYmHVcAcyHf+ooE4ALrQ
y2Cs7hOJledTNToIWzgA56EvEfIk+s4Ylp/Ts8V9IyI/m6QRBK4SzjeQ8ijMdYyR
9azVtch5jseR3N6LgD3kze08w7EoCmu7RQ7GUHXZI3bMHi4xjqsCzOLNHSMzTtYk
7GzDW8SHkAJ3CrIXL5eqjvLaQbRgdv6ZmOz4sr0nGStJj6olXpiytFTbrgEexH6i
Tq9wNpC1fhDAHmXnFZG1+34olQOP8p0yn8BIl3Jk7KaIrXMZxXXuJqfZdZSG16gQ
tjtS+xhhoMTJ4KCM8Tr7dHaV1a6e1F9p29nOfAM2RXkCgYEA/LxfgGStVcrxrHmi
pOfcybkBq+/RdN8ioi5enlePU71eXQNhIRN6S3p2qSt2wvSaBJn49lyJq0ia+G6k
AjJb0n45MczEUAn7Ap5Yp4cTMorsFP0kccvxQJZdNKb2HUmBZAcVliIICvEZOvCZ
JL6kX4aMgtfww4Pk2nzYAd4fAsUCgYEA001GnIXWirjgVGnQdpfZz20HVv9wzrCO
3FV5tvrTsd4hw21YkcjF5WAhlmGQWv8pbPf4HrQs1v7L29Nke4SabbW0FNFtGovI
czy0eNGxz4hetgBqtZdQ5Iesh5bvOG0x0XMbKvLOmT/JCDVAsINGV8X11LiQDybr
GH7O6B1xiX8CgYEAueGt99eUKNpXfzwC5HhnybGZSiTbD7MhXNjv3FOX5cYMhip7
IIGb27GZXnjKIz8VnDbGhiOvWVvQJtHxLHBvWlRdqoPpCtkcVWOy3pwZAX5tfk5k
pJGTwaYVrSjzML0kPjZ7qO0kry9+F/xnFkBk0qE57O33dUUnZ46UrGL6ueUCgYEA
qnErBBbxd/So/25bOU5D442O3h4uYIsKsbBA/dhV6qPDmGAbkXziJKPmc+c/CifI
wp1DB4FOqh3dUvSxmPDdoKFxIVnNKByZFFtjOBHt2/mkbCrp6JCmL7FA+h5F2L47
8TdoMryo6fUJtBVAmSFLHIISSgSWL6K1AI1JWPJnIwECgYEAmWGCkPRcbih7vKOy
mkuo2PGn3EL3Cs/AZf8daoGkRWcHy1k2QcoVs8NqPZYVxdj4URFZf7nH3XOhB6Cp
1P44msid1A7DgcFOE/FwY+qpp8K2faReF9/AyQ+H5spVfEboPl3wPESAkSBEOCZf
FKGnmW4RBiJLdnFBD2K6M+leVbI=
-----END PRIVATE KEY-----
```

Đấy, nó sẽ có dạng như thế. 

## Bước 2: Đi Mua SSL

Nếu mà bạn mua ở trên [GoGetSSL](https://my.gogetssl.com/) thì khi bạn thanh toán xong rồi, nó sẽ cho bạn nhập cái gọi là `CSR` thì lúc này, bạn cần phải paste cái phần public key vào đây (nó bao gồm cả cái ---END...) nhé.

## Bước 3: Xác Thực Website Này Thuộc Sở Hữu Của Bạn

Cái bước này nói chung kiểu gì cũng phải có. Nếu mà bạn xài Let's Encrypt ý, thì nó tự động luôn (Vì bạn làm trên hệ thống luôn mà :D ). 

Còn đối với [GoGetSSL](https://gogetssl.com) thì bạn cần phải upload cái file nó yêu cầu lên bằng tay.

Upload cũng dễ, nên khỏi nói nữa.

## Bước 4: Cấu Hình Lại cho Nginx

Thật sự mình rất lười nên mình Cài Certbot cho nó cấu hình mọi cái key basic của nó, định dạng nó .pem dạng như sau:
```markdown
listen 443 ssl; # managed by Certbot
    ssl_certificate /etc/nginx/ssl/phancuong_ga.crt; # managed by Certbot
    ssl_certificate_key /etc/nginx/ssl/priv.key; # managed by Certbot
    include /etc/letsencrypt/options-ssl-nginx.conf; # managed by Certbot
    ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem; # managed by Certbot
```

Không giống đâu, vì mình xóa chỉnh sửa một chút rồi.

Giờ bạn thay cái private.key: 
- Key này quan trọng, bạn giấu kỹ. Nếu mà thanh niên nào có được thì có được cái key này thì họ pro họ khai thác được bạn đấy. Cụ thể là gì thì các bạn cứ hóng blog mình đi, rãnh mình viết cho xem.
- Tạo cái file và cấu hình lại cho nginx

```markdown
ssl_certificate_key /etc/nginx/ssl/priv.key;
```

Còn cái certificate trên thì là cái key bạn mua từ trang web
```markdown
ssl_certificate /etc/nginx/ssl/phancuong_ga.crt;
```

Vô hiệu hóa mấy cái linh tinh:
```markdown
#include /etc/letsencrypt/options-ssl-nginx.conf; # managed by Certbot
#ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem; # managed by Certbot

```

## Bước 5: Restart lại nginx

`systemctl restart nginx`


Xong.