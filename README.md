# VSLdetect
## Phần mềm nhận diện thủ ngữ dựa trên mô hình RCNN của YoloV5
### Sử dụng dữ liệu cho huấn luyện và thử nghiệm trên Google Drive.
Trong sự án này bao gồm 2 file:
- train_yolo.ipynb.
- video_pic.ipynb.

Hiện không bao gốm sản phẩm cuối cùng trong repository (kho lưu trữ) này, để sử dụng phần mềm đã làm sẵn, tham khảo tại đây [Google Drive link](https://drive.google.com/drive/folders/117XhAG-hOCiw4yJNYHfpT1HviilNPznY?usp=sharing).

Lý do chọn Google Colab:
- cung cấp nền tảng cho việc huấn luyện machine learning trên cloud.
- cung cấp GPU, TPU cho việc huấn luyện.
- không yêu cầu phần cứng mãnh mẽ và miễn phí sử dụng.

Để huấn luyện, vui lòng tải 2 file này lên google drive và lưu trữ trong cùng 1 thư mục vì trong quá trình sẽ tải thêm 1 số file về Drive:
- train_yolo.ipynb: dùng để huấn luyện, mở file thông qua [Google Colab](https://colab.research.google.com/) tất cả hướng dẫn từng bước đã được đề cập bên trong.
- video_pic.ipynb: dùng để huấn luyện, bao gồm ***video mode*** - nhận diện thông qua video và ***picture mode*** - nhận diện thông qua hình ảnh. ***Lưu ý***: nhận diện hình ảnh phù thuộc vào camera của thiết bị nên có thể kết quả xuất ra có thể có tỉ suất khung hình trên giây (FPS) tương đối thấp.

Hiện tại chưa hỗ trợ nhận diện thời gian thực trên Google Drive.
### Sử dụng dữ liệu trên máy tính.
Vì đây là bản thử nghiệm, không phải bản thương mại nên cần phải sử dụng IDE của [Python 3](https://www.python.org/downloads/) để khởi chạy.
- Đối với hệ điều hành ***Window***: khuyến nghị sử dụng [Python 3.7](https://www.python.org/downloads/windows/) hoặc thấp hơn.
- Đối với hệ điều hành ***Linux***: khuyến nghị sử dụng Python 3.8 hoặc thấp hơn.
> sudo apt install python3.8

> sudo apt install python3-pip

Mở thư mục đã tải về và chạy lệnh trên CMD (đối với window) và Terminal (đối với linux) ngay tại thư mục này:
> pip3 install -r yolov5/requirements.txt

Lệnh này nhằm cài 1 số thư viện cơ bản để khởi chạy. Để chạy nhận diện thời gian thực:

> python3 yolov5/detect.py --weight best.pt --conf 0.3 --img-size 416 --source 0

Ở phần --source, người dùng có thể thay đổi thành đường dẫn file ảnh hay video, tham khảo tại file video_pic.ipynb
## Tài liệu tham khảo
- [Yolo V5](https://github.com/ultralytics/yolov5)
- [Pytorch](https://pytorch.org/)
- [Google Colab](https://colab.research.google.com/)
