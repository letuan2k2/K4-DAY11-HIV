# Sensor context

Slice B4-center gồm ba frame: `adasind_270517.jpg`, `adasind_271039.jpg`, `adasind_295948.jpg`.
Mọi mô tả dưới đây ghi theo quan sát trên ảnh, vì ADASIND không kèm tài liệu rig.

- Rig: Một camera fisheye duy nhất, ảnh dọc 1080×1920, nhìn về phía trước theo chiều đường.
  Camera đặt thấp, ngang tầm người ngồi trên xe, và có người/thân xe ở ngay sát ống kính.
  Vì vậy đây có thể là xe nhỏ chở khách, nhưng không xác định được loại xe, độ cao hay góc lắp.
- ego_body: Nằm ở phần dưới của vòng kính, sát camera.
  - `270517`: thấy ở rìa trái, nửa dưới (tay, áo kẻ caro, chân và dép của người trên xe), kéo xuống tới đáy vòng kính.
  - `295948`: thấy ở hai bên nửa dưới (người áo caro bên trái, người quấn khăn đỏ bên phải) và phần tối ở đáy vòng kính.
  - `271039`: không thấy thân xe nên không vẽ polygon `ego_body` (đúng với ngoại lệ trong GUIDE).
- Vòng kính (lens circle): Là một hình tròn bán kính khoảng 790–815 px. Tâm hơi lệch sang trái so với giữa ảnh (cx ≈ 417–496, cy ≈ 890–990).
  Đường kính (~1600 px) lớn hơn chiều ngang ảnh, nên vòng kính bị cắt ở hai cạnh trái/phải.
  Theo chiều dọc, vòng kính kéo dài khoảng từ y ≈ 100–175 đến y ≈ 1685–1800. Phần trong vòng kính chiếm khoảng 75–78% khung hình.
  Vành tối (`lens_border`) nằm ở dải trên và dải dưới ảnh, ngoài cung tròn. Hai polygon `lens_border` mỗi frame đến từ prefill; khi làm cần soát chúng khớp mép vòng kính thật.
- Méo và điều kiện ảnh: Vật ở rìa vòng kính bị kéo cong và co nhỏ. Frame `295948` bị ngược sáng mạnh, có lóe sáng (flare) ở giữa và phía trên.
- Giới hạn: Chỉ có ảnh từ một camera, không có calibration, độ sâu, timestamp hay camera khác để đối chiếu.
  Không suy ra khoảng cách, vùng lái an toàn hay góc nhìn của hệ SVM bốn camera từ ba ảnh này.
