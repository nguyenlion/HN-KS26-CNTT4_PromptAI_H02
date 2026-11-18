# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 02
- **Họ tên:** Nguyễn Khắc Hiếu
- **Lớp:** CNTT4
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký gói tập ra JSON

**KET QUA AI**

```text
[
{
"ma_goi": "PT10",
"ngay_bat_dau": "2026-12-15",
"nguoi_lon": 2,
"hoc_sinh": 1,
"ca_tap": "toi",
"ghi_chu": null
},
{
"ma_goi": "YOG1",
"ngay_bat_dau": "2027-01-04",
"nguoi_lon": 3,
"hoc_sinh": 0,
"ca_tap": null,
"ghi_chu": "vừa mổ dây chằng gối"
},
{
"ma_goi": "GYM1",
"ngay_bat_dau": null,
"nguoi_lon": 4,
"hoc_sinh": 0,
"ca_tap": "sang",
"ghi_chu": "hen suyễn"
}
]
```

**Link trò chuyện:** https://gemini.google.com/app/90758b0c4517003a

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
**1. Tiền người lớn:**
Nhóm đăng ký gói YOG1 (900.000 đồng/người lớn) với số lượng 6 người lớn.
$6 \times 900.000 = 5.400.000$ (đồng)

**2. Tiền học sinh:**
Có 2 học sinh (14 tuổi và 16 tuổi, thuộc độ tuổi từ 12 đến 17 tuổi nên tính 70% giá người lớn) và 1 bé 8 tuổi (dưới 12 tuổi nên miễn phí).
$2 \times (900.000 \times 70\%) = 2 \times 630.000 = 1.260.000$ (đồng)

**3. Tiền gói tập:**
Tiền gói tập = Tiền người lớn + Tiền học sinh
$5.400.000 + 1.260.000 = 6.660.000$ (đồng)

**4. Giảm giá nhóm:**
Nhóm có 6 người lớn (từ 5 người lớn trở lên) nên được giảm 5% trên tiền gói tập.
Số tiền được giảm: $6.660.000 \times 5\% = 333.000$ (đồng)
Tiền gói tập sau giảm: $6.660.000 - 333.000 = 6.327.000$ (đồng)

**5. Phụ thu:**
Có 2 người lớn thuê tủ đồ riêng (150.000 đồng/người, không giảm giá).
$2 \times 150.000 = 300.000$ (đồng)

**6. Tổng tiền:**
Tổng tiền = Tiền gói tập sau giảm + Phụ thu
$6.327.000 + 300.000 = 6.627.000$ (đồng)

[RESULT: 6.627.000 đồng]
```

**Link trò chuyện:** https://gemini.google.com/app/e45a83a001c8ab8f

### b) Kiểm tra kết quả AI

AI trả lời đúng 

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "huy_lop",
  "so_khach": 2,
  "so_buoi_bi_huy": 3,
  "tom_tat": "Khách khiếu nại 3 buổi lớp Yoga ca tối bị huỷ không báo trước và yêu cầu giải quyết."
}
```

**Link trò chuyện:** https://gemini.google.com/app/a72a03e43d648138

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
Chào bạn, với tư cách là quản lý nhân sự, tôi đã tiến hành chấm điểm bài làm của nhân viên tư vấn tập sự dựa trên rubric và thông tin chuẩn của công ty. Bài làm có chứa các lỗi sai nghiêm trọng về giá, chính sách bảo lưu và giọng điệu chưa chuyên nghiệp.

Dưới đây là bảng đánh giá chi tiết:

| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin** (5.0 điểm) | 0.0 / 5.0 | - **Giá sai:** "Gói gym 1 tháng bên em có 500.000đ thôi"<br>

<br>- **Bảo lưu sai:** "Anh tập 10 ngày rồi bảo lưu thì vẫn bảo lưu hết nha anh" (Thực tế tập 10 ngày nằm trong khoảng từ ngày 8 đến ngày 15, chỉ được bảo lưu 50% số ngày còn lại). | - Giá đúng: 600.000 đồng/người lớn.<br>

<br>- Bảo lưu đúng: Theo chính sách, từ ngày 8 đến ngày 15 được bảo lưu 50% số ngày còn lại. |
| **Đầy đủ** (3.0 điểm) | 0.0 / 3.0 | - Nhân viên bỏ sót câu hỏi/thông tin của khách.<br>

<br>- Không mời khách cung cấp ngày bắt đầu và ca tập để đăng ký. | Cần bổ sung câu hỏi mời khách: "Anh vui lòng cung cấp ngày bắt đầu và ca tập mong muốn để em hỗ trợ đăng ký cho mình nhé ạ!" |
| **Giọng điệu** (2.0 điểm) | 1.0 / 2.0 | - Dùng từ ngữ suồng sã, thiếu chuyên nghiệp: "rẻ lắm luôn ạ", "nha anh", "ib em nhé!". | Thay bằng giọng điệu lịch sự, chuyên nghiệp hơn: "Dạ em chào anh ạ. Gói tập bên em..." và tránh dùng từ viết tắt "ib". |
| **Tổng điểm** | **1.0 / 10** |  |  |
```

**Link trò chuyện:** https://gemini.google.com/app/f767fa34d75ad69d
