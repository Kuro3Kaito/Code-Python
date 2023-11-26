# Hệ điều hành Linux
## Ưu điểm của hệ thống Linux
1. Một hệ điều hành có mục đích chung không gắn liền với phần cứng cụ thể.
2. Được viết bằng ngôn ngữ C, nó có tính di động cao và có giao diện lập trình kernel.
3. Hỗ trợ nhiều người dùng và đa tác vụ, đồng thời hỗ trợ hệ thống tệp phân lớp an toàn.
4. Rất nhiều tiện ích, khả năng kết nối mạng toàn diện và tài liệu hỗ trợ mạnh mẽ.
5. Bảo mật đáng tin cậy và ổn định tốt, thân thiện với nhà phát triển hơn.

## Phiên bản phân phối hệ thống Linux
1. Redhat
2. Ubuntu
3. CentOS
4. Fedora
5. Debian
6. openSUSE

## Các lệnh cơ bản
Các lệnh hệ thống Linux thường có định dạng sau:
tên lệnh [tham số được đặt tên] [đối tượng lệnh]
1. Lấy thông tin đăng nhập - w / who / last / lastb
2. Kiểm tra Shell bạn đang sử dụng - ps
Hiện tại, shell mặc định của nhiều hệ thống Linux là bash (Bourne Again SHell), vì nó có thể sử dụng phím tab để hoàn thành các lệnh và đường dẫn, lưu các lệnh lịch sử, cấu hình các biến môi trường một cách thuận tiện và thực hiện các thao tác hàng loạt.
3. Xem mô tả và vị trí của lệnh - whatis / which / whereis
4. Xóa những gì hiển thị trên màn hình - clear
5. Xem tài liệu trợ giúp - man / info / --help / apropos
6. Xem hệ thống và tên máy chủ - uname / hostname
7. Thời gian và ngày - date / cal
8. Khởi động lại và tắt máy - reboot / shutdown
9. Đăng xuất - exit / logout
10. Xem lệnh lịch sử - history

## Tính thiết thực
Thao tác với tập tin và thư mục
1. Tạo/xóa các thư mục trống - mkdir / rmdir
2. Tạo/xóa tập tin - touch / rm
touch: Lệnh được sử dụng để tạo một file trống hoặc sửa đổi thời gian của file. Trong hệ thống Linux, một tệp có ba lần:
    Thời gian nội dung được thay đổi - mtime.
    Đã đến lúc thay đổi quyền - ctime.
    Lần truy cập cuối cùng - atime.
rm: Một số thông số quan trọng:
    -i: Xóa tương tác, bạn sẽ được hỏi về từng mục đã xóa.
    -r: Xóa một thư mục và xóa đệ quy các tập tin, thư mục trong thư mục đó.
    -f: Buộc xóa, bỏ qua các tập tin không tồn tại mà không có bất kỳ lời nhắc nào.
3. Chuyển sang và xem thư mục làm việc hiện tại - cd / pwd
4. Xem nội dung thư mục - ls .
    -l: Xem tập tin và thư mục ở định dạng dài.
    -a: Hiển thị các file và thư mục bắt đầu bằng dấu chấm (file ẩn).
    -R: Mở rộng đệ quy khi gặp một thư mục (tiếp tục liệt kê các tập tin và thư mục trong thư mục).
    -d: Chỉ liệt kê thư mục, không liệt kê nội dung nào khác.
    -S/ -t: Sắp xếp theo kích thước/thời gian.
5. em nội dung file - cat / tac / head / tail / more / less / rev / od
6. Sao chép/di chuyển tập tin - cp / mv
7. Đổi tên tập tin - rename
8. Tìm file và tìm nội dung - find / grep
9. Tạo liên kết và xem liên kết - ln / readlink
10. Nén/giải nén và lưu trữ/hủy lưu trữ - gzip / gunzip / xz
11. Lưu trữ và hủy lưu trữ - tar
12. Chuyển đổi đầu vào tiêu chuẩn thành đối số dòng lệnh - xargs
13. Hiển thị tập tin hoặc thư mục - basename / dirname .
14. Các công cụ liên quan khác.
    sort - Sắp xếp nội dung
    uniq - Loại bỏ các bản sao liền kề
    tr - thay thế nội dung được chỉ định bằng nội dung mới
    cut / paste – cắt/dán nội dung
    split - Tách một tập tin
    file - xác định loại tập tin
    wc - đếm số dòng, từ và byte trong một tệp
    iconv - chuyển đổi mã hóa

