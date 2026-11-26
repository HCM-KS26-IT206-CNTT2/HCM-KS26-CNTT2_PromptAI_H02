# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 09
- **Họ tên:** Đoàn Nguyễn Minh Tâm
- **Lớp:** HCM-KS26-CNTT2
- **Link repository Pha2:** https://github.com/HCM-KS26-IT206-CNTT2/HCM-KS26-CNTT2_PromptAI_H02.git
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** ChatGPT

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt chỗ workshop ra JSON

**KET QUA AI**

```text
[
  {
    "ma_lop": "NANTAY",
    "ngay_hoc": "2026-12-13",
    "nguoi_lon": 2,
    "tre_em": 1,
    "ca_hoc": "chieu",
    "ghi_chu": null
  },
  {
    "ma_lop": "BANXOAY",
    "ngay_hoc": "2027-01-10",
    "nguoi_lon": 3,
    "tre_em": 0,
    "ca_hoc": null,
    "ghi_chu": "1 người bị đau cổ tay"
  },
  {
    "ma_lop": "VEGOM",
    "ngay_hoc": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "ca_hoc": "sang",
    "ghi_chu": "1 bạn đi xe lăn"
  }
]
```

**Link trò chuyện:** https://chatgpt.com/share/6b07e31a-b804-83ec-90d5-7c978606e67c

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
Bảng báo giá lớp BANXOAY – Đất Việt Workshop

1. Tính tiền người lớn
- Số lượng: 5 người.
- Giá lớp BANXOAY: 550.000 đồng/người.
Tiền người lớn:

\(5 \times 550.000 = 2.750.000\) đồng.

2. Tính tiền trẻ em
- Trẻ em 8 tuổi: 70% × 550.000 = 385.000 đồng.
- Trẻ em 12 tuổi: 70% × 550.000 = 385.000 đồng.
- Bé 4 tuổi: Miễn phí vì dưới 6 tuổi và không làm sản phẩm.
Tiền trẻ em:

\(385.000 + 385.000 = 770.000\) đồng.

3. Tính tiền học

Tiền học = Tiền người lớn + Tiền trẻ em

\(2.750.000 + 770.000 = 3.520.000\) đồng.

4. Tính tiền sau khi giảm giá nhóm

Nhóm có 5 người lớn nên được giảm 5%.

- Tiền giảm giá:

\(3.520.000 \times 5\% = 176.000\) đồng.

- Tiền học sau giảm:

\(3.520.000 - 176.000 = 3.344.000\) đồng.

5. Tính phí nung và giao sản phẩm
- Số sản phẩm: 4.
- Phí nung và giao: 80.000 đồng/sản phẩm.
Phí nung và giao:

\(4 \times 80.000 = 320.000\) đồng.

6. Tính tổng tiền

Tổng tiền = Tiền học sau giảm + Phí nung và giao

\(3.344.000 + 320.000 = 3.664.000\) đồng.

TỔNG BÁO GIÁ
3.664.000 đồng
Đã bao gồm tiền học sau giảm giá và phí nung, giao 4 sản phẩm.

[RESULT: 3.664.000 đồng]
```

**Link trò chuyện:** https://chatgpt.com/share/6b07e3aa-12a8-83ec-8918-477e25d4364e

### b) Kiểm tra kết quả AI

(Ghi kết luận AI đúng hay sai; nếu sai, ghi bước sai đầu tiên và kết quả đúng của bước đó – xoá dòng này)

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "hong_san_pham",
  "so_khach": 3,
  "so_san_pham_bi_hong": 5,
  "tom_tat": "Gia đình 3 người nhận 5 sản phẩm bị nứt vỡ, đề nghị xưởng giải quyết thỏa đáng."
}
```

**Link trò chuyện:** https://chatgpt.com/share/6b07e3eb-3244-83ec-9ff2-d1a32758b5ef

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí             | Điểm       | Minh chứng                                                                                                                                                                                                                                                               | Đề xuất sửa                                                                                                                                |
| -------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Đúng thông tin (50%) | 2/5        | - Câu bị lỗi: “Lớp vẽ gốm bên em 200k thôi nè” → Sai giá, giá chuẩn là 250.000 đồng/người lớn.<br>- Câu bị lỗi: “Chị đổi trước 1 ngày thì free nha chị.” → Sai chính sách. Đổi trước 1 ngày (24 giờ) thuộc khoảng từ 12 đến dưới 48 giờ, phải trả phí 30.000 đồng/người. | “Lớp vẽ gốm có giá 250.000 đồng/người lớn. Nếu chị đổi lịch trước 1 ngày, phí đổi lịch là 30.000 đồng/người.”                              |
| Đầy đủ (30%)         | 1/3        | - Đã trả lời cả hai câu hỏi về giá và phí đổi lịch.<br>- Chưa mời khách cung cấp ngày học, ca học và số người để đặt chỗ.                                                                                                                                                | “Chị vui lòng cung cấp ngày học, ca học và số lượng người tham gia để bên em hỗ trợ đặt chỗ nhé!”                                          |
| Giọng điệu (20%)     | 0.5/2      | - Câu bị lỗi: “Hi chị ơi!” → Cách chào chưa chuyên nghiệp.<br>- Câu bị lỗi: “200k thôi nè, vui lắm luôn.” → Ngôn ngữ quảng cáo, suồng sã.<br>- Câu bị lỗi: “Có gì chị nhắn em nha!” → Cách diễn đạt thiếu tính chuyên nghiệp.                                            | Sử dụng cách xưng hô lịch sự, chuyên nghiệp như “Dạ, em xin gửi chị thông tin về lớp vẽ gốm...” và “Rất mong nhận được phản hồi từ chị ạ.” |
| **Tổng điểm**        | **3.5/10** | **Bài làm sai giá, sai chính sách đổi lịch và chưa có lời mời cung cấp thông tin đặt chỗ.**                                                                                                                                                                              | **Cần chú ý đối chiếu thông tin chuẩn và sử dụng ngôn ngữ chuyên nghiệp hơn.**                                                             |
```

**Link trò chuyện:** https://chatgpt.com/share/6b07e495-9864-83ec-af6b-33117c761760
