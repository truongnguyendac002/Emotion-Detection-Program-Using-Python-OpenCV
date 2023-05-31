# Emotion-Detection-Program-Using-Python-OpenCV
Nhập môn trí tuệ nhân tạo PTIT

Dữ liệu được lấy từ FER-2013 cung cấp bởi Manas Sambare:
https://www.kaggle.com/datasets/msambare/fer2013

Ứng dụng sử dụng các thư viện: Keras, OpenCV, Numpy, Matplotlib.

## 1. Preprocessing
Do kích thước và độ phức tạp của tập dữ liệu, không thể tải tất cả các hình ảnh vào bộ nhớ cùng một lúc. Do đó, chúng ta sẽ sử dụng các công cụ tạo dữ liệu để tạo ra các lô hình ảnh trong quá trình huấn luyện, giúp cho việc huấn luyện mô hình trên toàn bộ tập dữ liệu được hiệu quả hơn. 
Ngoài ra, chúng ta sẽ áp dụng các kỹ thuật tăng cường dữ liệu khác nhau cho các hình ảnh huấn luyện, như xoay, dịch chuyển và lật ngược. Điều này sẽ giúp tăng kích thước và đa dạng hóa tập huấn luyện, từ đó cải thiện hiệu suất của mô hình học sâu. 
![image](https://github.com/truongnguyendac002/Emotion-Detection-Program-Using-Python-OpenCV/assets/88220511/8d896a20-a827-4d95-8db7-0e98ca2c3d62)

## 2.Modeling
### CNN Model
Phát triển kiến trúc CNN bằng cách định nghĩa lớp đầu vào và số bộ lọc trong Convolutional Layer đầu tiên. Sau đó, chúng ta sẽ thêm các Convolutional Layer khác với số lượng bộ lọc tăng dần, tiếp theo là các Pooling Layer để giảm kích thước không gian của các bản đồ đặc trưng. Sau đó, chúng ta sẽ thêm các Fully Connected Layer để phân loại cảm xúc.
- Xây dụng CNN model từ lớp Sequental:
![image](https://github.com/truongnguyendac002/Emotion-Detection-Program-Using-Python-OpenCV/assets/88220511/c3b4b542-357f-4998-985b-23d4a3c4a146)
- Huấn luyện:
![image](https://github.com/truongnguyendac002/Emotion-Detection-Program-Using-Python-OpenCV/assets/88220511/da16fe0f-ad9e-4263-8894-7bc5bad4c9f4)

## 3. Evaluation
-	Đồ thị biểu diễn sự thay đổi của giá trị hàm mất mát (loss) trên tập dữ liệu huấn luyện (training set) và tập dữ liệu đánh giá (validation set) theo từng epoch trong quá trình huấn luyện mô hình:
![image](https://github.com/truongnguyendac002/Emotion-Detection-Program-Using-Python-OpenCV/assets/88220511/e2bfc4d7-a6a5-4f7b-86e8-082e53f4a21f)

-	Đồ thị biểu diễn độ chính xác (accuracy) của mô hình trên tập huấn luyện (training accuracy) và tập xác thực (validation accuracy) qua các epoch trong quá trình huấn luyện:
![image](https://github.com/truongnguyendac002/Emotion-Detection-Program-Using-Python-OpenCV/assets/88220511/a8bff134-100f-4958-b2a3-ae7558cf42e5)

## 4. Webcam
![image](https://github.com/truongnguyendac002/Emotion-Detection-Program-Using-Python-OpenCV/assets/88220511/ac127ed5-7f1c-4486-98a0-51db1d7da032)
