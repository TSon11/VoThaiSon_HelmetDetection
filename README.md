# 🪖 Helmet & Rider Detection

Ứng dụng phát hiện **người lái xe máy (rider)** và **mũ bảo hiểm (helmet)** trong hình ảnh, được xây dựng bằng **YOLOv8** kết hợp **Roboflow Inference API**, và triển khai giao diện trực quan bằng **Streamlit**.

---

## 🎯 Mục tiêu

- Phát hiện và phân loại **người lái xe máy** có hoặc không đội mũ bảo hiểm.  
- Hỗ trợ **giám sát an toàn giao thông** hoặc **phân tích video giám sát**.  
- Cung cấp **giao diện web thân thiện**, chạy trực tiếp bằng Streamlit.
---
## 🎥 Video Demo

<video width="720" controls>
  <source src="https://github.com/TSon11/VoThaiSon_HelmetDetection/issues/1#issue-3501559001">
  Your browser does not support the video tag.
</video>
*Nhấn ▶ để xem video minh họa kết quả*

## 🧾 Dataset

Bộ dữ liệu được quản lý trên **Roboflow Project**.  
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

## 🚀 Hướng dẫn chạy

```bash
# Cài đặt thư viện cần thiết
pip install ultralytics streamlit inference-sdk opencv-python pillow torch torchvision

# Chạy ứng dụng
streamlit run Method2.py
