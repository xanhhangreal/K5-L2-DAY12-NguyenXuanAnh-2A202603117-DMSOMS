# SUBMISSION — nộp gì, nộp ở đâu

Hạn: **12:00 trưa ngày hôm sau (giờ Việt Nam, GMT+7)**, trừ khi coach thông báo khác. Nên nộp ngay sau exit ticket. Nộp lên LMS: https://aithucchien.vinuni.edu.vn

## Cấu trúc thư mục nộp

```
K5-L2-DAY12-<HoVaTen>-<MSSV>-DMSOMS/
├── export_final.zip          # E1 – CVAT for images 1.1, KHÔNG kèm ảnh
├── export_final_v2.zip       # E1 – sau review chéo (nếu có sửa)
├── export_extra.zip          # tùy chọn – S09–S10 nếu làm phần mở rộng
├── check_cpA.txt             # E2
├── check_cpB.txt             # E2
├── check_final.txt           # E2 – 0 lỗi; mỗi WARN có 1 dòng giải thích ở cuối
├── check_final_v2.txt        # E2 – chạy lại sau khi sửa (nếu có v2)
├── disagreement_log.csv      # E3 – đã điền verdict / guideline_rule / action
├── ir_log.csv                # E4
├── class_list_v0.md          # E5
├── self_review.md            # tự đánh giá (mẫu ở templates/)
├── exit_ticket.md
├── TEAM.md                   # nhóm: ai review ai; cá nhân: tên bạn được ghép
└── prompts.md                # khai báo dùng AI
```

Nén cả thư mục thành `K5-L2-DAY12-<HoVaTen>-<MSSV>-DMSOMS.zip` rồi nộp. `<HoVaTen>` viết liền, không dấu, ví dụ `K5-L2-DAY12-NguyenVanAn-2A202600000-DMSOMS.zip`. Mã bộ ảnh `Gxx` ghi trong `TEAM.md`.

## Bảng bằng chứng

| Mã | File | Coach kiểm bằng gì |
|---|---|---|
| E1 | `export_final.zip` (+ `_v2`) | Chạy `cabin_check check --expect 22` |
| E2 | `check_cpA.txt`, `check_cpB.txt`, `check_final.txt` | Kiểm đúng phạm vi ở từng checkpoint, sửa các lỗi trước lần kiểm cuối và giải thích các cảnh báo còn lại |
| E3 | `disagreement_log.csv` | Ít nhất 5 dòng đã xử lý (hoặc tất cả nếu ít hơn 5) |
| E4 | `ir_log.csv` | Ít nhất 4 quan sát; cột `source` tách `real_IR` (D##) và `IR_sim` (S##) |
| E5 | `class_list_v0.md` | Ít nhất 6 lớp DMS + 6 lớp OMS, mỗi lớp có cột "để làm gì"; 2 câu hỏi leo thang có khung ví dụ |

## Trước khi nộp — kiểm 5 điều

1. `python -m zipfile -l export_final.zip` (chạy được trên Windows, macOS, Linux) chỉ thấy `annotations.xml`, không có `.png`/`.jpg`.
2. `check_final.txt` có dòng `Kết quả: 0 lỗi`.
3. Tên file đúng như trên (coach chấm bằng script).
4. Không kèm `manifest.csv`, ảnh, hay thư mục `Gxx/`.
5. `prompts.md` có mặt.
## Đối chiếu ngày 23/11/2026

| Bằng chứng | Tình trạng |
|---|---|
| E1 | Chưa có export CVAT của 22 ảnh. |
| E2 | Chưa có export để kiểm checkpoint A, B và lần cuối. |
| E3 | Chờ hai bản export cùng mã bộ ảnh và kết quả phân xử với bạn review. |
| E4 | Nhật ký có tiêu đề cột. Cần ít nhất 4 quan sát thực tế, ghi đúng nguồn. |
| E5 | Bản nháp có 6 mục DMS và 6 mục OMS. Hai câu hỏi đang dùng khung giả định, cần học viên đối chiếu trong job G06. |

Đã tạo task Day12-G06 (ID 30) trong project Day12 (ID 6) trên CVAT local v2.74.1. Đã kiểm đủ 8 cặp S01–S08 và 6 khung D01–D06. TEAM.md còn chờ tên bạn review. Phần tự rà soát 4 ảnh và đáp án exit ticket chờ học viên điền. Chưa đóng gói bộ nộp LMS.
