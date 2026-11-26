# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 05
- **Họ tên:** Trần Thị Diễm Trâm
- **Lớp:**
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé xem phim ra JSON

**KET QUA AI**

```text
```json
[
  {
    "loai_ve": "P2D",
    "ngay_chieu": "2026-12-24",
    "ve_nguoi_lon": 2,
    "ve_tre_em": 1,
    "loai_ghe": "thuong",
    "ghi_chu": null
  },
  {
    "loai_ve": "P3D",
    "ngay_chieu": "2027-01-01",
    "ve_nguoi_lon": 3,
    "ve_tre_em": 0,
    "loai_ghe": null,
    "ghi_chu": "Một người hay chóng mặt, cần ngồi gần lối ra"
  },
  {
    "loai_ve": "GOLD",
    "ngay_chieu": null,
    "ve_nguoi_lon": 4,
    "ve_tre_em": 0,
    "loai_ghe": "doi",
    "ghi_chu": "Một bạn đi xe lăn"
  }
]

```

https://share.gemini.google/a9Uu6XfxMKzl
``` 
## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
**Bước 1: Tiền vé người lớn**

* Giá vé phim 3D (P3D) người lớn: $130.000\text{ đồng/vé}$
* Số lượng người lớn: $5\text{ người}$
* Phép tính: $5 \times 130.000 = 650.000\text{ đồng}$

**Bước 2: Tiền vé trẻ em**

* 2 trẻ em cao $1,1\text{ m}$ và $1,25\text{ m}$ (nằm trong khoảng từ $1\text{ m}$ đến $1,3\text{ m}$) tính $70\%$ giá vé người lớn:
* Giá 1 vé trẻ em: $130.000 \times 70\% = 91.000\text{ đồng}$
* Tiền vé 2 trẻ em: $2 \times 91.000 = 182.000\text{ đồng}$


* 1 bé cao $0,9\text{ m}$ (dưới $1\text{ m}$) ngồi cùng người lớn được miễn phí ($0\text{ đồng}$).
* Tổng tiền vé trẻ em: $182.000 + 0 = 182.000\text{ đồng}$

**Bước 3: Tiền vé**

* Tiền vé = tiền vé người lớn + tiền vé trẻ em
* Phép tính: $650.000 + 182.000 = 832.000\text{ đồng}$

**Bước 4: Giảm giá nhóm**

* Nhóm có $5\text{ người lớn}$ (đủ điều kiện từ $5\text{ người lớn}$ trở lên) nên được giảm $10\%$ trên tiền vé.
* Số tiền được giảm: $832.000 \times 10\% = 83.200\text{ đồng}$
* Tiền vé sau giảm: $832.000 - 83.200 = 748.800\text{ đồng}$

**Bước 5: Tiền combo**

* Giá combo bắp nước: $75.000\text{ đồng/combo}$
* Số lượng combo: $3\text{ combo}$
* Phép tính: $3 \times 75.000 = 225.000\text{ đồng}$

**Bước 6: Tổng tiền**

* Tổng tiền = tiền vé sau giảm + tiền combo
* Phép tính: $748.800 + 225.000 = 973.800\text{ đồng}$

[RESULT: 973.800 đồng]
```

**Link trò chuyện:**
https://share.gemini.google/A1VKABGUed5B

### b) Kiểm tra kết quả AI

kết quả của AI là đúng.

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loi_su_co": "loi_ky_thuat",
  "so_khach": 4,
  "so_suat_bi_loi": 2,
  "tom_tat": "Tối 02/11/2026, gia đình 4 người xem 2 suất phim liên tiếp tại phòng 3 đều bị mất tiếng giữa phim hơn 15 phút; không phàn nàn về nhân viên và đề nghị rạp giải quyết thỏa đáng."
}
```

**Link trò chuyện:**
https://share.gemini.google/EQ0ANzkR7R0U
## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh Chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50% - tối đa 5.0đ)** | 0.0 / 5.0 | - **Câu bị lỗi:** "Vé 2D bên em có 80k thôi nè"<br>

<br>- **Lý do sai:** Sai giá vé chuẩn (giá chuẩn là 90.000 đồng/vé người lớn).<br>

<br>- **Câu bị lỗi:** "Anh huỷ trước 2 tiếng vẫn được hoàn 50% nha anh."<br>

<br>- **Lý do sai:** Sai chính sách huỷ vé (huỷ trước giờ chiếu dưới 3 tiếng sẽ không được hoàn tiền). | "Giá vé phim 2D hiện tại là 90.000 đồng/vé người lớn. Về chính sách huỷ vé, trường hợp huỷ trước giờ chiếu dưới 3 tiếng sẽ không được hoàn tiền ạ." |
| **Đầy đủ (30% - tối đa 3.0đ)** | 1.5 / 3.0 | - **Đạt:** Đã đề cập đến cả 2 ý hỏi của khách (giá vé và việc hoàn tiền khi huỷ vé).<br>

<br>- **Câu bị lỗi (thiếu ý):** "Cần gì nhắn em nha!"<br>

<br>- **Lý do sai:** Thiếu lời mời khách cung cấp ngày, suất chiếu và số lượng vé để hỗ trợ đặt chỗ. | "Nếu anh có nhu cầu đặt vé, vui lòng cung cấp giúp em thông tin về ngày xem, suất chiếu và số lượng vé để em hỗ trợ đặt chỗ cho mình ạ." |
| **Giọng điệu (20% - tối đa 2.0đ)** | 0.0 / 2.0 | - **Câu bị lỗi:** "Hi anh! Vé 2D bên em có 80k thôi nè, rẻ xỉu.", "nha anh", "Cần gì nhắn em nha!"<br>

<br>- **Lý do sai:** Dùng từ ngữ suồng sã, thiếu chuyên nghiệp ("Hi", "thôi nè", "rẻ xỉu", "nha", "nhắn em nha"). | "Dạ chào anh! Em xin phép gửi đến anh thông tin giá vé và chính sách huỷ vé của bên em ạ... Anh cần hỗ trợ thêm thông tin gì xin vui lòng phản hồi để em tư vấn cho mình nhé." |
| **TỔNG ĐIỂM** | **1.5 / 10** |  |  |
```

**Link trò chuyện:**
https://share.gemini.google/TAZdS86032ds