## Đường ống và chuyển hướng
1. Cách sử dụng ống - |
VD: Tìm file trong thư mục hiện tại: find ./ | wc -l
2. Chuyển hướng đầu ra và chuyển hướng lỗi - > / >> / 2>
3. Nhập chuyển hướng - <
4. Đa mục tiêu - tee

## Bí danh
1. Alias
2. unalias

## Xử lý van bản
1. Trình chỉnh sửa luồng ký tự - sed .
    sed là công cụ thao tác, lọc và chuyển đổi nội dung văn bản.
    Thay thế ký tự a trong văn bản bằng @.
    sed 's#a#@#' fruit.txt 
2. Ngôn ngữ xử lý và khớp mẫu - awk

## Quản lý người dùng
1. Tạo và xóa người dùng - useradd / userdel
    -d- Chỉ định thư mục chính của người dùng khi tạo người dùng
    -g- Chỉ định nhóm người dùng mà người dùng thuộc về khi tạo người dùng
2. Tạo và xóa nhóm người dùng - groupadd / groupdel
3. Thay đổi mật khẩu - passwd
    -l/ -u- Khóa/mở khóa người dùng.
    -d- Xóa mật khẩu người dùng.
    -e- Đặt mật khẩu hết hạn ngay lập tức và người dùng sẽ buộc phải thay đổi mật khẩu khi đăng nhập.
    -i- Đặt số ngày mà người dùng sẽ bị vô hiệu hóa sau khi mật khẩu hết hạn.
4. Xem và sửa đổi ngày hết hạn mật khẩu - chage
    Người dùng phải thay đổi mật khẩu sau 100 ngày. Người dùng sẽ được thông báo 15 ngày trước khi hết hạn và người dùng sẽ bị vô hiệu hóa 7 ngày sau khi hết hạn.
5. Chuyển đổi người dùng - su
6. Thực thi lệnh với tư cách quản trị viên - sudo
7. Chỉnh sửa tệp sudoers - visudo
8. Hiển thị thông tin người dùng và nhóm người dùng - id .
9. Gửi tin nhắn cho người dùng khác - write / wall
10. Xem/đặt có nhận tin nhắn do người dùng khác gửi hay không - mesg

## Hệ thống tập tin
### Tập tin và đường dẫn
1. Quy tắc đặt tên: Độ dài tối đa của tên tệp có liên quan đến loại hệ thống tệp. Nói chung, tên tệp không được vượt quá 255 ký tự.
2. Phần mở rộng: Phần mở rộng của tệp trong hệ thống Linux là tùy chọn, nhưng việc sử dụng phần mở rộng sẽ giúp hiểu được nội dung của tệp. Một số ứng dụng nhận dạng file theo phần mở rộng, nhưng nhiều ứng dụng không dựa vào phần mở rộng của file, giống như lệnh filekhông xác định loại file dựa trên phần mở rộng khi xác định file.
3. Tệp ẩn: Tệp bắt đầu bằng dấu chấm là tệp ẩn (tệp ẩn) trong hệ thống Linux.
### Cấu trúc thư mục
1. /bin - Tệp nhị phân cho các lệnh cơ bản.
2. /boot - Các tệp tĩnh cho bộ tải khởi động.
3. /dev - tập tin thiết bị.
4. /etc - Tệp cấu hình.
5. /home - thư mục mẹ của thư mục chính của người dùng bình thường.
6. /lib - Tệp thư viện được chia sẻ.
7. /lib64 - tệp thư viện 64-bit được chia sẻ.
8. /lost+found - lưu trữ các tập tin chưa được liên kết.
9. /media - Gắn thư mục để tự động nhận dạng thiết bị.
10. /mnt - Điểm gắn kết để gắn kết hệ thống tập tin tạm thời.
11. /opt - Vị trí cài đặt gói plug-in tùy chọn.
12. /proc - Thông tin hạt nhân và quy trình.
13. /root - Thư mục chính của người dùng quản trị viên cấp cao.
14. /run - lưu trữ những thứ cần thiết khi hệ thống đang chạy.
15. /sbin - Tệp nhị phân siêu người dùng.
16. /sys - Hệ thống tệp giả của thiết bị.
17. /tmp - Thư mục tạm thời.
18. /usr - Thư mục ứng dụng của người dùng.
19. /var - Thư mục dữ liệu biến.
### Quyền truy cập
1. chmod - Thay đổi bit chế độ tập tin
r:4 , w:2 , x:1
2. chown - Thay đổi chủ sở hữu tập tin
3. chgrp - Thay đổi nhóm người dùng
### Quản lý đĩa
1. Liệt kê việc sử dụng đĩa của một hệ thống tập tin - df 
2. Hoạt động bảng phân vùng đĩa - fdisk .
3. Công cụ phân vùng đĩa - parted .
4. Định dạng hệ thống tập tin - mkfs .
    -t- Chỉ định loại hệ thống tập tin.
    -c- Kiểm tra lỗi đĩa khi tạo hệ thống tập tin.
    -v- Hiển thị chi tiết.
