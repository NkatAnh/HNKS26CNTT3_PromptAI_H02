# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 08
- **Họ tên:** Phạm Nhật Anh
- **Lớp:** HNKS26CNTT3
- **Link repository Pha2:** https://github.com/NkatAnh/HNKS26CNTT3_PromptAI_H02.git
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt lịch khám ra JSON

**KET QUA AI**

```text
[
  {
    "ma_dich_vu": "TRAM",
    "ngay_hen": "2026-12-17",
    "nguoi_lon": 2,
    "tre_em": 1,
    "khung_gio": "chieu",
    "ghi_chu": null
  },
  {
    "ma_dich_vu": "CAOVOI",
    "ngay_hen": "2027-01-06",
    "nguoi_lon": 3,
    "tre_em": 0,
    "khung_gio": null,
    "ghi_chu": "1 người bị tiểu đường"
  },
  {
    "ma_dich_vu": "TAYTRANG",
    "ngay_hen": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "khung_gio": "sang",
    "ghi_chu": "1 người dị ứng thuốc tê"
  }
]
```

**Link trò chuyện:** https://share.gemini.google/KxdJLuWtOMkh

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text

===
**BẢNG GIÁ DỊCH VỤ (đồng/người lớn)**

* CAOVOI – Khám và cạo vôi răng: 350.000
* TRAM – Trám răng thẩm mỹ (1 răng): 500.000
* TAYTRANG – Tẩy trắng răng: 2.500.000

**QUY TẮC TÍNH GIÁ**

1. Trẻ em từ 6 đến 12 tuổi tính 80% giá người lớn. Trẻ dưới 6 tuổi được khám miễn phí.
2. Nhóm từ 5 người lớn trở lên được giảm 10% trên tiền dịch vụ (tiền người lớn + tiền trẻ em).
3. Phí chụp X-quang: 150.000 đồng/phim. Phí này không được giảm giá.
4. Tổng tiền = tiền dịch vụ sau giảm + phí chụp X-quang.

# **YÊU CẦU BÁO GIÁ**
Nhóm nhân viên công ty làm dịch vụ CAOVOI gồm 6 người lớn, 2 trẻ em (7 tuổi và 11 tuổi) và 1 bé 4 tuổi. Có 3 người cần chụp X-quang (mỗi người 1 phim).

1. **Tiền người lớn:** Nhóm có 6 người lớn sử dụng dịch vụ CAOVOI (350.000 đồng/người).
Phép tính: $6 \times 350.000 = 2.100.000$ đồng.
2. **Tiền trẻ em:** Có 2 trẻ em trong độ tuổi từ 6 đến 12 (7 tuổi và 11 tuổi) được tính 80% giá người lớn; 1 bé 4 tuổi (dưới 6 tuổi) được miễn phí.
Phép tính: $2 \times (350.000 \times 80\%) + 1 \times 0 = 2 \times 280.000 = 560.000$ đồng.
3. **Tiền dịch vụ:** Tổng chi phí dịch vụ CAOVOI của người lớn và trẻ em.
Phép tính: $2.100.000 + 560.000 = 2.660.000$ đồng.
4. **Giảm giá nhóm:** Nhóm có 6 người lớn (từ 5 người lớn trở lên) nên được giảm 10% trên tổng tiền dịch vụ.
Phép tính giảm giá: $2.660.000 \times 10\% = 266.000$ đồng.
Tiền dịch vụ sau giảm: $2.660.000 - 266.000 = 2.394.000$ đồng.
5. **Phí X-quang:** Có 3 người chụp X-quang, mỗi người 1 phim với giá 150.000 đồng/phim (không áp dụng giảm giá).
Phép tính: $3 \times 150.000 = 450.000$ đồng.
6. **Tổng tiền:** Cộng tiền dịch vụ sau giảm và phí chụp X-quang.
Phép tính: $2.394.000 + 450.000 = 2.844.000$ đồng.

[RESULT: 2.844.000 đồng]
```

**Link trò chuyện:** https://share.gemini.google/9QcrsapMUR8v

### b) Kiểm tra kết quả AI

AI tính đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "tre_hen",
  "so_khach": 3,
  "so_lan_hen_bi_tre": 2,
  "tom_tat": "Gia đình 3 khách phải chờ hơn 1 tiếng trong 2 lần hẹn cạo vôi răng."
}
```

**Link trò chuyện:** https://share.gemini.google/kQkcYKKlEh4o

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 0 / 5.0 | - **Câu bị lỗi:** `"Trám răng bên em 450k/răng thôi"`<br>

<br>- **Lý do sai:** Báo sai giá niêm yết của công ty (500.000 đồng/răng).<br>

<br>

<br>- **Câu bị lỗi:** `"Bong sau 8 tháng thì em làm lại free cho anh nha."`<br>

<br>- **Lý do sai:** Sai chính sách bảo hành. Tháng thứ 8 nằm trong khoảng từ tháng 7 đến tháng 12 nên chỉ được giảm 50%, không phải miễn phí. | - **Sửa giá:** "Dịch vụ trám răng thẩm mỹ bên em có giá 500.000 đồng/răng ạ."<br>

<br>

<br>- **Sửa bảo hành:** "Nếu miếng trám bị bong sau 8 tháng, bên em sẽ hỗ trợ làm lại với mức giảm giá 50% theo chính sách bảo hành từ tháng thứ 7 đến tháng thứ 12 ạ." |
| **Đầy đủ (30%)** | 2.0 / 3.0 | - Đã trả lời đủ 2 ý hỏi của khách (về giá và chính sách khi bong sau 8 tháng).<br>

<br>- **Lỗi thiếu ý (bị động):** `"Cần gì cứ inbox em ạ!"`<br>

<br>- **Lý do sai:** Thiếu lời mời khách cung cấp ngày hẹn và khung giờ cụ thể để đặt lịch. | "Anh vui lòng cho em xin thông tin về ngày hẹn và khung giờ thuận tiện để em hỗ trợ đặt lịch thăm khám cho mình nhé ạ." |
| **Giọng điệu (20%)** | 1.0 / 2.0 | - **Câu bị lỗi:** `"450k/răng thôi, đẹp như răng thật luôn. Bong sau 8 tháng thì em làm lại free cho anh nha. Cần gì cứ inbox em ạ!"`<br>

<br>- **Lý do sai:** Sử dụng nhiều từ ngữ suồng sã, thiếu tính chuyên nghiệp trong tư vấn dịch vụ y tế/nha khoa ("450k", "thôi", "luôn", "free", "nha", "inbox"). | "Dạ chào anh! Dịch vụ trám răng thẩm mỹ bên em có giá 500.000 đồng/răng, đảm bảo tính thẩm mỹ tự nhiên như răng thật. Trường hợp miếng trám bị bong sau 8 tháng, bên em áp dụng chính sách bảo hành giảm 50% chi phí làm lại ạ. Anh vui lòng cho em biết ngày hẹn và khung giờ phù hợp để em đặt lịch cho mình nhé!" |
| **TỔNG ĐIỂM** | **3.0 / 10** |  |  |
```

**Link trò chuyện:** https://share.gemini.google/Tt0iwXu47KKC
