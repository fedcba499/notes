
# 🧠 YOLOv11 Training Notes

## ✅ Model Info
- Base Model: `yolov11n.pt`
- Dataset: Aadhaar Card Detection
- Epochs: 50
- Image size: 640x640

## 🛠️ Training Command
```python
model = YOLO("yolov11n.pt")
model.train(data="data.yaml", epochs=50)
