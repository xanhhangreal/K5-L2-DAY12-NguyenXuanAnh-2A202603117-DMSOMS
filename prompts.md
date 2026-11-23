# Khai báo dùng AI — Nguyễn Xuân Anh

Không dùng AI thì xóa bảng và ghi: **Không dùng.**

Nhắc lại: không đưa ảnh cabin hay ảnh tài xế (kể cả ảnh chụp màn hình) cho bất kỳ công cụ AI nào.

| # | Công cụ | Bạn hỏi gì (tóm tắt) | Bạn dùng kết quả thế nào | Bạn có kiểm lại không? Bằng gì? |
|---|---|---|---|---|
| 1 | Codex | Lên kế hoạch Day 12 theo hình thức cá nhân | Sắp thứ tự gán nhãn, checkpoint và review chéo | Chờ học viên đối chiếu GUIDE và CHECKPOINTS |
| 2 | Codex | Triển khai phần chuẩn bị của kế hoạch | Clone repo, chuẩn bị biểu mẫu và kiểm tra môi trường | Đã chạy cabin_check --help trên máy |
| 3 | Codex | Rà Day 12 theo SUBMISSION.md và chuẩn bị commit | Soạn bản nháp danh sách lớp, rà bằng chứng và cập nhật checklist | Đối chiếu cabin_schema.py, RULES.md và các file có trong repo. Hai tình huống trong danh sách lớp là giả định. |
| 4 | Codex | Tạo project và task theo README từ gói G06 | Nhập schema và 22 ảnh vào CVAT local | Kiểm danh sách tên ảnh và số khung sau khi CVAT tạo job. |
| 5 | Codex, YOLO11l và SAM ViT-B local | Chạy thử prelabel trên bản sao G06 | Nhập 31 box và 22 tag tự động vào job 31 để học viên duyệt | Đọc lại nguồn auto trong CVAT, export XML và chạy ba phạm vi của cabin_check. |
