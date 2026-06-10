# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600744
**Name:** Trần Văn Thắng
**Date:** 6-10-2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Agent returns the best electronic product correctly based on valid data. | 8 | Data is clean and contains valid prices/categories. |
| Garbage Data (`garbage_data.csv`) | Agent likely fails or reports an error due to invalid rows, bad prices, or missing categories. | 3 | Garbage data breaks validation and makes inference unreliable. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Khi du lieu la garbage, cac ban ghi co gia <= 0 hoac category rong se lam sai logic cua Agent. Du lieu khong hop le khong chi lam sai ket qua tinh toan tren price ma con lam cho viec loc thong tin bi loi. Neu Agent su dung category de tim mat hang, thi category rong hoac sai kieu se khong duoc xet duoc. Ngoai ra, du lieu nhieu loi lam cho ham preprocess phai loai bo ban ghi, va neu Agent tu tin lay tat ca ban ghi se gay ra ket qua khong chinh xac.

Trong thuc te, pipeline ETL phai danh dau, loai bo va chuan hoa du lieu truoc khi truyen cho Agent. Neu bo qua buoc validation, Agent co the dong y voi cac mat hang khong hop le va de xuat thong tin sai. Do do, doi voi bai toan nay, chat luong du lieu quan trong hon prompt vi loi du lieu co the lam loi toan bo ket qua.

---

## 3. Ket luan

**Quality Data > Quality Prompt?**

Dong y. Du lieu chat luong cao cho phep Agent dong goi thong tin dung va thuc hien su ra quyet dinh chinh xac hon. Prompt tot giup huong dan Agent, nhung neu du lieu dau vao bi loi thi ket qua van se sai. Do do, trong he thong AI du lieu hop le va quan sat chat luong la yeu to trung tam.
