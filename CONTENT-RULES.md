# 05 — LUẬT NỘI DUNG (bắt buộc cho MỌI post từ 05/07/2026)

> Suong chốt sau khi duyệt bản nháp post 01. Vi phạm = viết lại. Áp dụng cho slide text, caption, mọi thứ hiển thị.

## R1. CẤM dấu gạch ngang
Không dùng `—`, `–`, `-` làm dấu câu trong bất kỳ text nào.
- Thay bằng: dấu phẩy, dấu chấm, dấu hai chấm, hoặc tách thành 2 câu.
- Khoảng số viết chữ: "0 tới 2", "dưới 3" (không viết "0-2").
- Dấu `·` (middle dot) trong kicker vẫn được phép (không phải gạch ngang).

## R2. Nguồn số liệu
- Nguồn phải nằm **dòng riêng**, **in nghiêng**, **màu xám** `#9AA3AE` (không cùng màu body).
- Trong recipe: dùng text element riêng `{type:"text", italic:true, color:"#9AA3AE", box:"none", scale:~0.62}` đặt dưới body, phía trên handle.
- Caption: nguồn để dòng cuối, trong ngoặc đơn.

## R3. Kiểm soát xuống dòng
- KHÔNG để canvas tự wrap. Mọi body phải bẻ dòng chủ động bằng `\n`.
- Mỗi dòng tối đa ~40 ký tự (body 40px, khổ 1080, margin 2 bên).
- Bẻ dòng theo cụm nghĩa, không bẻ giữa cụm từ.
- Body tối đa 4 dòng. Dài hơn thì cắt ý, không giảm cỡ chữ.

## R4. Giọng văn native
- Viết như người Việt nói chuyện với đồng nghiệp, không như bản dịch.
- Xưng "mình", gọi "bạn". Câu ngắn. Khẩu ngữ tự nhiên được khuyến khích
  ("xài", "giùm", "khỏi chờ", "nói thật").
- Cấm các cụm dịch máy: "phương án cuối cùng", "lợi thế cạnh tranh",
  "nền tảng để", "đẳng cấp", "tối ưu hóa trải nghiệm".
- Test: đọc to lên, nghe không giống lời nói thường ngày thì viết lại.

## R5. CTA cuối không sến
- Cấm kiểu "hành trình", "kim chỉ nam", "đồng hành cùng bạn", "soi lại mỗi tháng".
- CTA tốt = ngắn, tỉnh, tự tin. Nói thẳng lợi ích: follow thì được gì, nhịp đăng ra sao.
- Chuẩn tham chiếu: "Giờ tới lượt bạn. Save lại để lúc cần lôi ra xem."

## Checklist trước khi bàn giao (đi kèm checklist bản địa hóa ở 01-swipe-file.md)
- [ ] Zero dấu gạch ngang trong toàn bộ text
- [ ] Nguồn: dòng riêng, nghiêng, xám
- [ ] Mọi dòng body ≤ 40 ký tự, bẻ theo cụm nghĩa
- [ ] Đọc to không thấy giọng dịch
- [ ] Slide cuối không sến
