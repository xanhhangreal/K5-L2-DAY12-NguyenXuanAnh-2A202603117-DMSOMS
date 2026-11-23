# Danh sách lớp v0 — Nguyễn Xuân Anh · 2A202603117

## DMS — theo dõi tài xế

| Lớp hoặc thuộc tính | Giá trị | Để làm gì | Khả năng quan sát trên IR |
|---|---|---|---|
| face.eye_left | open / closed / unknown | Theo dõi thời gian nhắm mắt trái qua nhiều khung | Cần thấy mí mắt trái của tài xế. |
| face.eye_right | open / closed / unknown | Đánh giá mắt phải độc lập khi mắt trái bị che | Phản xạ trên một tròng kính có thể che riêng mắt phải. |
| face.gaze_zone | road / mirror_l / mirror_r / mirror_c / cluster / center / lap / other | Phân biệt nhìn gương với nhìn xuống đùi | Cần đủ chi tiết để phân biệt các vùng nhìn. |
| face13 | 13 mốc mắt, mũi và miệng | Theo dõi hình học khuôn mặt giữa các khung | Mặt rộng từ 60 px mới gán; từng điểm có cờ che khuất hoặc ngoài ảnh. |
| hand.on_wheel | yes / no / unknown | Xác định tay có đặt trên vô lăng | Chỗ tiếp xúc có thể khuất sau vành lái. |
| phone.state | held / mounted / lap | Phân biệt điện thoại cầm tay với điện thoại gắn giá hoặc nằm trên đùi | Dựa vào hình dạng và vị trí tương đối với bàn tay, giá đỡ hoặc đùi. |

## OMS — theo dõi khoang hành khách

| Lớp hoặc thuộc tính | Giá trị | Để làm gì | Khả năng quan sát trên IR |
|---|---|---|---|
| person.seat | driver / front_passenger / rear_left / rear_middle / rear_right | Xác định ghế có người để nhắc kiểm tra đúng vị trí | Dựa vào hình người và vị trí ghế theo hệ tọa độ của xe. |
| person.seatbelt | worn_correct / worn_incorrect / not_worn / unknown | Kiểm tra tình trạng dây theo từng người | Chỉ kết luận khi nhìn đủ đường đi của dây. |
| child_seat.occupied | no / unknown | Phân biệt ghế trẻ em thấy rõ trống với ghế chưa xác định được | Vật che lòng ghế có thể làm mất căn cứ xác định. |
| infant_seat.facing | rear / front | Ghi nhận hướng đặt nôi so với hướng xe chạy | Cần thấy đủ hình dáng và hướng của nôi. |
| object.type | bag / box / cup / other | Phân biệt đồ đặt trên ghế với hành khách | Dựa vào đường viền và cấu trúc của vật. |
| frame_meta.camera_blocked | yes / no | Nhận biết khung cần kiểm tra vì camera bị che | Xét toàn khung để phân biệt che camera với che riêng một ghế. |

## Hai câu hỏi cho coach

Các mã dưới đây minh họa tình huống giả định. Cần đối chiếu khung thực tế của bộ được giao trước khi nộp.

1. **D01** — Nếu đốm phản xạ chỉ che tâm mắt nhưng vẫn thấy một phần mí, cần thấy đến đâu để phân biệt open và closed? Tạm chọn unknown cho riêng mắt bị che khi phần mí còn lại chưa đủ phân biệt.
2. **S01_ir** — Nếu một túi nằm ngang qua hai ghế và phần đáy bị khuất, dùng điểm tựa hay phần lớn diện tích để chọn seat? Tạm ghi nhận một object loại bag và chờ coach xác định ghế vì schema yêu cầu một vị trí.
