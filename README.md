**1. Giới thiệu về Phân loại Cảm xúc**

Phân loại cảm xúc (Sentiment Analysis) là một nhánh quan trọng trong Xử lý Ngôn ngữ Tự nhiên (NLP), tập trung vào việc xác định và phân loại cảm xúc hoặc thái độ trong văn bản. Đối với tiếng Việt, việc phân loại cảm xúc đối mặt với nhiều thách thức do đặc thù ngôn ngữ và thiếu hụt tài nguyên ngôn ngữ chất lượng cao.

**2. Bộ dữ liệu VLSP 2018**

Năm 2018, Hội thảo Xử lý Ngôn ngữ và Tiếng nói Việt Nam (VLSP) đã tổ chức một cuộc thi về phân tích cảm xúc, cung cấp bộ dữ liệu chuẩn cho cộng đồng nghiên cứu. Bộ dữ liệu này bao gồm các đánh giá sản phẩm từ các trang thương mại điện tử, được gán nhãn cảm xúc tích cực, tiêu cực hoặc trung tính. Đây là nguồn dữ liệu quan trọng giúp thúc đẩy nghiên cứu và phát triển các mô hình phân loại cảm xúc cho tiếng Việt.
Đường link github: https://github.com/ds4v/absa-vlsp-2018
Lĩnh vực khách sạn và nhà hàng 
**3. Mô hình PhoBERT**

PhoBERT là một mô hình ngôn ngữ tiền huấn luyện dựa trên kiến trúc Transformer, được tối ưu hóa cho tiếng Việt. Được phát triển dựa trên BERT, PhoBERT tận dụng dữ liệu tiếng Việt lớn để học các đặc trưng ngôn ngữ, giúp cải thiện hiệu suất trong các tác vụ NLP, bao gồm phân loại cảm xúc. Việc sử dụng PhoBERT đã chứng minh hiệu quả vượt trội so với các mô hình truyền thống trong nhiều nghiên cứu. 
JOS.HUEUNI.EDU.VN

**4. Ứng dụng PhoBERT trong Phân loại Cảm xúc**

Việc áp dụng PhoBERT trong phân loại cảm xúc tiếng Việt đã thu hút sự quan tâm của nhiều nhà nghiên cứu. Các bước triển khai thường bao gồm tiền xử lý văn bản, phân đoạn từ, mã hóa bằng tokenizer của PhoBERT và huấn luyện mô hình trên bộ dữ liệu đã gán nhãn. Một số nghiên cứu đã chỉ ra rằng PhoBERT cải thiện đáng kể độ chính xác trong phân loại cảm xúc so với các phương pháp trước đó.

**5. Cụ thể, bài toán chúng tôi thực hiện là Phân tích Cảm xúc theo Danh mục Khía cạnh (Aspect Category Sentiment Analysis - ACSA), bao gồm hai nhiệm vụ con:**

A. Phát hiện Danh mục Khía cạnh (Aspect Category Detection - ACD)
Xác định thực thể (E - Entity) và thuộc tính (A - Attribute) được biểu đạt trong một câu đánh giá.

E và A được chọn từ tập các thực thể và thuộc tính được định nghĩa trước.
Ví dụ:
Thực thể: "ROOMS" (phòng), "HOTEL" (khách sạn)
Thuộc tính: "PRICE" (giá cả), "QUALITY" (chất lượng)
B. Phân loại Cảm xúc theo Khía cạnh (Sentiment Polarity Classification - SPC)
Mỗi cặp E#A được gán một nhãn cảm xúc:

"Positive" (tích cực)
"Negative" (tiêu cực)
"Neutral" (trung lập)
Ví dụ:

Câu tiếng Việt: "Phòng rộng rãi, thoáng mát, nhân viên phục vụ tận tình."
Dịch sang tiếng Anh: "The room is spacious, airy, staff is enthusiastic."
Nhận diện cảm xúc theo khía cạnh:
{cate: "ROOMS#DESIGN", pol: "positive"}
{cate: "SERVICE#GENERAL", pol: "positive"}
