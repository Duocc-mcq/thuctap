CentOS a 

Before login
Chỉnh sửa trong tệp /etc/issue

After login
Chỉnh sửa trong tệp /etc/motd

Ubuntu

Before login
Chỉnh sửa trong tệp /etc/issue

After login
Chỉnh sửa trong /etc/update-motd.d/

Cronjob là các lệnh thực thi hành động đặt trước vào thời điểm nhất định. Crontab là nơi lưu trữ các cronjob.
Cron là một tiện ích giúp lập lịch chạy những dòng lệnh bên phía server để thực thi một hoặc nhiều công việc nào đó theo thời gian được lập sẵn.Một số người gọi những công việc đó là Cron job hoặc Cron task.
Cron là một chương trình deamon, tức là nó được chạy ngầm mãi khi được khởi động lên. Như các deamon khác thì bạn cần khởi động lại nó nếu như có thay đổi thiết lập gì.Chương trình này nhìn vào file thiết lập có tên crontab để thực thi những task được mô tả bên trong.
Một cron schedule đơn giản là một text file. Mỗi người dùng có một cron schedule,file này thường nằm trong /var/spoll/cron. Crontab files không cho phép bạn tạo hoặc chỉnh sửa trực tiếp với bất kì trình text editor nào, trừ khi bạn dùng lệnh crontab.
ví dụ: chạy script 30 phút 1 lần :

crontab -e: tạo hoặc chỉnh sửa file crontab

crontab -l: hiển thị file crontab

crontab -r: xóa file crontab

Hầu hết là crontab được cài đặt sẵn trên Linux, tuy nhiên vẫn có trường hợp không có. Nếu bạn sử dụng lệnh crontab -l mà thấy output trả lại: "-bash: crontab: command not found" thì cần cài crontab thủ công

Cài đặt crontab
Trên RedHat/Fedora/CentOS: yum install cronie

Trên Ubuntu/Debian: apt install cron

Start crontab và tự động chạy mỗi khi khởi động

systemctl start crond
systemctl enable crond