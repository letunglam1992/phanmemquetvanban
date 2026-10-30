# Nhật ký thay đổi: tác vụ quét iOffice

## v2 (30/10/2026): Nhiệm vụ Phòng Kế hoạch - Tài chính theo thành viên
- Đọc tab **Cau hinh quet KHTC** mỗi lượt: từ khóa giao phòng (Chủ trì/Tham mưu/Phối hợp, bật/tắt được) và danh sách thành viên (Tên gọi, Họ tên đầy đủ trên iOffice, Bí danh).
- Nhận diện văn bản đến giao Phòng KHTC; ghi cột **P “Vai trò phòng”**. Việc giao riêng Lâm tham mưu giữ nguyên quy tắc v1 và ghi `Cá nhân tham mưu`.
- Đọc bước Lê Tùng Lâm “Chuyển xử lý” cho thành viên; ghi Tên gọi vào cột M. Chưa chuyển thì ghi `Chưa phân công` và quét lại ở các lượt sau (`khtc_unassigned`). Không ghi đè M người dùng đã sửa tay (`khtc_assignee_written`).
- Văn bản đi đã phát hành do thành viên soạn thảo được dùng để tự hoàn thành nhiệm vụ của chính người đó (quy tắc khớp chặt như v1).
- Mốc kích hoạt nhóm KHTC là ô J4 của tab cấu hình (ngày triển khai), có baseline riêng `khtc_baseline`; không quét bù.
- Không ghi vào các cột ẩn của Calendar / báo văn bản mới.
- Yêu cầu: Apps Script dashboard v7 và đã chạy `caiDatTheoDoiKHTC`.

## v1 (24/09/2026)
- Quét văn bản đến giao Lê Tùng Lâm tham mưu, văn bản đi chờ/đã phát hành do Lâm soạn; ghi tab `Danh sach nhiem vu` A–O.
