# DỰ ĐOÁN BỆNH TIM SỬ DỤNG MÁY HỌC
Trường Đại Học Sài Gòn, Thành Phố Hồ Chí Minh, Việt Nam


**[2025-01] Phương Pháp Nghiên Cứu Khoa Học**


giảng viên hướng đãn: **Đỗ Như Tài**


Sinh viên: **Hoàng Vũ, Huỳnh Thanh Bình, Nguyễn Minh Tú, Phạm Tấn Khương**


**Mục tiêu:  Tạo mô hình máy học dự đoán bệnh tim với độ chính xác cao nhất và thời gian xử lý không quá chậm**

## 1 Tóm Tắt Nghiên Cứu
**Bệnh tim mạch** là một trong những nguyên nhân gây tử vong hàng đầu trên toàn thế giới. Việc chẩn đoán sớm và chính xác đóng vai trò quan trọng trong việc điều trị và ngăn ngừa biến chứng. Tuy nhiên, các phương pháp chẩn đoán truyền thống thường đòi hỏi thời gian, chi phí và chuyên môn cao. Trước thực trạng đó, nghiên cứu này được thực hiện nhằm xây dựng một mô hình dự đoán bệnh tim dựa trên các kỹ thuật học máy, giúp hỗ trợ bác sĩ và người bệnh trong quá trình ra quyết định.


Mục tiêu chính của nghiên cứu là ứng dụng **kỹ thuật Ensemble Learning** – cụ thể là **phương pháp Voting Ensemble** kết hợp giữa mô hình SVM và Logistic Regression – để nâng cao độ chính xác dự đoán so với việc sử dụng từng mô hình đơn lẻ. Dữ liệu huấn luyện được tiền xử lý bằng các kỹ thuật chuẩn hóa và mã hóa phù hợp, sau đó huấn luyện hai mô hình riêng biệt và kết hợp dự đoán đầu ra bằng cách trung bình hóa kết quả.


Kết quả thử nghiệm cho thấy mô hình kết hợp đạt độ chính xác cao hơn so với từng mô hình thành phần, đồng thời giao diện ứng dụng trực quan được xây dựng bằng Tkinter giúp dễ dàng sử dụng. Nghiên cứu kết luận rằng phương pháp Ensemble Learning có tiềm năng ứng dụng thực tiễn trong lĩnh vực y tế, đặc biệt là trong hỗ trợ chẩn đoán bệnh tim.


## 2 Kết quả đạt được
Trong nghiên cứu này, chúng tôi đã huấn luyện và đánh giá hiệu suất của 6 thuật toán học máy phổ biến trên cùng một tập dữ liệu bệnh tim từ UCI. Các mô hình bao gồm: K-Nearest Neighbors (KNN), Random Forest, Logistic Regression, Naive Bayes, Support Vector Machine (SVM) và Decision Tree. Bảng dưới đây tổng hợp các chỉ số đo lường hiệu quả mô hình:


![image](https://github.com/user-attachments/assets/c72892b3-0c13-42bf-b536-bcc3b3b99200)
 
### Đánh giá và phân tích kết quả
KNN đạt độ chính xác kiểm thử cao nhất (95.08%), nhưng có nguy cơ overfitting vì accuracy huấn luyện đạt tuyệt đối (100%). Điều này cho thấy KNN ghi nhớ quá mức dữ liệu huấn luyện, có thể không ổn định với dữ liệu mới.


Random Forest là mô hình cân bằng tốt giữa độ chính xác huấn luyện và kiểm thử (91.80% test accuracy), cho thấy khả năng tổng quát hóa cao, nhờ cơ chế bootstrap và bagging trong quá trình học.


Logistic Regression hoạt động ổn định và có kết quả khá tốt (90.16% accuracy), phù hợp với các bài toán tuyến tính và có khả năng giải thích mô hình.


Naive Bayes có kết quả kiểm thử khá tốt dù mô hình đơn giản (88.52%), cho thấy thuật toán này phù hợp với bài toán khi các thuộc tính độc lập tương đối.


SVM đạt độ chính xác huấn luyện cao (94.61%) nhưng kiểm thử thấp hơn (85.25%), có thể do mô hình chưa tối ưu được siêu tham số (kernel, C).


Decision Tree có mức chênh lệch lớn giữa train (93.78%) và test (81.97%), cho thấy dấu hiệu overfitting nghiêm trọng nếu không có cắt tỉa hoặc giới hạn độ sâu.


Github tham khảo : https://github.com/g-shreekant/Heart-Disease-Prediction-using-Machine-Learning/tree/master
link google drive để chạy 3 giải thuật: https://drive.google.com/drive/folders/14oVJdCe7swG-t19P5qqexoDkJRrGjLkG?usp=sharing
