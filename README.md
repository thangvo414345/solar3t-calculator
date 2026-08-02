# Bảng tính quy mô điện mặt trời & vay vốn ưu đãi — Quỹ BVMT Nghệ An

Công cụ tính nhanh, chạy hoàn toàn trên trình duyệt (không cần cài đặt, không cần server, không gửi dữ liệu đi đâu cả) dành cho đội kinh doanh **Solar 3T Nghệ An** khi tư vấn khách hàng lắp điện mặt trời áp mái và vay vốn ưu đãi từ Quỹ Bảo vệ môi trường Nghệ An.

**Demo:** mở trực tiếp file [`index.html`](./index.html) bằng trình duyệt, hoặc bật GitHub Pages cho repo này (Settings → Pages → Deploy from branch → `main` / `root`).

## Công cụ làm được gì

1. **Quy mô hệ thống điện mặt trời** — nhập một trong hai cách:
   - Theo ngân sách đầu tư dự kiến, hoặc
   - Theo hoá đơn tiền điện hàng tháng hiện tại của khách hàng

   Ra ngay: công suất hệ thống (kWp), số tấm pin cần lắp (mặc định tấm 620W), diện tích mái cần thiết (m²), tổng mức đầu tư, tiền điện tiết kiệm được mỗi tháng, và cơ cấu vốn vay 70% / vốn đối ứng 30% theo cơ chế Quỹ BVMT.

2. **Lịch trả nợ vay ưu đãi** — tính lịch trả gốc và lãi hàng tháng theo lãi suất 1,5%/năm (dự án năng lượng tái tạo) hoặc 2,6%/năm (dự án khác) theo Quyết định 02/QĐ-HĐQL ngày 09/02/2026 của Quỹ Bảo vệ môi trường Nghệ An, với 2 phương thức trả: dư nợ giảm dần hoặc trả đều hàng tháng (annuity).

3. **So sánh dòng tiền** — đối chiếu tiền điện tiết kiệm được mỗi tháng với số tiền phải trả nợ trung bình mỗi tháng, cho biết khách hàng dư ra hay còn thiếu.

4. **In / Lưu PDF** và **xuất CSV** lịch trả nợ để lưu hồ sơ hoặc gửi khách hàng.

## Giả định kỹ thuật & tài chính mặc định

Toàn bộ giả định đều có thể chỉnh sửa trực tiếp trên giao diện (mục "⚙ Tuỳ chỉnh giả định kỹ thuật"). Mặc định:

- Hệ thống tính cho loại **hoà lưới bám tải, không lưu trữ** (on-grid, không có pin lưu điện) — loại phổ biến nhất cho điện mặt trời áp mái dân dụng/thương mại tại Việt Nam. Hệ có lưu trữ (hybrid/off-grid) có suất đầu tư cao hơn đáng kể, cần báo giá riêng.
- Suất đầu tư và giá điện bình quân được tra cứu tự động theo quy mô đầu tư (quy mô càng lớn, suất đầu tư/kWp càng thấp nhờ lợi thế quy mô) — xem bảng chi tiết trong mục tuỳ chỉnh giả định trên giao diện.
- Tấm pin mặc định 620W, giá tham khảo 2.500.000 đ/tấm, diện tích ~2,6 m²/tấm, hệ số dự phòng diện tích lắp đặt 1,3 lần (khoảng cách, kết cấu đỡ, lối đi bảo trì).
- Sản lượng phát bình quân 1.450 kWh/kWp/năm (tham khảo bức xạ khu vực Nghệ An).
- Tỷ lệ điện dư được phép bán tối đa 50%, theo Nghị định 243/2026/NĐ-CP.

Các con số trên là **ước tính tham khảo tại thời điểm 8/2026**, dùng để tư vấn ban đầu. Trước khi chốt hợp đồng cần khảo sát kỹ thuật thực tế (bức xạ, kết cấu mái, phụ tải tiêu thụ) và lấy báo giá chính thức từ đối tác thi công, đồng thời xác nhận điều kiện vay cụ thể với Quỹ Bảo vệ môi trường Nghệ An.

## Lưu dữ liệu

Đây là công cụ tính toán tại chỗ (client-side) — **không lưu trữ dữ liệu** giữa các lần mở lại trang và không gửi bất kỳ thông tin nào lên máy chủ. Mỗi lần tải lại trang, các ô nhập sẽ về giá trị mặc định. Nếu cần lưu hồ sơ, dùng nút **"In / Lưu PDF"** hoặc **"Xuất CSV"** sau khi tính xong.

## Công nghệ

Một file HTML duy nhất — HTML, CSS thuần và JavaScript thuần (không framework, không build step, không phụ thuộc ngoài trừ Google Fonts). Mở bằng bất kỳ trình duyệt hiện đại nào.

## Đóng góp / chỉnh sửa

Toàn bộ logic tính toán nằm trong thẻ `<script>` ở cuối file `index.html`, bảng tra cứu giả định theo quy mô nằm trong hằng số `TIERS`. Sửa trực tiếp file và mở lại trình duyệt để xem thay đổi — không cần build.

## Liên hệ

**SOLAR 3T NGHỆ AN**
Nghi Phú, TP. Vinh, Nghệ An
ĐT: 0977 687 227

## Giấy phép

Phát hành theo giấy phép [MIT](./LICENSE) — có thể dùng, sửa, phân phối lại tự do, ghi rõ nguồn nếu cần.