5. Kiểm tra hệ thống tập tin - fsck .
6. Chuyển đổi hoặc sao chép tập tin - dd .
7. Gắn/tháo gắn kết - mount / umount .
8. Tạo/kích hoạt/đóng phân vùng trao đổi - mkswap / swapon / swapoff .
### Biên tập viên - vim

## Cài đặt và cấu hình phần mềm
### Sử dụng các công cụ quản lý gói
1. yum - Yellowdog Updater Modified。
    yum search: Tìm kiếm các gói, ví dụ yum search nginx.
    yum list installed: Liệt kê các gói đã cài đặt, yum list installed | grep zlibví dụ:
    yum install: Cài đặt các gói, ví dụ yum install nginx.
    yum remove:Xóa một gói, ví dụ yum remove nginx.
    yum update: Cập nhật các gói, ví dụ yum updatetất cả các gói đều có thể được cập nhật, nhưng yum update tarchỉ tar mới được cập nhật.
    yum check-update: Kiểm tra những gói có sẵn để cập nhật.
    yum info: Hiển thị thông tin liên quan của gói phần mềm, ví dụ yum info nginx.
2. rpm - Redhat Package Manager。
    Cài đặt gói: rpm -ivh <packagename>.rpm.
    Xóa gói: rpm -e <packagename>.
    Truy vấn các gói phần mềm: rpm -qa, chẳng hạn, có thể rpm -qa | grep mysqlđược sử dụng để kiểm tra xem các gói phần mềm liên quan đến MySQL đã được cài đặt chưa.

### Dịch vụ và cấu hình
1. Bắt đầu dịch vụ tường lửa.
    systemctl start firewalld
2. Chấm dứt dịch vụ tường lửa.
    systemctl stop firewalld
3. Khởi động lại dịch vụ tường lửa.
    systemctl restart firewalld
4. Kiểm tra trạng thái dịch vụ tường lửa.
    systemctl status firewalld
5. Đặt/tắt dịch vụ tường lửa để tự động khởi động khi khởi động.
    [root ~]# systemctl enable firewalld
    Created symlink from /etc/systemd/system/dbus-org.fedoraproject.FirewallD1.service to /usr/lib/systemd/system/firewalld.service.
    Created symlink from /etc/systemd/system/multi-user.target.wants/firewalld.service to /usr/lib/systemd/system/firewalld.service.
    [root ~]# systemctl disable firewalld
    Removed symlink /etc/systemd/system/multi-user.target.wants/firewalld.service.
    Removed symlink /etc/systemd/system/dbus-org.fedoraproject.FirewallD1.service.
### Nhiệm vụ lịch trình
1. Thực hiện lệnh tại thời điểm được chỉ định.
    at - xếp hàng một tác vụ sẽ được thực thi tại một thời điểm nhất định.
    atq - Xem hàng đợi các nhiệm vụ đang chờ xử lý.
    atrm - xóa tác vụ đang chờ xử lý khỏi hàng đợi.
2. Trình lập lịch biểu - crontab 
    Các file liên quan đến crontab đều nằm trong /etc, các tác vụ đã lên lịch cũng có thể được tùy chỉnh bằng cách sửa đổi file crontab trong thư mục.
### Truy cập và quản lý mạng
1. Kết nối từ xa an toàn - ssh .
2. Nhận tài nguyên qua mạng - wget .
    -b chế độ tải xuống nền
    -O Tải xuống thư mục được chỉ định
    -r tải xuống đệ quy
