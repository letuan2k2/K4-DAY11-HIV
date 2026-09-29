# Thành viên và phân vai — Day11 SVM 360 Fisheye

## 1. Thông tin nhóm
- Khóa/lớp: K4
- Tên nhóm: HIV
- Repo Public: [K4-DAY11-HIV]
- Máy giữ hồ sơ chính / người quản lý: Ngô Văn Hưng (vai C)
- Slice chung lấy từ mode.json: B4-center
- Tên định danh vai A dùng cho --self: tuananh
- Đại diện nộp (vai C): Ngô Văn Hưng, 2A202602094
- Commit chốt bài: [Điền sau khi push]

## 2. Ba vai chính

| Vai | Họ và tên | MSSV | Tên định danh trong mode | Trách nhiệm |
|---|---|---|---|---|
| A · Gán nhãn | Lê Tuấn Anh | 2A202602066 | tuananh | Parking/C0/slice, self-QC, lock, rework |
| B · QA độc lập | Nguyễn Phúc Đại | 2A202602145 | dai | Review trước reference, finding QA, kiểm lại ca sửa |
| C · Chẩn đoán & điều phối | Ngô Văn Hưng | 2A202602094 | hung | Báo cáo, phân xử, kế hoạch, tích hợp, check và nộp |

## 3. Bàn giao theo pha

| Mốc | Người giao → nhận | File / commit / mã khóa | Người nhận đã kiểm gì? | Trạng thái |
|---|---|---|---|---|
| P0 · Chốt môi trường và vai | C → A, B | mode.json, slice B4-center | Đang kiểm | Đang thực hiện |
| P2 · Khóa bản đầu | A → B, C | [XML, lock.txt, slice, code] | [Điền] | Chưa bắt đầu |
| P3 · Chốt QA mù | B → C, A | [review, findings, ảnh] | [Điền] | Chưa bắt đầu |
| P4 · Quyết định sửa | C → A, B | [finding, decision log] | [Điền] | Chưa bắt đầu |
| P5 · Kiểm bản sửa | A → B → C | [v2, lock2, delta] | [Điền] | Chưa bắt đầu |
| P6 · Chốt nộp | A, B → C | [manifest, commit chốt] | [Điền] | Chưa bắt đầu |

## 4. Bất đồng và phối hợp
- Một ca đã phân xử: [Chưa có]
- Ca còn mở: [Chưa có]
- Thay đổi phân công: Không có

## 5. Xác nhận trước khi nộp
- [ ] A xác nhận nhãn và export đúng phiên bản
- [ ] B xác nhận đã QA độc lập trước reference và kiểm lại ca sửa
- [ ] C xác nhận báo cáo đúng bản khóa, các file đầy đủ và check exit 0
- [ ] manifest.json tại commit chốt có failed_gates rỗng
- [ ] Repo nhóm Public, ảnh và bằng chứng mở được
- [ ] C đã push và gửi link repo + commit qua kênh lớp
