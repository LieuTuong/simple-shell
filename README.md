# simple-shell
Đồ án 1 hệ điều hành


TRƯỜNG ĐẠI HỌC KHOA HỌC TỰ NHIÊN TP.HCM
KHOA CÔNG NGHỆ THÔNG TIN 

BÁO CÁO ĐỒ ÁN 1 – SIMPLE SHELL
MÔN HỆ ĐIỀU HÀNH

    • Thành viên nhóm:
Đỗ Hữu Trung 	 	1712843
Thái Thanh Tùng 	1712885
Liêu Cập Cát Tường	1712886


    I. Mô tả đồ án:
    • Mức độ hoàn thành: 100%
    • Thiết kế đồ án:
while(1)
{
    1. Nhận lệnh từ người dùng nhập vào inputLine.
    2. Kiểm tra xem inputLine có nằm trong những trường hợp:
    • Nếu là null thì continue vòng lặp.
    • Nếu là “exit” thì thoát khỏi vòng lặp.
    • Nếu là !! thì inputLine = history.
    3. Kiểm tra TYPE của inputLine như pipe (|), redirect (<,>) hay câu lệnh bình thường.
    4. Tách token inputLine.
    5. Thực hiện lệnh tùy theo TYPE, kiem tra &, forking ra tiến trình con và gọi lệnh execvp().
}

    • Các test case:
        1. ls
        2. ls -l
        3. aaa
        4. exit
        5. !!
        6. cat Hello1.txt
        7. cat Hello1.txt Hello2.txt
        8. echo “ He dieu hanh”
        9. grep mySHELL out.txt
        10. clear  
        11.  ls -l > out.txt
        12.  cat Hello1.txt Hello2.txt > out.txt
        13.  sort < number.txt
        14.  cat out.txt | head -4
        15.  cat out.txt | tail -4
        16.  ls -la | grep .txt

    II. Hướng dẫn sử dụng các tính năng:
    a) Thực hiện được các câu lệnh đơn giản (không là câu lệnh chuyển hướng Input, Output hay câu lệnh giao tiếp qua Pipe):
    • Câu lệnh “ls” liệt kê thư mục hiện hành và câu lệnh “ls -l” hiện thị đầy đủ các thông tin (quyền truy cập, chủ, kích thước…).

    • Câu lệnh “exit” dùng để thoát chương trình. Ngoài ra chương trình còn xử lí được các trường hợp nhập lệnh sai.

    • Câu lệnh “cat” để xem nội dung 1 tập tin ngắn và lệnh “echo” hiện thị nội dung văn bản.

    • Câu lệnh “grep” để tìm kiếm chuỗi trong file.

    b) Tính năng History:
    • Người dùng có thể thực hiện lệnh gần đây nhất bằng cách nhập lệnh “!!”
    • Nếu như trong History chưa có câu lệnh gần đây nhất được lưu thì chương trình sẽ xuất thông báo “No commands in history”. 
    • Trường hợp người dùng bỏ trống không nhập lệnh mà chỉ nhấn enter thì khi gõ “!!”, chương trình sẽ lấy câu lệnh gần đây nhất mà không bị bỏ trống.

    c) Tính năng chuyển hướng Input và Output:
Chuyển hướng Input


					Chuyển hướng Output

					Chuyển hướng Output

    d) Tính năng giao tiếp qua Pipe:



    III. Nguồn tài liệu tham khảo:
    • https://www.geeksforgeeks.org/making-linux-shell-c/ 
    • https://brennan.io/2015/01/16/write-a-shell-in-c/ 
    • https://github.com/pranav93y/myshell 
    • Linux Programmer's Manual  
