# DỰ ĐOÁN BỆNH TIM SỬ DỤNG MÁY HỌC
Trường Đại Học Sài Gòn, Thành Phố Hồ Chí Minh, Việt Nam


**[2025-01] Phương Pháp Nghiên Cứu Khoa Học**


giảng viên hướng đãn: **Đỗ Như Tài**


Sinh viên: **Hoàng Vũ, Huỳnh Thanh Bình, Nguyễn Minh Tú, Phạm Tấn Khương**


**Mục tiêu:  Tối ưu mô hình dự đoán bệnh tim bằng máy học**

## 1. Giới thiệu
Bệnh tim là một trong những nguyên nhân hàng đầu gây tử vong trên toàn thế giới. Việc chẩn đoán sớm và chính xác bệnh tim có ý nghĩa quan trọng trong việc điều trị và giảm nguy cơ biến chứng. Với sự phát triển của trí tuệ nhân tạo (AI) và học máy (ML), nhiều phương pháp hiện đại đã được áp dụng để hỗ trợ dự đoán bệnh tim một cách chính xác và hiệu quả hơn so với các phương pháp truyền thống.

## 2. Các phương pháp học máy trong dự đoán bệnh tim
Nhiều nghiên cứu đã sử dụng các thuật toán học máy để phân tích dữ liệu y tế và dự đoán nguy cơ mắc bệnh tim. Một số thuật toán phổ biến bao gồm:

K-Nearest Neighbors (KNN): Phân loại bệnh dựa trên dữ liệu của các bệnh nhân có đặc điểm tương tự.
Hồi quy Logistic (Logistic Regression): Phân tích mối quan hệ giữa các yếu tố nguy cơ và khả năng mắc bệnh tim.
Random Forest Classifier: Kết hợp nhiều cây quyết định để cải thiện độ chính xác dự đoán.

## 3. Mô hình ban đầu

### 🎯 Hiệu năng mô hình

* Mô hình được huấn luyện bằng phương pháp **chia dữ liệu thành tập huấn luyện và tập kiểm tra (Train-Test Split)**.
* **Độ chính xác trên tập kiểm tra** đạt **85.25%**, cho thấy mô hình có khả năng phân loại khá tốt.
* Các chỉ số đánh giá chi tiết:

```
               precision    recall  f1-score   support

           0       0.83      0.86      0.85        29
           1       0.87      0.84      0.86        32

    accuracy                           0.85        61
   macro avg       0.85      0.85      0.85        61
weighted avg       0.85      0.85      0.85        61
```

* Các chỉ số Precision, Recall, F1-score đều nằm trong khoảng **0.83–0.87**, thể hiện mô hình **cân bằng giữa hai lớp** và **không bị thiên lệch**.

### 📊 Độ quan trọng của các đặc trưng

Dựa trên kết quả phân tích tầm quan trọng, ta nhận thấy:

* **Các đặc trưng số (numeric)** đóng vai trò quan trọng nhất:

  * `num__ca` (số mạch máu chính): **12.2%**
  * `num__thalach` (nhịp tim tối đa): **11.9%**
  * `num__age`, `num__chol`, `num__trestbps`: từ **8–10%**

* **Một số đặc trưng phân loại (categorical)** như:

  * `cat__thal_2`, `cat__thal_3`, `cat__cp_0` cũng có độ quan trọng tương đối (\~5–8%)

* **Các đặc trưng ít quan trọng** (dưới 1%), như `cat__thal_0`, `cat__restecg_2`, `cat__fbs_1`, gần như **không đóng góp vào mô hình** và có thể **loại bỏ** để tinh gọn mô hình.

### ✅ Kết luận

Mô hình đã đạt được kết quả **tốt và ổn định** với độ chính xác cao và các chỉ số đánh giá cân bằng. Các đặc trưng quan trọng nhất chủ yếu đến từ **các yếu tố sức khỏe dạng số** như nhịp tim, mạch máu, huyết áp và cholesterol, phù hợp với bài toán dự đoán trong lĩnh vực y tế.

Dưới đây là phiên bản **mới** của phần `README.md` theo phong cách bạn cung cấp, cập nhật theo kết quả mới của bạn (accuracy: 90.16%, các chỉ số đã nêu):

## 4. Kết quả đạt được (Tối ưu mô hình trên)
### 🎯 Hiệu năng mô hình

* Mô hình được huấn luyện bằng phương pháp **chia dữ liệu thành tập huấn luyện và tập kiểm tra (Train-Test Split)**.
* **Độ chính xác trên tập kiểm tra** đạt **90.16%**, cho thấy mô hình có hiệu năng **rất tốt** trong việc phân loại dữ liệu.
* Các chỉ số đánh giá chi tiết:

```
               precision    recall  f1-score   support

           0       0.87      0.93      0.90        29
           1       0.93      0.88      0.90        32

    accuracy                           0.90        61
   macro avg       0.90      0.90      0.90        61
weighted avg       0.90      0.90      0.90        61
```

* Các chỉ số Precision, Recall, F1-score đều đạt **trên 0.88**, thể hiện mô hình có khả năng **cân bằng tốt giữa hai lớp** và **phân loại hiệu quả** cho cả trường hợp có và không có bệnh tim.

### 📊 Độ quan trọng của các đặc trưng

Dựa trên phân tích tầm quan trọng từ mô hình Random Forest:

* **Các đặc trưng số (numeric)** chiếm vai trò then chốt:

  * `num__ca` (số mạch máu chính): **\~12%**
  * `num__thalach` (nhịp tim tối đa): **\~11.9%**
  * Các đặc trưng khác như `num__age`, `num__chol`, `num__trestbps`: dao động từ **8–10%**

* **Một số đặc trưng phân loại (categorical)** cũng có mức đóng góp đáng kể:

  * `cat__thal_2`, `cat__thal_3`, `cat__cp_0`: trong khoảng **5–8%**

* **Những đặc trưng có tầm quan trọng thấp** (dưới 1%) như `cat__thal_0`, `cat__restecg_2`, `cat__fbs_1` có thể được cân nhắc **loại bỏ để giảm độ phức tạp của mô hình**.

### ✅ Kết luận

Mô hình đạt được **hiệu năng rất cao và ổn định**, với độ chính xác vượt 90% và các chỉ số đánh giá đồng đều. Các đặc trưng đầu vào quan trọng phần lớn thuộc về **yếu tố sức khỏe định lượng**, hỗ trợ tốt cho việc dự đoán bệnh tim một cách chính xác và có cơ sở.

Github tham khảo : https://github.com/g-shreekant/Heart-Disease-Prediction-using-Machine-Learning/tree/master
