# So sánh L với R

Chỉ số L/R là thứ tự box cao ≥ H=40 trong từng frame, theo thứ tự XML; bắt đầu từ 1.
Box L trong ignore_region được báo IGNORE_SCOPE, không tính SPURIOUS.

## adasind_270517.jpg
- L3 mid IGNORE_SCOPE
## adasind_271039.jpg
- L10 center IGNORE_SCOPE
- L3 center SPURIOUS
- L4+R7 mid WRONG_CLASS
- L8 center SPURIOUS
- L12 edge SPURIOUS
- L13 center SPURIOUS
- L14 center SPURIOUS
- R6 mid MISSING
- R10 center MISSING
## adasind_295948.jpg
- L1 mid IGNORE_SCOPE
- L5 mid IGNORE_SCOPE
- L6 mid IGNORE_SCOPE
- L7 center IGNORE_SCOPE
- L2+R1 center WRONG_CLASS
- L4 center SPURIOUS
- R3 mid MISSING

## Theo zone
| zone | n_ref | matched | missing | spurious |
|---|---|---|---|---|
| center | 12 | 10 | 2 | 6 |
| mid | 5 | 2 | 3 | 1 |
| edge | 3 | 3 | 0 | 1 |
