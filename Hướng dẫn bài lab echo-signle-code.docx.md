***Nội dung và hướng dẫn thực hiện bài lab***

**Giấu tin trong âm thanh sử dụng thuật toán echo hiding single kernel**

**1\. Chuẩn bị môi trường**

* Máy ảo Ubuntu có cài đặt labtainer  
* File imodule của labtainer echo-single-code

**2\. Các bước thực hiện**

**2.1. Chuẩn bị bài lab**

* Tải bài lab:

*imodule [https://github.com/tai1503/echo-single-code/raw/refs/heads/main/imodule.tar](https://github.com/tai1503/echo-single-code/raw/refs/heads/main/imodule.tar)*

* Khởi động bài lab:  
  *labtainer \-r echo-single-code*

**2.2 Thực hiện bài lab**

Cài đặt các thư viện cần thiết cho bài lab:

*pip3 install numpy*

*pip3 install scipy*

*pip3 install matplotlib*

*pip3 install scikit-learn*

*sudo apt update*

*sudo apt install python3-tk*

Bài lab gồm các file:

* text\_to\_bits.py: chuyển đổi thông điệp sang dạng bit.  
* echo\_encode.py: giấu thông điệp vào trong file âm thanh .wav  
* echo\_extract.py: giải mã thông điệp từ file âm thanh .wav  
* compare.py: so sánh hai file âm thanh trước và sau khi giấu tin

Xem nội dung file thông điệp:

*cat text.txt*

Chuyển đổi thông điệp sang dạng bit và lưu vào file *bits\_mes.txt*:

*python3 text\_to\_bits.py \>\> bits\_mes.txt*

Xem nôi dung file *bits\_mes.txt:*

*cat bits\_mes.txt*

Thực hiên giấu tin vào file âm thanh:

*python3 echo\_encode.py input.wav bits\_mes.txt*

Thực hiện tách tin từ file âm thanh *output.wav*:

*python3 echo\_extract.py*

So sánh giữa hai file âm thanh sau khi giấu tin và trước khi giấu tin:

*python3 compare.py input.wav output.wav*

* MSE (Mean Squared Error): Là sai số bình phương trung bình giữa tín hiệu gốc và tín hiệu đã biến đổi. MSE càng nhỏ ⇒ tín hiệu càng giống gốc**.**

* SNR (Signal-to-Noise Ratio): Là tỉ lệ giữa năng lượng tín hiệu và nhiễu, đo bằng dB. SNR càng lớn ⇒ tín hiệu càng ít nhiễu, chất lượng càng cao.

Trên terminal đầu tiên:

* Kiểm tra kết quả bài lab:

*checkwork*

* Kết thúc bài lab:

*stoplab*

* Khởi động lại bài lab:

*labtainer \-r echo-single-code*