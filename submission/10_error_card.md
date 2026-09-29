# Error analysis card

## Zone × block

| zone | block | what | count |
|---|---|---|---:|
| center | B4 | IGNORE_SCOPE | 2 |
| center | B4 | MISSING | 5 |
| center | B4 | SPURIOUS | 15 |
| center | B4 | WRONG_CLASS | 1 |
| center | C0 | SPURIOUS | 3 |
| edge | B4 | MISSING | 1 |
| edge | B4 | SPURIOUS | 3 |
| edge | C0 | WRONG_CLASS | 1 |
| mid | B4 | IGNORE_SCOPE | 4 |
| mid | B4 | MISSING | 5 |
| mid | B4 | SPURIOUS | 5 |
| mid | B4 | WRONG_CLASS | 1 |

## Top defects
- SPURIOUS: 26 (ví dụ frame adasind_019560.jpg)
- MISSING: 11 (ví dụ frame adasind_271039.jpg)
- IGNORE_SCOPE: 6 (ví dụ frame adasind_270517.jpg)

## Phân tích của bạn

Hai bảng trên do `python3 lab11.py card` tính từ `findings.csv`; chạy lại lệnh sẽ cập nhật bảng và giữ nguyên mục này. Viết cho lỗi nổi bật nhất, dẫn frame/`object_ref`.

- Nguyên nhân khả dĩ (`why`) và vì sao bạn nghĩ vậy: Done
- Cách sửa và ai nhận việc (`owner`): Done
- Bằng chứng (ảnh trong `screenshots/`, dòng findings, rule): Done
