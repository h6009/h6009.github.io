## Hướng dẫn cài đặt Phalcon PHP Framework Cho Ubuntu 18.04
### Bước 1: Cài Đặt Các Gói Cần Thiết

```markdown
sudo apt install software-properties-common 
sudo add-apt-repository ppa:ondrej/php
sudo apt-get update
sudo apt-get install php7.3 curl php7.3-cli php7.3-fpm php7.3-json php7.3-pdo php7.3-mysql php7.3-zip php7.3-gd  php7.3-mbstring php7.3-curl php7.3-xml php7.3-bcmath php7.3-json
sudo apt install php7.3-phalcon
```

### Bước 2: Add Extension vào PHP.ini
```markdown
extension=phalcon.so
```

Sau đó restart lại dịch vụ
```mardown
sudo systemctl restart apache2
```

Bạn có thể kiểm tra bằng `phpinfo()` hoặc là lệnh cli `php -r 'print_r(get_loaded_extensions());'` hoặc `php -m`

### Lưu Ý:
1. Bạn không thể cài php7.3-phalcon nếu như bạn chưa cài php7.3 hoặc chưa có thư viện cài php7.3.
2. Bạn không thể sử dụng nếu bạn không thêm extension phalcon.so vào php.ini 