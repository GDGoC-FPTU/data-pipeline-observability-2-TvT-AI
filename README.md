[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24112993&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student ID:** 2A202600744
**Name:** Trần Văn Thắng

---

## Mo ta

Bài lab này xây dựng một pipeline ETL đơn giản để đọc dữ liệu JSON, loại bỏ bản ghi không hợp lệ, tính giá giảm 10%, chuẩn hóa danh mục sản phẩm và lưu kết quả ra CSV. Kết quả gồm 3 bản ghi hợp lệ từ 5 bản ghi gốc, với 2 bản ghi bị loại do giá không đúng hoặc danh mục rỗng.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
python agent_simulation.py
```

---

## Ket qua

Sau khi chay pipeline, file `processed_data.csv` duoc tao ra voi 3 ban ghi hop le. 2 ban ghi bi loai do:
- `price <= 0`
- `category` rong

File `processed_data.csv` bao gom cac cot: `id`, `product`, `price`, `category`, `discounted_price`, `processed_at`.

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

(Tom tat ket qua: bao nhieu records da xu ly, bao nhieu bi loai, v.v.)
