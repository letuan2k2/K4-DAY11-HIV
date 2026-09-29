# Quan sát vạch ô đỗ

- Hai vạch parking_line đã vẽ (mô tả vị trí trong ảnh): Các vạch sơn trắng phân chia ô đỗ xe nằm ở dãy đỗ xe phía trước bãi.
- Một vạch/dấu sơn hoặc biên **không** vẽ, và vì sao: Không vẽ vạch trắng dài nằm ở rìa bãi (phía sau khu vực đỗ xe) vì đó là vạch chỉ dẫn mép đường/lối xe chạy, không phải ranh giới phân chia ô đỗ cụ thể.
- Polygon ree_space dừng ở đâu; có phần bị che nào không: Dừng ở mép của các ô đỗ xe phía trước và phía sau. Không bị che lấp bởi xe cản hay chướng ngại vật nào trong vùng đã khoanh.
- Ca chưa chắc cần hỏi người soát (nếu không có, ghi “không có”): không có
