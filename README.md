Tải AnacondaPrompt
https://www.anaconda.com/download
Windows: tải bản .exe
MacOS/Linux: tải bản .pkg hoặc .sh

// Tạo môi trường ảo trong conda
nhớ cd về thư mục project của mình
conda create -n myenv python=3.12 -y
 phiên bản python khác thì thay chỗ 3.12 thành phiên bản của mình
// kích hoạt môi trường
conda activate myenv

nhớ cd về thư mục project của mình
// Cập nhật các thư viện
python -m pip install --upgrade pip setuptools wheel


// Cài các thư viện chính
pip install numpy pandas opencv-python dlib face-recognition tensorflow torch torchvision pymongo flask pygame

// nếu cài dlib bị lỗi thì dùng cách thủ công
 https://github.com/z-mahmud22/Dlib_Windows_Python3.x

 chọn phiên bản phù hợp với phiên bản python của mình
 pip install dlib‑19.24.2‑cp312‑cp312‑win_amd64.whl


// tạo tài khoản mongoAtlas 
Nhấn vào Sign Up để tạo tài khoản.

Nhập email, mật khẩu, và chọn Free Shared Cluster (miễn phí).

Xác nhận email để hoàn tất đăng ký.
Tạo Cluster miễn phí
Sau khi đăng nhập, chọn Create a New Cluster.

Chọn Shared Cluster (Miễn phí).

Chọn khu vực máy chủ (AWS, Azure, hoặc Google Cloud).

Khuyến nghị chọn khu vực gần bạn để có tốc độ nhanh nhất.

Đặt tên Cluster (ví dụ: MyCluster).

Nhấn Create Cluster và đợi khoảng 5 phút để hệ thống thiết lập.
Kết Nối MongoDB Atlas với Ứng Dụng
3.1. Tạo User và Lấy URL Kết Nối
Vào Database Access, chọn + Add New Database User.

Đặt username/password để kết nối.

Chọn Allow Access From Anywhere để có thể kết nối từ mọi nơi.

Sao chép Connection String để sử dụng sau này.
mongodb+srv://username:password@mycluster.mongodb.net/mydatabase?retryWrites=true&w=majority

ví dụ: (trong config/database)
class Database:
    def __init__(self):
        username = quote_plus("thy230200")  # đổi thành cái username của mình
        username
        password = quote_plus("Thy@2304")  # đổi cái password vừa tạo
        password
        uri = f"mongodb+srv://{username}:{password}@cluster0.5wunr.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0"

// chạy chương trình
python main.py