3. Gửi và nhận thư - mail .
4. Công cụ cấu hình mạng (cũ) - ifconfig .
5. Công cụ cấu hình mạng (mới) - ip .
6. Kiểm tra khả năng tiếp cận mạng - ping .
7. Hiển thị hoặc quản lý bảng định tuyến - route .
8. Xem các dịch vụ và cổng mạng - netstat / ss .
9. Giám sát mạng và chụp gói - tcpdump .
10. Sao chép tệp an toàn - scp .
11. Công cụ đồng bộ hóa tập tin - rsync 
12. Truyền tệp an toàn - sftp .
    help: Hiển thị thông tin trợ giúp.
    ls/ lls: Hiển thị danh sách thư mục từ xa/cục bộ.
    cd/ lcd: Chuyển đổi đường dẫn từ xa/cục bộ.
    mkdir/ lmkdir: Tạo thư mục từ xa/cục bộ.
    pwd/ lpwd: Hiển thị thư mục làm việc hiện tại từ xa/cục bộ.
    get:Tải tập tin.
    put:tải tập tin lên.
    rm: Xóa các tập tin từ xa.
    bye// exit: quit Thoát sftp. 
### Quản lý quy trình
1. Xem các quy trình - ps .
2. Hiển thị cây trạng thái tiến trình - pstree .
3. Tìm các quy trình phù hợp với tiêu chí đã chỉ định - pgrep .
4. Chấm dứt một tiến trình bằng ID tiến trình của nó - kill .
5. Tiêu diệt tiến trình theo tên tiến trình - killall / pkill .
6. Đặt quá trình chạy ở chế độ nền.
    Ctrl+Z- Phím tắt để dừng một quá trình và đặt nó ở chế độ nền.
    &- Đặt tiến trình chạy ở chế độ nền.  
7. Truy vấn quy trình nền - jobs
8. Hãy để quá trình tiếp tục chạy ở chế độ nền - bg .
9. Đưa quy trình nền lên nền trước - fg .
10. Điều chỉnh mức độ ưu tiên thời gian chạy chương trình/quy trình - nice / renice .
11. Quá trình tiếp tục hoạt động sau khi người dùng đăng xuất - nohup .
12. Cuộc gọi hệ thống quy trình theo dõi - strace .
13. Xem runlevel hiện tại - runlevel .
14. Giám sát thời gian thực việc sử dụng tài nguyên theo quy trình - top .
    -c- Hiển thị toàn bộ đường dẫn của quá trình.
    -d- Chỉ định thời gian (tính bằng giây) giữa các lần làm mới.
    -i- Không hiển thị các tiến trình nhàn rỗi hoặc zombie.
    -p- Hiển thị thông tin về quá trình được chỉ định.
### Chẩn đoán hệ thống
1. Chẩn đoán ngoại lệ khởi động hệ thống - dmesg .
2. Xem thông tin hoạt động hệ thống - sar .
    -A- Hiển thị trạng thái sức khỏe của tất cả các thiết bị (CPU, bộ nhớ, đĩa).
    -u- Hiển thị trạng thái tải của tất cả các CPU.
    -d- Hiển thị việc sử dụng tất cả các đĩa.
    -r- Hiển thị mức sử dụng bộ nhớ.
    -n- Hiển thị trạng thái hoạt động của mạng.
3. Xem mức sử dụng của bộ nhớ - free
4. Thống kê bộ nhớ ảo - vmstat .
5. Thống kê thông tin CPU - mpstat .
6. Kiểm tra mức sử dụng bộ nhớ của tiến trình - pmap .
7. Báo cáo thống kê CPU và I/O của thiết bị - iostat .
8. Hiển thị tất cả các thiết bị PCI - lspci .
9. Hiển thị trạng thái của cơ sở liên lạc giữa các tiến trình - ipcs .


# Tổng quan về cơ sở dữ liệu quan hệ và MySQL 
    Cơ sở lý thuyết: đại số quan hệ (các phép toán quan hệ, lý thuyết tập hợp, logic vị từ bậc nhất).
    Biểu diễn cụ thể: Sử dụng bảng hai chiều (có hàng và cột) để sắp xếp dữ liệu.
    Ngôn ngữ lập trình: Ngôn ngữ truy vấn có cấu trúc (SQL).
## Các lệnh cơ bản của MySQL
### Xem lệnh
1. Xem tất cả cơ sở dữ liệu
    show databases;
2. Xem tất cả các bộ ký tự
    show character set;
