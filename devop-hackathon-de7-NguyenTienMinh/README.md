# 1. Kiểm tra mình đang là ai / đang ở đâu
whoami
pwd
ls -lah

# 2. Tạo user + cấp sudo
sudo adduser USER
sudo usermod -aG sudo USER
id USER
groups USER

# 3. Cập nhật và cài phần mềm
sudo apt update
sudo apt install -y TEN_GOI

# 4. Kiểm tra service
sudo systemctl status TEN_SERVICE
sudo systemctl start TEN_SERVICE
sudo systemctl restart TEN_SERVICE
sudo systemctl enable TEN_SERVICE

# 5. Firewall
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 22/tcp
sudo ufw allow PORT/tcp
sudo ufw enable
sudo ufw status numbered

# 6. Tạo/sửa file và thư mục
mkdir -p TEN_THU_MUC
nano TEN_FILE
cp FILE_NGUON FILE_DICH
chmod 644 TEN_FILE
chmod 755 TEN_THU_MUC
chown USER:GROUP TEN_FILE

# 7. Nginx
sudo nginx -t
sudo systemctl reload nginx

# 8. Kiểm tra cổng
sudo ss -tlnp

# 9. Test dịch vụ/web
curl http://127.0.0.1:PORT
curl -I http://127.0.0.1:PORT

# 10. Xem lỗi/log
sudo journalctl -u TEN_SERVICE -n 50
sudo tail -f /var/log/nginx/error.log

# 11. Lưu lịch sử bài thi
history > history.log

whoami
pwd
ls -lah

id
groups

sudo apt update
sudo apt install -y ...

sudo ufw allow 22/tcp
sudo ufw enable
sudo ufw status numbered

sudo nginx -t
sudo systemctl reload nginx
sudo systemctl status nginx

sudo ss -tlnp
curl -I http://127.0.0.1:PORT

history > history.log