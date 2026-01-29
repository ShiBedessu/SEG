# Vietnamese Constitution Law Retrieval System

Dự án này là **bài tập / dự án cá nhân trong trường học**, tập trung vào **truy xuất văn bản pháp luật Việt Nam (Hiến pháp)**. Hệ thống sử dụng cả **sparse retrieval (BM25)** và **dense retrieval (embedding)** để tìm kiếm và so sánh hiệu quả truy vấn văn bản pháp luật.

---

## Cấu trúc thư mục

```
.
├── data_retrieve.ipynb   # Test kết nối & truy xuất dữ liệu từ database
├── VNlaws.py             # Xử lý dữ liệu luật (làm sạch, chuẩn hoá, tách điều/khoản)
├── Sparse_BM25.ipynb     # Truy xuất văn bản pháp luật bằng BM25
├── Dense_me5base.ipynb  # Truy xuất bằng dense embedding
├── Main.ipynb            # Notebook tổng hợp & so sánh kết quả
└── README.md             # Tài liệu mô tả dự án
```

---

## Mục tiêu dự án

* Làm quen với bài toán **Information Retrieval (IR)**
* Áp dụng vào **văn bản pháp luật Hiến pháp Việt Nam**
* So sánh hai hướng tiếp cận:

  * **Sparse Retrieval (BM25)**
  * **Dense Retrieval (Semantic Search)**
* Phục vụ mục đích **học tập, nghiên cứu cá nhân**, không dùng cho mục đích thương mại

---

## Yêu cầu môi trường

* Python >= 3.10
* Jupyter Notebook

Thư viện chính:

```bash
pip install numpy pandas scikit-learn rank-bm25
pip install sentence-transformers torch
pip install underthesea pyvi
```

---

## Hướng dẫn sử dụng

### 1️⃣ Kiểm tra kết nối dữ liệu

```text
data_retrieve.ipynb
```

* Dùng để **test kết nối database**
* Load dữ liệu văn bản luật (Hiến pháp)
* Kiểm tra dữ liệu đầu vào cho pipeline truy xuất

---

### 2️⃣ Sparse Retrieval (BM25)

```text
Sparse_BM25.ipynb
```

* Tokenize văn bản pháp luật tiếng Việt
* Xây dựng chỉ mục BM25
* Truy vấn theo từ khoá
* Phù hợp với câu hỏi dạng chính xác từ ngữ

---

### 3️⃣ Dense Retrieval (Embedding)

```text
Dense_me5base.ipynb
```

* Sử dụng sentence-transformer đa ngôn ngữ
* Encode điều luật & câu hỏi
* So sánh cosine similarity
* Phù hợp với truy vấn mang tính ngữ nghĩa

---

### 4️⃣ Tổng hợp & đánh giá

```text
Main.ipynb
```

* So sánh kết quả BM25 và Dense Retrieval
* Đánh giá khả năng truy xuất văn bản luật
* Phân tích ưu / nhược điểm của từng phương pháp

---

## So sánh nhanh

| Phương pháp | Ưu điểm                  | Nhược điểm                |
| ----------- | ------------------------ | ------------------------- |
| BM25        | Đơn giản, dễ hiểu, nhanh | Không hiểu ngữ nghĩa      |
| Dense       | Hiểu ngữ nghĩa tốt       | Tốn tài nguyên, cần model |

---

## Phạm vi & ghi chú

* Dữ liệu giới hạn trong **Hiến pháp Việt Nam**
* Dự án mang tính **học thuật / cá nhân**
* Code viết để chạy trực tiếp trong Jupyter Notebook
---

Chỉ sử dụng cho mục đích học tập (Educational Use)