3. Xem tất cả các quy tắc sắp xếp
    show collation;
4. Xem tất cả động cơ
    show engines;
5. Xem tất cả các tệp nhật ký
    show binary logs;
6. Xem tất cả các bảng trong cơ sở dữ liệu
    show tables;
### Được giúp đỡ
    Trong công cụ dòng lệnh MySQL, bạn có thể sử dụng helplệnh hoặc ? để nhận trợ giúp, như hiển thị bên dưới.
1. Xem showtrợ giúp cho lệnh.
    ? show
2. Xem nội dung trợ giúp nào có sẵn.
    ? contents
3. Nhận trợ giúp cho một chức năng.
    ? functions
4. Nhận trợ giúp về các loại dữ liệu.
    ? data types
### Các lệnh khác
1. Tạo/xây dựng lại kết nối máy chủ - connect/ resetconnection.
2. Xóa đầu vào hiện tại - \c. Khi bạn mắc lỗi đầu vào, bạn có thể xóa \cđầu vào hiện tại và bắt đầu lại.
3. Sửa đổi dấu kết thúc (dấu phân cách) - delimiter. Dấu kết thúc mặc định là ;, bạn có thể dùng lệnh này để đổi sang ký tự khác, ví dụ muốn đổi thành $ký hiệu thì có thể dùng delimiter $lệnh.
4. Mở trình soạn thảo mặc định của hệ thống - edit. Sau khi chỉnh sửa xong, lưu và đóng, dòng lệnh sẽ tự động thực thi nội dung đã chỉnh sửa.
5. Xem trạng thái máy chủ - status.
6. Sửa đổi lời nhắc mặc định - prompt.
7. Thực thi lệnh hệ thống - system. Các lệnh hệ thống có thể systemđược thực thi sau lệnh và systemlệnh cũng có thể được viết tắt \!.
8. Thực thi tệp SQL - source. sourceLệnh được theo sau bởi đường dẫn tệp SQL.
9. Chuyển hướng đầu ra - tee/ notee. Đầu ra của lệnh có thể được chuyển hướng đến một tệp được chỉ định.
10. Chuyển đổi cơ sở dữ liệu - use.
11. Hiển thị thông báo cảnh báo - warnings.
12. Thoát khỏi dòng lệnh quit-hoặc exit.


# MySQL chuyên sâu
Có 1 số điều cần đáng chú ý trong MySQL
1. select_type: Loại truy vấn.
    SIMPLE: CHỌN đơn giản, không cần sử dụng thao tác UNION hoặc truy vấn con.
    PRIMARY: Nếu truy vấn chứa truy vấn phụ, CHỌN ngoài cùng được đánh dấu CHÍNH.
    UNION: Câu lệnh SELECT thứ hai hoặc tiếp theo trong thao tác UNION.
    SUBQUERY: CHỌN đầu tiên trong truy vấn phụ.
    DERIVED: Truy vấn con CHỌN của bảng dẫn xuất.
2. table: Truy vấn bảng tương ứng.
3. type: Cách MySQL tìm các hàng thỏa mãn điều kiện trong bảng hay còn gọi là kiểu truy cập, bao gồm: ALL(quét toàn bộ bảng), index(quét toàn bộ chỉ mục, chỉ duyệt qua cây chỉ mục), ( quét phạm vi chỉ mục), range(quét phạm vi chỉ mục), ref(không quét toàn bộ chỉ mục). quét chỉ mục duy nhất), eq_ref(quét chỉ mục duy nhất), const/ system(truy vấn mức không đổi), NULL(không cần truy cập bảng hoặc chỉ mục). Trong số tất cả các loại quyền truy cập, rõ ràng ALL có hiệu suất kém nhất. Việc quét toàn bộ bảng mà nó thể hiện có nghĩa là mọi hàng trong bảng phải được quét để tìm các hàng phù hợp.
4. possible_keys: MySQL có thể chọn chỉ mục, nhưng nó có thể không được sử dụng .
5. key: Chỉ mục thực sự được MySQL sử dụng. Nếu có thì NULLcó nghĩa là chỉ mục đó không được sử dụng.
6. key_len: Độ dài của chỉ mục được sử dụng, nếu nó không ảnh hưởng đến truy vấn thì độ dài càng ngắn thì càng tốt.
7. rows: Số hàng cần quét để thực hiện truy vấn. Đây là ước tính .
8. extra: Thông tin bổ sung về truy vấn.
    Using filesort: MySQL không thể sử dụng chỉ mục để hoàn thành thao tác sắp xếp.
    Using index: Chỉ sử dụng thông tin chỉ mục mà không cần tra cứu thêm bảng để có thêm thông tin.
    Using temporary: MySQL cần sử dụng các bảng tạm thời để lưu trữ các tập kết quả, thường được sử dụng để nhóm và sắp xếp.
    Impossible where: wheremệnh đề sẽ dẫn đến không có hàng nào phù hợp với điều kiện.
    Distinct: Sau khi MySQL tìm thấy hàng khớp đầu tiên, nó sẽ ngừng tìm kiếm thêm hàng cho tổ hợp hàng hiện tại.
    Using where: Cột được truy vấn không nằm trong chỉ mục và điều kiện lọc không phải là cột đầu tiên của chỉ mục.

