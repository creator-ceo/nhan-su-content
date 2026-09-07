# nhan-su-content

**Vai Content trong đội nhân sự A.I** — của [Tô Hải Đoàn](https://www.facebook.com/tohaidoan/).

Một plugin Claude Code. Cài xong bạn có `/viet-content`: viết bài, đặt hook, ra ý tưởng, viết lại, tái sử dụng, kịch bản video ngắn/dài, mindmap — **chạy trên bộ não thứ 2 của chính bạn**, không phải của tôi.

> **Phiên bản:** `1.2.0` · 2026-09-07 · giấy phép MIT

---

## Cài

Hai lệnh, hai bước riêng — thêm kho trước, cài plugin sau:

```bash
claude plugin marketplace add creator-ceo/nhan-su-content
```

```bash
claude plugin install content
```

Xong thì gõ `/` sẽ thấy `/viet-content`.

---

## ⚠️ Cần cái nền chạy trước

Vai này **đọc** bộ não thứ 2 của bạn, nó không tự dựng ra bộ não đó. Nền là bộ khung riêng:

```bash
git clone https://github.com/creator-ceo/nhan-su-thu-thu.git
```

Mở Claude Code trong thư mục vừa clone, nhắn `bắt đầu`, trả lời phỏng vấn — bạn có `wiki/` với giọng văn, kho chuyện, chân dung khách của bạn. Nền cũng giữ `/nap-kho`, **đường ghi duy nhất** vào bộ não.

### Lần chạy đầu: vai này tự dựng kho của nó

Nền **cố ý không tạo sẵn** `voice-profile`, `hook-library`, `models/`… kể cả dưới dạng file rỗng — vì nó không dựng nổi chúng, và một vỏ rỗng thì vai này vẫn phải mở ra đọc mới biết bên trong có gì. Nên việc dựng thuộc về đây.

Lượt đầu sau khi cài, nó hỏi bạn và dựng **10 kho**, chia hai tầng:

| Tầng | Kho | Nhịp |
|---|---|---|
| **Nền của vai** | `voice-profile` *(rút từ 5–10 bài bạn đã đăng thật)* · `video-production-setup` | làm **một lần**, dùng mãi |
| **Kho biến thiên** | `experiences-library` · `customer-wins` · `quoted-authority` · `models/` · `hook-library` · `content-library` · `audience-insights` · `so-lieu-chuan` | nạp thêm **mãi mãi** |

⏱ Tầng 1 mất khoảng **20–30 phút** nếu bạn có sẵn bài cũ. Chưa muốn làm thì bỏ qua được — vai vẫn chạy, chỉ là chạy ở mức cảnh báo *(xem dưới)*.

⚡ **Nó chỉ dựng trang nào CÓ CHẤT LIỆU THẬT, không dựng cho đủ bộ.** Không có lời chứng thực nào thì `customer-wins` chưa tồn tại — chứ không phải tồn tại mà rỗng. Trang rỗng làm cửa vào đếm nhầm là *"đã có"*, rồi bài ra nhạt mà không có cảnh báo nào.

### Chưa dựng kho thì sao?

Vẫn chạy, và đây là chỗ dễ hiểu nhầm nhất. Cửa vào đếm bốn file nền rồi hành xử theo ba mức:

| Kho có gì | Vai làm gì |
|---|---|
| **0 file** | không viết. Hỏi đúng ba câu để dựng tối thiểu, rồi mới viết |
| **1–3 file** | viết, nhưng **nói trước là thiếu gì và vì thế bài sẽ yếu ở đâu** |
| **đủ 4 file** | chạy thẳng |

Nó không im lặng viết một bài trơn tru bằng trí nhớ chung chung rồi để bạn tưởng đó là giọng mình.

---

## Trong này có gì, và không có gì

| Đi kèm plugin — **luật nghề** | Nằm trong `wiki/` của bạn — **chất liệu** |
|---|---|
| Quy trình 7 bước | Giọng văn của bạn (`voice-profile.md`) |
| 10 luật lõi nghề + 7 khung viết | Câu chuyện thật (`experiences-library.md`) |
| 8 kiểu hook, kèm cách chấm | Chân dung khách (`target-customer.md`) |
| 4 tầng dấu hiệu văn AI | Quan điểm ngược dòng (`contrarian-beliefs.md`) |
| Khuôn kịch bản video ngắn + dài | Hình mẫu bạn đang học (`models/`) |
| Khuôn mindmap từ một trang bộ não | Kết quả khách, lời chứng thực (`customer-wins.md`) |
| Ba kiểu dùng sai con số, xếp theo độ khó bắt | Con số thành tích thật của bạn (`so-lieu-chuan.md`) |
| **10 khuôn kho** (`khuon/`) — cấu trúc từng trang | Nội dung thật trong 10 kho đó |

**Vì sao tách:** luật nghề thì ai viết cũng dùng chung nên nó đi theo plugin. Giọng và chuyện là **của riêng bạn** và bạn sẽ sửa liên tục — chép chúng vào plugin là có hai bản, rồi bản trong plugin âm thầm lạc hậu.

🚫 **Skill này không dạy bạn viết giọng Tô Hải Đoàn.** Nó dạy *nghề*. Giọng lấy từ `wiki/voice-profile.md` của bạn.

🚫 **Skill này không tự ghi vào `wiki/`.** Bộ não chỉ có một đường ghi là `/nap-kho`. Trong lúc viết mà bật ra thứ đáng lưu, nó **đề xuất** nạp chứ không tự sửa file.

---

## Vai này nằm ở đâu trong đội

Sáu vai nhân sự A.I. Đây là vai thứ ba, và là vai đầu tiên được đóng gói rời:

| Vai | Kho | Trạng thái |
|---|---|---|
| 🧑‍🏫 **Thủ thư** — cái nền, cài trước tiên | `creator-ceo/nhan-su-thu-thu` | ✅ |
| ✍️ **Content** | `creator-ceo/nhan-su-content` | ✅ **kho này** |
| 🎛️ Điều phối · 💰 Bán hàng | `nhan-su-dieu-phoi` · `nhan-su-ban-hang` | 🟡 đang đóng gói |
| 🎨 Thiết kế · 🤝 Chăm sóc · 🔍 Nghiên cứu | — | ⬜ chưa |

Có `/tong-giam-doc` (nằm trong nền) thì nó tự giao việc viết xuống vai này. Không có cũng không sao — gõ thẳng `/viet-content`, vai này đứng một mình đủ.

---

## Cập nhật

```bash
claude plugin update content
```

Luật nghề trong plugin bị ghi đè bằng bản mới; `wiki/` của bạn nằm ở thư mục khác nên **không bị đụng tới**. Đó là lý do hai thứ ở hai kho.

---

## Ai làm cái này

**Tô Hải Đoàn** — người làm nội dung và xây thương hiệu cá nhân tại Việt Nam. Đây không phải skill dựng cho vui: nó là quy trình tôi dùng cho công việc của chính mình mỗi ngày, đóng gói lại để bạn chạy được trên dữ liệu của bạn.

**Kẹt ở đâu, hoặc muốn được hướng dẫn dùng cho đúng việc của bạn** thì nhắn tôi: **[facebook.com/tohaidoan](https://www.facebook.com/tohaidoan/)**

Dùng thấy chỗ nào tắc, luật nào sai với ngành của bạn — báo lại. Bộ này lớn lên bằng đúng cách đó.
