# Đề xuất gold set theo camera — tình huống giả lập

**Đầu bài:** 50.000 frame từ bốn camera SVM, ngân sách chọn 200 frame để review/gold.

| camera_id | Hard case cần chọn | Vì sao dễ sai | Annotation space / calibration cần giữ | Cách review trước khi gọi là gold |
|---|---|---|---|---|
| front | Xe cắt ngang, ngược sáng | Biến dạng rìa kính lớn khi xe đi vào mép | Viền kính (lens_border) phía dưới | QA mù 2 vòng độc lập |
| rear | Xe bám sát đuôi | Bóng đổ, bụi cản tầm nhìn | Vùng che của biển số/cốp xe | Đo lường độ thống nhất IoU |
| left | Xe máy lách, người đi bộ | Lóe sáng, tốc độ tương đối cao | Đường viền dọc hông xe | Chéo nhau kiểm tra |
| right | Chướng ngại vật sát lề | Khuất tầm nhìn, xe đỗ sát | Phần che của gương chiếu hậu | Review bởi senior QA |

- Khi nào cần refresh gold set: Khi thay đổi cấu hình camera (rig), khi có luật gán nhãn mới hoặc khi phát hiện lỗi hệ thống lặp lại nhiều lần.
- Một ca seam/cross-camera cần policy và evidence trước khi ghép hai box: Cần tham chiếu ID của xe trên cả 2 ảnh camera để đảm bảo nối đúng 1 vật thể.
- Vì sao peer agreement hoặc quality report trên ảnh một camera chưa chứng minh gold set đúng cho cả bốn camera: Mỗi camera có góc lắp, độ méo và điểm mù khác nhau; mô hình có thể tốt ở camera trước nhưng rất tệ ở camera bên hông.