## Nguyên tắc thiết kế chỉ mục
1. Các cột phù hợp nhất để lập chỉ mục là những cột xuất hiện trong mệnh đề WHERE và mệnh đề nối.
2. Số lượng bản số của cột chỉ mục càng lớn (nhiều giá trị và ít giá trị trùng lặp) thì hiệu ứng chỉ mục sẽ càng tốt.
3. Việc sử dụng các chỉ mục tiền tố có thể làm giảm không gian bị chỉ mục chiếm giữ và có thể lưu trữ nhiều chỉ mục hơn trong bộ nhớ.
4. Càng nhiều chỉ mục thì càng tốt.Mặc dù các chỉ mục giúp tăng tốc các thao tác đọc (truy vấn) nhưng các thao tác ghi (thêm, xóa, sửa) sẽ trở nên chậm hơn, vì những thay đổi về dữ liệu sẽ gây ra các cập nhật chỉ mục, giống như việc thêm và xóa các chương sách. làm thư mục cập nhật.
5. Khi sử dụng công cụ lưu trữ InnoDB, chỉ mục thông thường của bảng sẽ lưu giá trị của khóa chính, vì vậy khóa chính phải có kiểu dữ liệu ngắn hơn càng nhiều càng tốt . Điều này có thể giảm không gian chiếm dụng của chỉ mục một cách hiệu quả và cải thiện hiệu ứng bộ đệm của chỉ mục.

## Xem
Chế độ xem là một đối tượng trong cơ sở dữ liệu quan hệ kết hợp tập kết quả bao gồm một tập hợp các hướng dẫn truy vấn vào bảng dữ liệu có thể truy vấn. Nói một cách đơn giản, dạng xem là một bảng ảo, nhưng không giống như bảng dữ liệu, bảng dữ liệu là một cấu trúc thực thể, trong khi dạng xem là một cấu trúc ảo
Việc sử dụng chế độ xem mang lại những lợi ích sau:
1. Các bảng dữ liệu thực thể có thể được ẩn đi để các chương trình bên ngoài không thể biết cấu trúc dữ liệu thực tế, cho phép khách truy cập sử dụng các phần của bảng thay vì toàn bộ bảng, giảm nguy cơ bị tấn công cơ sở dữ liệu.
2. Trong hầu hết các trường hợp, chế độ xem là chỉ đọc (cập nhật chế độ xem thường có nhiều hạn chế) và các chương trình bên ngoài không thể sửa đổi trực tiếp dữ liệu thông qua chế độ xem.
3. Sử dụng lại các câu lệnh SQL để bao bọc các truy vấn có độ phức tạp cao trong các bảng dạng xem và truy cập trực tiếp vào dạng xem để truy xuất dữ liệu cần thiết; bạn cũng có thể coi dạng xem như một bảng dữ liệu cho các truy vấn kết nối.
4. Chế độ xem có thể trả về dữ liệu ở định dạng khác với bảng dữ liệu thực thể và dữ liệu có thể được định dạng khi tạo chế độ xem.

