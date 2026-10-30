# Phần mềm quét văn bản iOffice → Google Sheets

Tác vụ AI định kỳ (09:00, 15:00, 22:00) đọc iOffice Sở Nông nghiệp và Môi trường Sơn La và ghi nhiệm vụ vào Google Sheet dùng chung với dashboard [theodoinhiemvu](https://github.com/letunglam1992/theodoinhiemvu).

| Tệp | Dùng để |
|---|---|
| `PROMPT_DongBo_v2.md` | Prompt của tác vụ định kỳ (phiên bản hiện hành) |
| `CAP_NHAT_v2_KHTC.md` | Lệnh chạy **một lần** khi nâng từ v1 lên v2: kiểm tra Sheet, sao lưu và khởi tạo state |
| `CHANGELOG.md` | Nội dung từng phiên bản |

## Cập nhật lên v2 (Phòng KHTC theo thành viên)

1. **Apps Script (làm trước):** cập nhật `Code.gs` v7 của dashboard, triển khai phiên bản mới, chạy `caiDatTheoDoiKHTC` một lần. Kiểm tra tab **Theo doi phong KHTC** không còn `#ERROR!`.
2. **Điền họ tên đầy đủ trên iOffice** cho từng thành viên ở cột F, tab **Cau hinh quet KHTC**. Sửa từ khóa ở cột A–C nếu cần.
3. **Thay prompt tác vụ định kỳ** bằng toàn bộ nội dung `PROMPT_DongBo_v2.md` (mở tác vụ định kỳ đang chạy → sửa phần hướng dẫn/prompt → dán → lưu). Giữ nguyên lịch chạy, máy chạy và nơi lưu state.
4. **Chạy một lần** nội dung `CAP_NHAT_v2_KHTC.md` trong cùng môi trường (ví dụ: “Chạy ngay” một tác vụ tạm với prompt này, hoặc dán vào phiên làm việc trên cùng máy có Chrome đã đăng nhập iOffice). Đọc báo cáo trả về: phải là “Đã cập nhật lên v2”.
5. Theo dõi 1–2 lượt quét đầu: dòng mới của phòng có cột P, cột M là tên thành viên hoặc `Chưa phân công`. Việc nhận nhầm người: sửa tay cột M (tác vụ không ghi đè) và bổ sung họ tên/bí danh trong tab cấu hình.

Bỏ qua bước 4 vẫn an toàn: prompt v2 tự khởi tạo mốc và baseline ở lượt đầu, chỉ không có bản sao state và báo cáo kiểm tra.

**Quay về v1:** xem mục “Gỡ cập nhật” trong `CAP_NHAT_v2_KHTC.md`.
