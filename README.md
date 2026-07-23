# Hướng dẫn sử dụng Hugo (PC Wiwndows - Github - VP)
# Cài đặt trên máy tính Wiwndows
## Visual Studio Code
## Cài đặt và cấu hình Hugo
Link https://github.com/gohugoio/hugo/releases
Để cài đặt Hugo trên Windows và cấu hình biến môi trường (Environment Variables) giúp VS Code nhận diện được lệnh hugo, bạn thực hiện theo các bước chuẩn dưới đây:Bước 1: Tải Hugo về máy tínhTruy cập vào trang chứa các bản cài đặt của Hugo trên GitHub tại đây.Cuộn xuống phần Assets của phiên bản mới nhất, tìm bản dành cho Windows.Bạn cực kỳ nên chọn bản Extended để sau này cài theme không bị lỗi xử lý giao diện (SASS/SCSS).Tên file có dạng: hugo_extended_X.X.X_windows-amd64.zip (Tải file đuôi .zip, không tải các file .deb hay .tar.gz).Bước 2: Giải nén và sắp xếp thư mụcVào ổ C:\ trên máy tính của bạn, tạo một thư mục mới tên là hugo (Đường dẫn sẽ là C:\hugo).Mở file .zip vừa tải về, giải nén toàn bộ các file bên trong (bao gồm file hugo.exe) vào thẳng thư mục C:\hugo vừa tạo.Bước 3: Cấu hình biến môi trường (Path) cho WindowsBước này giúp Windows hiểu được lệnh hugo khi bạn gõ trong Terminal của VS Code.Bấm phím Windows trên bàn phím (hoặc ô tìm kiếm), gõ chữ env và chọn Edit the system environment variables.Một cửa sổ nhỏ hiện ra, bấm vào nút Environment Variables... ở góc dưới cùng bên phải.Ở khung User variables for [Tên_Máy_Tính] phía trên, tìm dòng có tên là Path, bấm chuột vào đó rồi chọn Edit...Cửa sổ mới hiện ra, bấm nút New ở bên phải, rồi gõ (hoặc dán) đường dẫn thư mục của bạn vào: C:\hugoBấm OK ➔ OK ➔ OK để đóng toàn bộ các cửa sổ lại và lưu cấu hình.Bước 4: Kiểm tra thành quả trong VS CodeKhởi động lại phần mềm VS Code (Bắt buộc phải tắt đi bật lại để VS Code cập nhật biến môi trường mới).Mở thư mục dự án của bạn, bật Terminal (`Ctrl + ``) và gõ lệnh:bashhugo version
Hãy thận trọng khi sử dụng mã.Nếu màn hình hiển thị thông tin phiên bản dạng hugo v0.X.X+extended windows/amd64 nghĩa là bạn đã cài đặt thành công 100%.
## Cài phần mềm Git
Link https://git-scm.com/download/win
Truy cập vào trang chủ của Git: git-scm.comBấm vào dòng Click here to download để tải về bản cài đặt tự động (thường là bản 64-bit Git for Windows Setup).Sau khi tải xong, mở file .exe vừa tải về lên.Cứ bấm Next liên tục từ đầu đến cuối (giữ nguyên các tùy chọn mặc định của nhà sản xuất) cho đến khi bấm Install và hoàn thành.Bước 2: Cập nhật lại phần mềm VS Code (Quan trọng)Sau khi cài đặt Git xong, Windows đã nhận lệnh nhưng cửa sổ VS Code hiện tại của bạn thì chưa.Hãy tắt hoàn toàn phần mềm VS Code đi (Bấm dấu X ở góc màn hình).Mở lại VS Code và mở lại thư mục dự án Hugo của bạn.Bật lại Terminal (`Ctrl + ``) và gõ lệnh kiểm tra:bashgit --version
Hãy thận trọng khi sử dụng mã.Nếu màn hình hiển thị thông tin dạng git version 2.X.X.windows.1 nghĩa là hệ thống đã nhận diện thành công 100%.
# Kết nối với Kết nối Git từ máy tính Windows lên GitHub
# 1. Khởi tạo Git cho thư mục Hugo của bạn (nếu trước đó chưa làm)
git init
# 2. Tạo một file tên là .gitignore để không đẩy các file thừa lên GitHub
# Bạn có thể tạo file này thủ công trong VS Code và dán nội dung sau vào:
echo "public/" >> .gitignore
echo "resources/_gen/" >> .gitignore
echo ".hugo_build.lock" >> .gitignore

# 3. Gom tất cả các file lại để chuẩn bị tải lên
git add .

# 4. Tạo một ghi chú cho lần tải lên này
git commit -m "First commit from Windows"