các quy tắc và hạn chế.
1. Các khung nhìn có thể được lồng vào nhau và một khung nhìn mới có thể được xây dựng bằng cách sử dụng dữ liệu được truy xuất từ ​​các khung nhìn khác. Chế độ xem cũng có thể được sử dụng với bảng.
2. Mệnh đề có thể được sử dụng khi tạo một chế độ xem order by, nhưng nếu nó cũng được sử dụng khi truy xuất dữ liệu từ chế độ xem order bythì mệnh đề gốc trong chế độ xem order bysẽ bị ghi đè.
3. Chế độ xem không thể sử dụng chỉ mục và sẽ không kích hoạt việc thực thi trình kích hoạt (trong quá trình phát triển thực tế, do hiệu suất và các cân nhắc khác, thường không nên sử dụng trình kích hoạt, vì vậy chúng tôi sẽ không giới thiệu khái niệm này).

## Nội dung khác
### Lý thuyết mẫu
Lý thuyết mô hình là hệ tư tưởng hướng dẫn để thiết kế các bảng hai chiều trong cơ sở dữ liệu quan hệ.
1. Dạng bình thường thứ nhất: Phạm vi giá trị của mỗi cột của bảng dữ liệu được cấu thành từ các giá trị nguyên tử và không thể chia thêm được.
2. Dạng chuẩn thứ hai: Mọi dữ liệu trong bảng dữ liệu phải phụ thuộc hoàn toàn vào các khóa (khóa chính và khóa ứng viên) của bảng dữ liệu.
3. Dạng chuẩn thứ ba: Tất cả các thuộc tính không khóa chỉ liên quan đến khóa ứng viên, nghĩa là các thuộc tính không khóa phải độc lập và không liên quan với nhau.
### Toàn vẹn dữ liệu
1. Tính toàn vẹn của thực thể - mỗi thực thể là duy nhất
    Khóa chính ( primary key) / ràng buộc duy nhất ( unique)
2. Tính toàn vẹn tham chiếu (Tính toàn vẹn tham chiếu) - Không được phép tham chiếu đến các thực thể không tồn tại trong mối quan hệ
    khóa ngoại ( foreign key)
3. Tính toàn vẹn của tên miền - dữ liệu hợp lệ
    Kiểu dữ liệu và độ dài
    ràng buộc không null ( not null)
    Ràng buộc giá trị mặc định ( default)
    Kiểm tra các ràng buộc ( check)
### tính nhất quán của dữ liệu
1. Giao dịch: Một loạt các thao tác đọc/ghi vào cơ sở dữ liệu đều thành công hoặc tất cả đều thất bại.
2. Thuộc tính ACID của giao dịch
    Tính nguyên tử: Toàn bộ giao dịch được thực hiện và tất cả hoặc không có thao tác nào trên cơ sở dữ liệu chứa trong đó được thực thi.
    Tính nhất quán: Các giao dịch phải đảm bảo rằng trạng thái của cơ sở dữ liệu thay đổi từ trạng thái nhất quán này sang trạng thái nhất quán khác
    Cô lập: Khi nhiều giao dịch được thực hiện đồng thời, việc thực hiện một giao dịch sẽ không ảnh hưởng đến việc thực hiện các giao dịch khác
    Độ bền: Các sửa đổi đối với cơ sở dữ liệu bằng các giao dịch đã cam kết phải được lưu trữ vĩnh viễn trong cơ sở dữ liệu
3. Hoạt động giao dịch trong MySQL
    Môi trường giao dịch mở
        start transaction
    cam kết giao dịch
        commit
    Giao dịch khôi phục
        rollback
4. Xem mức độ cô lập giao dịch
    show variables like 'transaction_isolation';
5. Sửa đổi mức độ cô lập giao dịch (phiên hiện tại)
    set session transaction isolation level read committed;


