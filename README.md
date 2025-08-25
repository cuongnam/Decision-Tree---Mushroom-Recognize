🍄 Mushroom Prediction – Dự đoán nấm ăn được hay độc

Ứng dụng dự đoán nấm có ăn được hay không dựa trên một số đặc trưng như:

- Mùi (odor)

- Màu mũ nấm (cap-color)

- Màu phiến nấm (gill-color)

Mô hình học máy được huấn luyện từ bộ dữ liệu Mushroom (UCI dataset). Người dùng có thể nhập thông tin đặc trưng của nấm và hệ thống sẽ dự đoán ăn được (Edible) hoặc độc (Poisonous).

⚙️ Sử dụng công nghệ, thuật toán, ngôn ngữ lập trình gì

Ngôn ngữ: Python (huấn luyện mô hình & GUI Tkinter) + HTML/JavaScript (Web demo)

Thư viện:

- scikit-learn để xây dựng mô hình Decision Tree

- pickle để lưu mô hình

- tkinter để tạo giao diện desktop

Thuật toán: Decision Tree (Cây quyết định)

Giao diện web: HTML + CSS + JavaScript, có thể upload mô hình ở dạng .json để dự đoán

🖼️ Một số giao diện cơ bản

Giao diện Web

<img width="1077" height="551" alt="image" src="https://github.com/user-attachments/assets/588cebff-20d3-464b-a273-8ae008d348ce" />

Form chọn 3 thuộc tính (mùi, màu mũ, màu phiến)

<img width="1035" height="151" alt="image" src="https://github.com/user-attachments/assets/0f996ebb-75f2-4eda-82ac-a127906cf565" />

Nút Dự đoán

<img width="285" height="78" alt="image" src="https://github.com/user-attachments/assets/5fd01a47-c5e8-4762-9839-eaefea2c4ff6" />

Hiển thị kết quả:

<img width="1078" height="624" alt="image" src="https://github.com/user-attachments/assets/0395f39c-2b1d-4dcd-8d3f-3af8e76672e6" />

🍄 Nấm ăn được (Edible)

☠️ Nấm độc (Poisonous)

🚀 Cách chạy project
1. Chạy giao diện Desktop (Tkinter)
```bash
Clone repo:

git clone https://github.com/<your-username>/mushroom-prediction.git
cd mushroom-prediction
```

Cài đặt thư viện cần thiết:

```bash
pip install scikit-learn
```
Chạy file Python giao diện:
```bash
python mushroom_gui.py
```
2. Tạo ra file model đã huấn luyện
```bash
run train_model_ID3.py
```

Sau khi hoàn thành ta được file 'mushroom_model.pkl'

3. Chạy giao diện Web

Đảm bảo bạn đã có mô hình dạng JSON (chạy file exchange.py):
```bash
import pickle, json
with open('mushroom_model.pkl','rb') as f:
    tree = pickle.load(f)
with open('mushroom_model.json','w',encoding='utf-8') as f:
    json.dump(tree, f, ensure_ascii=False)
```
Mở file index.html trong trình duyệt.

Bấm Chọn tệp để nạp mushroom_model.json.

Chọn thuộc tính và nhấn Dự đoán để xem kết quả.
