# 📝 Ghi chú Machine Learning - Report Week 2

## 1. Supervised Learning (Học có giám sát)

**Định nghĩa:** Phương pháp học máy mà mô hình được huấn luyện qua tập dữ liệu có nhãn (labeled data). Mục tiêu là tìm ra hàm ánh xạ từ Input ($X$) sang Output ($y$) để dự đoán dữ liệu mới.

### Quy trình xử lý:
1.  **Thu thập & Gán nhãn dữ liệu:** Tổng hợp thông tin thành dataset và gán nhãn.
2.  **Tiền xử lý dữ liệu (Data Preprocessing):**
    * *Xử lý dữ liệu thiếu:* Xóa bỏ hoặc điền giá trị trung bình.
    * *Xử lý dữ liệu nhiễu/ngoại lai:* Xóa bỏ hoặc điền giá trị trần/sàn.
    * *Mã hóa dữ liệu:*
        * Mã hóa nhãn (Label Encoding): Dùng cho dữ liệu có thứ tự.
        * One-hot encoding: Dùng cho dữ liệu không thứ tự (ví dụ: N, a, y, n -> vector 0/1).
    * *Chuẩn hóa dữ liệu:*
        * Normalization (Max-Min scaling): Nén dữ liệu về đoạn [0, 1].
        * Standardization (Z-score scaling): Đưa về phân phối chuẩn (mean=0), giá trị >3 thường là outlier.
3.  **Chia Dataset:**
    * *Train set:* Để mô hình học (95% hoặc 80%).
    * *Validation set:* Để tinh chỉnh mô hình (3% hoặc lấy từ train set).
    * *Test set:* Để kiểm tra độ chính xác cuối cùng (2% hoặc 20%).
4.  **Training:** Huấn luyện mô hình, cập nhật trọng số để giảm thiểu sai số.
5.  **Đánh giá (Evaluation):** Dùng các chỉ số như Accuracy, Confusion Matrix, MAE, MSE, F1 score...
6.  **Tối ưu (Optimization):** Tinh chỉnh siêu tham số (hyperparameters).
7.  **Triển khai & Giám sát:** Đưa vào thực tế và cập nhật liên tục.

### Phân biệt Classification & Regression:
* **Classification (Phân loại):** Nhãn đầu ra là biến rời rạc (Ví dụ: Spam/Not Spam).
* **Regression (Hồi quy):** Nhãn đầu ra là biến liên tục (Ví dụ: Dự đoán giá nhà).

---

## 2. Unsupervised Learning (Học không giám sát)

**Định nghĩa:** Làm việc với dữ liệu không nhãn (unlabeled data) để tìm cấu trúc ẩn hoặc gom nhóm dữ liệu.

**Mục tiêu & Ứng dụng:** Phân khúc khách hàng, gợi ý sản phẩm, phát hiện gian lận...

### Phân loại chính:
* **Clustering (Phân cụm):** Gom các điểm dữ liệu giống nhau (Ví dụ: K-Means, DBSCAN).
* **Dimensionality Reduction (Giảm chiều):** Giảm số lượng biến đầu vào nhưng giữ thông tin quan trọng (Ví dụ: PCA, t-SNE).

---

## 3. So sánh Supervised vs Unsupervised Learning

| Tiêu chí | Supervised Learning | Unsupervised Learning |
| :--- | :--- | :--- |
| **Dữ liệu đầu vào** | Có nhãn (Input $X$, Output $y$) | Không nhãn (Chỉ có Input $X$) |
| **Mục tiêu** | Dự đoán kết quả (Prediction) | Khám phá cấu trúc (Discovery) |
| **Độ phức tạp** | Dễ đánh giá hơn (có Ground Truth) | Khó đánh giá hơn |
| **Thuật toán** | Linear Reg, SVM, Decision Tree... | K-Means, PCA, Apriori... |

---

## 4. Các thuật toán tiêu biểu

### Supervised:
* **Linear Regression:** Tìm đường thẳng/mặt phẳng khớp nhất với dữ liệu liên tục.
* **Logistic Regression:** Phân loại xác suất (thường là nhị phân) dùng hàm Sigmoid.
* **Decision Tree:** Ra quyết định dựa trên quy tắc if-else dạng cây.
* **SVM (Support Vector Machine):** Tìm siêu phẳng phân chia các lớp với lề (margin) lớn nhất.
* **KNN (K-Nearest Neighbors):** Phân loại dựa trên "bầu cử" của $k$ điểm lân cận.

### Unsupervised:
* **K-Means:** Phân chia dữ liệu thành $K$ cụm dựa trên khoảng cách đến tâm cụm.
* **DBSCAN:** Phân cụm dựa trên mật độ (tốt cho dữ liệu nhiễu/hình dạng phức tạp).
* **PCA (Principal Component Analysis):** Chiếu dữ liệu sang không gian ít chiều hơn, giữ phương sai lớn nhất.