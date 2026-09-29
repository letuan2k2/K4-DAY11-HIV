# Đối chiếu chất lượng cục bộ — rectangle

Teaching reference, không phải gold set đã phê duyệt; không có điểm đạt tự động.
Nguồn: export r1_craft đã khóa SHA256 `ce320bc257a51b169953844d7ebc9d696a02884750b8f6ab98cb85437ba1fa7b`; slice `B4-center`.
Ghép hình học greedy một-một theo IoU ≥ 0.50, rồi so class; H ≥ 40 px.
Box trái nằm chủ yếu trong ignore_region reference không tính. Polygon, polyline, track không được chấm.
Đây là phép tính offline của lab, không phải báo cáo hay kết quả tương đương CVAT Premium.

Frame được tính: adasind_270517.jpg, adasind_271039.jpg, adasind_295948.jpg. Frame thiếu trong export: không.
TP=15; FP=8; FN=5; số lần đối chiếu=26; mean IoU của TP=0.831.

| Chỉ số | Micro | Macro | Nhãn thấp nhất |
|---|---:|---:|---:|
| accuracy | 0.577 | 0.900 | 0.846 |
| precision | 0.652 | 0.633 | 0.500 |
| recall | 0.750 | 0.775 | 0.600 |
| jaccard | 0.536 | 0.519 | 0.429 |
| dice | 0.698 | 0.680 | 0.600 |

| Nhãn | TP | FP | FN | Accuracy | Precision | Recall | Jaccard | Dice |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Bike | 2 | 1 | 1 | 0.923 | 0.667 | 0.667 | 0.500 | 0.667 |
| Car | 3 | 1 | 2 | 0.885 | 0.750 | 0.600 | 0.500 | 0.667 |
| Pedestrian | 6 | 2 | 1 | 0.885 | 0.750 | 0.857 | 0.667 | 0.800 |
| ThreeWheeler | 3 | 3 | 1 | 0.846 | 0.500 | 0.750 | 0.429 | 0.600 |
| Truck | 1 | 1 | 0 | 0.962 | 0.500 | 1.000 | 0.500 | 0.667 |

| Frame | TP | FP | FN | Accuracy | Precision | Recall |
|---|---:|---:|---:|---:|---:|---:|
| adasind_270517.jpg | 7 | 0 | 0 | 1.000 | 1.000 | 1.000 |
| adasind_271039.jpg | 7 | 6 | 3 | 0.467 | 0.538 | 0.700 |
| adasind_295948.jpg | 1 | 2 | 2 | 0.250 | 0.333 | 0.333 |

Confusion matrix: hàng = teaching reference; cột = export đã khóa.
`<missing>` là thiếu box; `<extra>` là box thừa. Xem `local_quality_confusion.csv`.

| Reference \ Export | Bike | Car | Pedestrian | ThreeWheeler | Truck | <missing> |
|---|---:|---:|---:|---:|---:|---:|
| Bike | 2 | 0 | 0 | 0 | 0 | 1 |
| Car | 0 | 3 | 0 | 1 | 1 | 0 |
| Pedestrian | 0 | 0 | 6 | 0 | 0 | 1 |
| ThreeWheeler | 0 | 0 | 0 | 3 | 0 | 1 |
| Truck | 0 | 0 | 0 | 0 | 1 | 0 |
| <extra> | 1 | 1 | 2 | 2 | 0 | 0 |

Chi tiết xung đột trong `local_quality_conflicts.csv`; dữ liệu máy đọc trong `local_quality.json`.
Mismatching label đóng góp một FP cho class vẽ và một FN cho class reference; attribute khác được báo riêng.
Micro accuracy đếm mỗi cặp ghép sai class là một lần đối chiếu; Jaccard đếm cả FP và FN.
Macro/worst bỏ nhãn không xuất hiện ở cả hai phía; chỉ số không có mẫu là N/A.
