# Olist Customer Segmentation & Hybrid Recommendation System 🚀

## 📌 Tổng quan dự án (Overview)
Dự án tập trung vào việc phân loại 100,000 khách hàng của Olist (Sàn TMĐT lớn nhất Brazil) và xây dựng hệ thống gợi ý sản phẩm cá nhân hóa. Kết quả hỗ trợ đội ngũ Marketing tối ưu hóa chiến dịch quảng cáo và giúp đội ngũ Dev cải thiện trải nghiệm người dùng.

---

## 🏗️ Cấu trúc dự án theo mô hình S.T.A.R

### 1. Situation (Bối cảnh)
* **Dữ liệu:** 100,000 đơn hàng thực tế từ năm 2016 - 2018 tại Brazil.
* **Vấn đề:** Olist có lượng khách hàng khổng lồ nhưng chưa có chiến lược tiếp thị riêng biệt cho từng nhóm, dẫn đến chi phí Ads cao nhưng hiệu quả giữ chân khách hàng (Retention) chưa tối ưu.

### 2. Task - Nhiệm vụ
* **Phân khúc:** Sử dụng mô hình RFM (Recency, Frequency, Monetary) để định danh các nhóm khách hàng.
* **Gợi ý:** Xây dựng hệ thống Hybrid Recommendation giúp gợi ý đúng sản phẩm, đúng phân khúc.

### 3. Action (Hành động)
* **Data Integration:** Kết nối và xử lý logic cho 8 bảng dữ liệu gốc (Orders, Customers, Payments, Reviews...).
* **Feature Engineering:** Tính toán bộ chỉ số RFM và xử lý độ lệch (Skewness) bằng Log Transformation.
* **Machine Learning:** - Sử dụng thuật toán **K-Means Clustering** để phân cụm.
    - Tìm số cụm tối ưu qua **Elbow Method** và **Silhouette Score**:
    ![Biểu đồ Elbow và Silhouette](Images\image-1.png)
* **Recommendation System:** - Xây dựng **Item-Item Collaborative Filtering** bằng ma trận thưa (Sparse Matrix) để tối ưu RAM.
    - Phát triển cơ chế **Hybrid Filter** (Lọc theo sở thích cá nhân + Đặc trưng phân cụm).

### 4. Result (Kết quả)
* **Phân cụm:** Xác định được 4 nhóm khách hàng mục tiêu: **VIP, Chủ lực (Mainstream), Tiềm năng (Potential)** và **Nguy cơ rời bỏ (At Risk)**.
* **Hệ thống gợi ý:** Đưa ra danh sách Top 5 sản phẩm cá nhân hóa với điểm tương đồng (Similarity Score) vượt trội so với gợi ý đại trà.
* **Chiến lược:** Đề xuất 4 giải pháp Marketing riêng biệt cho từng nhóm nhằm tăng tỷ lệ chuyển đổi.

---

## 🛠️ Công nghệ sử dụng (Tech Stack)
* **Ngôn ngữ:** Python
* **Thư viện:** Pandas, NumPy, Scikit-learn, Scipy (Sparse Matrix), Matplotlib, Seaborn.
* **Công cụ:** VS Code, Jupyter Notebook.

---

## 📊 Kết quả Demo
![DEMO HỆ THỐNG RS](Images\image.png)
## 👉 [https://drive.google.com/drive/folders/1GfE_vmKSdH2sVLqLbxXIka9292G3tlYs?usp=sharing]