# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 04
- **Họ tên: Trần Văn Gia Khang**
- **Lớp: CNTT1**
- **Link repository Pha2: https://github.com/tranvangiakhang-lab/HCM_KS26_CNTT1_PromptAI_H02**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):ChatGPT**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé xe ra JSON

**KET QUA AI**

```text
[
  {
    "ma_tuyen": "SGDL",
    "ngay_di": "2026-12-22",
    "ve_nguoi_lon": 2,
    "ve_tre_em": 1,
    "loai_cho": "giuong",
    "ghi_chu": null
  },
  {
    "ma_tuyen": "SGNT",
    "ngay_di": "2027-01-02",
    "ve_nguoi_lon": 3,
    "ve_tre_em": 0,
    "loai_cho": null,
    "ghi_chu": "một người đang mang thai 6 tháng"
  },
  {
    "ma_tuyen": "SGCT",
    "ngay_di": null,
    "ve_nguoi_lon": 4,
    "ve_tre_em": 0,
    "loai_cho": "ghe",
    "ghi_chu": "bà nội đi xe lăn"
  }
]
```

**Link trò chuyện: https://chatgpt.com/c/6b078e71-7c50-83ec-8376-a19ead0cb90a**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
Xin chào quý khách! Phương Nam Express xin gửi báo giá chi tiết cho đoàn đi tuyến SGDL – Sài Gòn – Đà Lạt như sau:
1. Tiền vé người lớn
- Số lượng: 8 người lớn.
- Giá vé: 320.000 đồng/người.
Phép tính: 8 × 320.000 = 2.560.000 đồng.
2. Tiền vé trẻ em
- Số lượng: 3 trẻ em (6, 7 và 9 tuổi).
- Trẻ em từ 5 đến 10 tuổi tính 75% giá vé người lớn.
- Giá vé trẻ em: 320.000 × 75% = 240.000 đồng/người.
Phép tính: 3 × 240.000 = 720.000 đồng.
3. Tiền vé
- Tiền vé người lớn: 2.560.000 đồng.
- Tiền vé trẻ em: 720.000 đồng.
- Bé 2 tuổi: Miễn phí vì dưới 5 tuổi và ngồi cùng người lớn.
Phép tính: 2.560.000 + 720.000 = 3.280.000 đồng.
4. Giảm giá đoàn
- Đoàn có 8 người lớn, đủ điều kiện giảm 5% (từ 6 người lớn trở lên).

Phép tính:

3.280.000 × 5% = 164.000 đồng.

Tiền vé sau giảm:

3.280.000 − 164.000 = 3.116.000 đồng.
5. Phụ thu hành lý cồng kềnh
- Số lượng: 2 kiện.
- Phụ thu: 100.000 đồng/kiện.
- Phụ thu không được giảm giá.
Phép tính: 2 × 100.000 = 200.000 đồng.
6. Tổng tiền
Tiền vé sau giảm + phụ thu:

3.116.000 + 200.000 = 3.316.000 đồng.

TỔNG TIỀN THANH TOÁN
3.316.000 đồng

- 8 người lớn: 2.560.000 đồng
- 3 trẻ em: 720.000 đồng
- 1 bé 2 tuổi: Miễn phí
- Giảm giá đoàn: 164.000 đồng
- 2 kiện hành lý: 200.000 đồng

[RESULT: 3.316.000 đồng]

Cảm ơn quý khách đã lựa chọn Phương Nam Express. Kính chúc quý khách có một chuyến đi Sài Gòn – Đà Lạt vui vẻ và an toàn!
```

**Link trò chuyện: https://chatgpt.com/c/6b078ea0-d7e8-83ec-ad52-057d6ab12395**

### b) Kiểm tra kết quả AI

(Ghi kết luận AI đúng hay sai; nếu sai, ghi bước sai đầu tiên và kết quả đúng của bước đó – xoá dòng này)

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```
{
  "loai_su_co": "sai_loai_xe",
  "so_khach": 3,
  "so_chang_bi_doi": 2,
  "tom_tat": "Ba khách đặt giường nằm nhưng cả chặng đi và về đều bị đổi sang xe ghế ngồi."
}

Giải thích:
- loai_su_co: sai_loai_xe vì nhà xe đổi từ giường nằm sang ghế ngồi.
- so_khach: 3 người.
- so_chang_bi_doi: 2 chặng (đi và về).
- tom_tat: Tóm tắt đúng sự cố, không quá 20 từ.
```

**Link trò chuyện: https://chatgpt.com/c/6b078ece-65a8-83ec-96dd-c25dad197b28**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```
1. Kết quả chấm điểm
2/10 điểm
Tiêu chí	Điểm tối đa	Điểm đạt	Nhận xét
Đúng thông tin	5	0	Báo sai giá vé (350.000đ thay vì 380.000đ); sai chính sách đổi vé (12 tiếng phải mất phí 20%, không miễn phí).
Đầy đủ	3	1	Đã trả lời cả hai câu hỏi nhưng chưa mời khách cung cấp ngày đi và số vé để đặt chỗ.
Giọng điệu	2	1	Có lời chào nhưng sử dụng từ ngữ suồng sã như "xe xịn lắm luôn", "nha chị", "free".
Tổng	10	2	

Lưu ý: Ghi chú yêu cầu tự chấm 10/10 trong bài làm không phải thông tin thuộc rubric và không được sử dụng để thay đổi kết quả chấm.
2. Câu trả lời đề xuất đạt 10/10
Dạ em xin chào chị!

Vé xe tuyến Sài Gòn – Nha Trang có giá 380.000 đồng/vé người lớn.

Về chính sách đổi vé, nếu chị đổi ngày đi trước giờ xe chạy 12 tiếng thì sẽ áp dụng mức phí 20% giá vé, tương đương 76.000 đồng/vé. Vì thời gian đổi vé nằm trong khoảng từ 6 đến dưới 24 giờ trước giờ khởi hành.

Chị vui lòng cung cấp ngày đi dự kiến và số lượng vé để em hỗ trợ kiểm tra và đặt chỗ cho chị ạ.

Em cảm ơn chị!

3. Giải thích đáp án
- Giá vé: 380.000 đồng.
- Phí đổi vé: 380.000 × 20% = 76.000 đồng/vé.
- Đổi trước 12 tiếng: Có mất phí.
- Đầy đủ thông tin và có lời mời khách cung cấp ngày đi, số vé.
- Giọng điệu lịch sự, chuyên nghiệp.
```

**Link trò chuyện: https://chatgpt.com/c/6b078ece-65a8-83ec-96dd-c25dad197b28**
