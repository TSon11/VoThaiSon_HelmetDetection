# 🪖 Helmet & Rider Detection using YOLOv8 + Roboflow API

Ứng dụng phát hiện **người lái xe máy (rider)** và **mũ bảo hiểm (helmet)** trong hình ảnh, được xây dựng bằng **YOLOv8** kết hợp **Roboflow Inference API**, và triển khai giao diện trực quan bằng **Streamlit**.

---

## 🎯 Mục tiêu

- Phát hiện và phân loại **người lái xe máy** có hoặc không đội mũ bảo hiểm.  
- Hỗ trợ **giám sát an toàn giao thông** hoặc **phân tích video giám sát**.  
- Cung cấp **giao diện web thân thiện**, chạy trực tiếp bằng Streamlit.

---

## ⚙️ Công nghệ sử dụng

| Thành phần | Mô tả |
|-------------|--------|
| **YOLOv8 (Ultralytics)** | Mô hình phát hiện đối tượng (Object Detection) |
| **Roboflow Inference API** | Chạy mô hình online qua cloud API |
| **Streamlit** | Xây dựng giao diện web đơn giản và nhanh |
| **Python 3.11** | Ngôn ngữ lập trình chính |
| **OpenCV · Pillow · Torch · NumPy** | Thư viện xử lý ảnh và tính toán |

---

## 🧾 Dataset

Bộ dữ liệu được quản lý trên **Roboflow Project “[danguit2-wxror](https://app.roboflow.com/danguit2-wxror)”**.  
Mục tiêu: phát hiện **rider**, **helmet**, và **no-helmet** trong nhiều điều kiện ánh sáng và góc chụp khác nhau.

**Thông tin tổng quan:**
- Tổng số ảnh: ~**5.000**  
- Định dạng: JPG / PNG  
- Chia tập dữ liệu:  
  - Train: **80%**  
  - Validation: **10–15%**  
  - Test: **5–10%**

---

## 📊 Hiệu suất mô hình

Mô hình được huấn luyện bằng **YOLOv8** trên **Roboflow Train** và triển khai bằng **Inference SDK**.

| Chỉ số | Giá trị |
|:-------|:--------|
| **mAP50** | **93.2%** |
| **mAP50-95** | **82.4%** |
| **Precision** | **92.7%** |
| **Recall** | **91.3%** |

> 📈 *Kết quả được đo trên tập validation của phiên bản `detect-rider2/3`.*

---

## 💻 Demo ứng dụng

Người dùng có thể:
- Tải ảnh lên hoặc chụp trực tiếp từ camera.  
- Ứng dụng hiển thị kết quả nhận diện và bounding boxes trực tiếp trên ảnh.  
- Giao diện thân thiện, thao tác dễ dàng.

🎥 **Video minh họa kết quả:**
[![Watch the video][(https://img.youtube.com/vi/<VIDEO_ID>/0.jpg)](https://www.youtube.com/watch?v=<VIDEO_ID>)
](https://drive.google.com/file/d/1PEKz70paqt8j5T3_V44_tWrzQP4Tcxyi/view?usp=drive_link)
---

## 🚀 Hướng dẫn chạy

```bash
# Cài đặt thư viện cần thiết
pip install ultralytics streamlit inference-sdk opencv-python pillow torch torchvision

# Chạy ứng dụng
streamlit run Method2.py