# Chương trình Python truy cập cơ sở dữ liệu
Ta có thể sử dụng mysqlclienthoặc pymysqlthư viện của bên thứ ba để truy cập cơ sở dữ liệu MySQL và triển khai các hoạt động lưu giữ dữ liệu. Cách sử dụng của cả hai đều giống hệt nhau, ngoại trừ tên mô-đun được nhập vào là khác nhau.
Các bước sử dụng pymysqlMySQL như sau:
1. Tạo kết nối. Sau khi máy chủ MySQL được khởi động, nó sẽ cung cấp các dịch vụ mạng dựa trên TCP (Giao thức điều khiển truyền dẫn). Chúng ta có thể kết nối với máy chủ MySQL thông qua các chức năng pymysqlcủa mô-đun connect. Khi gọi connecthàm, bạn cần chỉ định máy chủ ( host), cổng ( port), tên người dùng ( user), mật khẩu ( password), cơ sở dữ liệu ( database), bộ ký tự ( charset) và các tham số khác, hàm sẽ trả về một Connectionđối tượng.
2. Lấy con trỏ. Sau khi kết nối thành công với máy chủ MySQL, việc tiếp theo cần làm là gửi câu lệnh SQL đến máy chủ cơ sở dữ liệu, MySQL sẽ thực thi câu lệnh SQL nhận được và trả về kết quả thực thi qua mạng. cursorĐể thực hiện thao tác này, trước tiên bạn cần lấy đối tượng con trỏ ( ) thông qua phương thức đối tượng kết nối Cursor.
3. Vấn đề SQL. Thông qua các phương thức của đối tượng con trỏ execute, chúng ta có thể đưa ra các câu lệnh SQL tới cơ sở dữ liệu.
4. Nếu bạn thực hiện inserthoặc vận hành, bạn cần phải cam kết hoặc khôi deletephục updategiao dịch theo tình hình thực tế. Bởi vì khi tạo kết nối, môi trường giao dịch được bật theo mặc định, sau khi thao tác hoàn tất, bạn cần sử dụng đối tượng commithoặc rollbackphương thức của đối tượng kết nối để cam kết hoặc khôi phục giao dịch. rollbackPhương thức này thường được đặt excepttrong khối mã bắt ngoại lệ. Nếu selectthao tác được thực hiện, kết quả truy vấn cần được ghi lại thông qua đối tượng con trỏ, có ba phương thức tương ứng là: fetchone, fetchmanyvà fetchall. Phương thức này fetchonesẽ tìm nạp một bản ghi và trả về dưới dạng một bộ dữ liệu hoặc từ điển; phương thức fetchmanyand fetchallsẽ tìm nạp nhiều bản ghi và trả về dưới dạng một bộ dữ liệu lồng nhau hoặc một danh sách từ điển.
5. Đóng kết nối. Sau khi hoàn thành thao tác kiên trì, vui lòng đừng quên đóng kết nối và giải phóng các tài nguyên bên ngoài. Chúng ta thường finallysử dụng phương thức đối tượng kết nối closetrong khối mã để đóng kết nối.


# Hive
Hive là một công cụ kho dữ liệu dựa trên Hadoop có nguồn mở bởi Facebook. Đây hiện là giải pháp xử lý dữ liệu lớn được sử dụng rộng rãi nhất. Nó có thể chuyển đổi các truy vấn SQL thành MapReduce (một kiến ​​trúc phần mềm do Google đề xuất để xử lý song song các tập dữ liệu quy mô lớn) . Computation), cung cấp hỗ trợ hoàn hảo cho SQL và có thể thực hiện thống kê dữ liệu lớn rất thuận tiện.
1. Ánh xạ dữ liệu có cấu trúc trong HDFS vào các bảng.
2. Bằng cách phân tích cú pháp và chuyển đổi Hive-SQL, một loạt tác vụ MapReduce/Spark dựa trên Hadoop cuối cùng đã được tạo và quá trình xử lý dữ liệu được hoàn thành bằng cách thực thi các tác vụ này.
## Chuẩn bị
1. Xây dựng một nền tảng dữ liệu lớn
2. Truy cập nền tảng dữ liệu lớn thông qua nút Máy khách.
3. Tạo tệp trong hệ thống tệp Hadoop.
    hadoop fs -mkdir /data  
    hadoop fs -chmod g+w /data
4. Sao chép các tệp dữ liệu đã chuẩn bị vào hệ thống tệp Hadoop.
    hadoop fs -put /home/ubuntu/data/* /data

## Tạo/xóa cơ sở dữ liệu
tạo nên.
    create database if not exists demo;
hoặc
    hive -e "create database demo;"
xóa bỏ.
    drop database if exists demo;
công tắc.
    use demo;

## Các hàm thường dùng
1. from_unixtime:Chuyển đổi dấu thời gian thành ngày
2. unix_timestamp:Chuyển đổi ngày thành dấu thời gian
3. datediff: Tính chênh lệch thời gian giữa hai ngày
4. if: Trả về các giá trị khác nhau dựa trên điều kiện
5. substr: Chuỗi con
6. get_json_objectkey: Trích xuất chuỗi tương ứng được chỉ định từ chuỗi JSON value, chẳng hạn như: get_json_object(info, '$.first_name').

### Thêm
Tìm hiểu thêm về NoSQL Databases 