# 8.2 — Hệ thống cách chơi và cơ chế

> **Trạng thái:** Bản làm việc / Hướng đã chọn  
> **Mục đích:** Xác định các hệ thống cách chơi cụ thể cần có để thể hiện 5 trụ cách chơi đã thiết lập ở 8.1.

## 8.2.1 Kiến trúc hệ thống

### Hệ thống cách chơi lõi

1. Hệ thống khám phá
2. Hệ thống quan sát và điều tra
3. Hệ thống tương tác và lựa chọn
4. Hệ thống trạng thái thế giới
5. Hệ thống ký ức và mâu thuẫn
6. Hệ thống hệ quả và lưu giữ

### Hệ thống hỗ trợ

7. Hội thoại và hiểu biết nhân vật
8. Bằng chứng / Khám phá
9. Bạn đồng hành / Thú cưng
10. Tiến trình và theo dõi hiểu biết
11. Quản lý hoạt động / phiên chơi
12. Phản hồi và chỉ dẫn

## 8.2.2 Hệ thống lõi 01 — Khám phá

**Mục đích:** Di chuyển tự do và khám phá không gian.

Khám phá nên tạo ra cảm giác:

> “Tôi đến đây vì tò mò.”

### Đầu vào

- Di chuyển
- Máy quay
- Dẫn đường
- Vào / rời địa điểm
- Quay lại địa điểm

### Đầu ra

- Địa điểm mới
- Vật thể
- NPC
- Manh mối môi trường
- Tương tác mới
- Câu hỏi mới

### Quy tắc

Đừng rút khám phá còn:

> Điểm dẫn → Dấu → Vật phẩm → Quay về

Dấu đánh dấu có thể tồn tại để cho rõ ràng, nhưng **sự tò mò vẫn là chính**.

## 8.2.3 Hệ thống lõi 02 — Quan sát và điều tra

Hệ thống này biến:

> “Tôi nhìn thấy”

thành:

> “Tôi nhận ra.”

### Hành động

- Quan sát vật thể
- Kiểm tra
- Đọc dấu vết
- Xem môi trường
- Lắng nghe NPC
- So sánh thông tin
- Phát hiện bất thường
- Kết nối bằng chứng
- Hiểu lại bằng chứng

### Phân biệt

**Quan sát:** “Tôi thấy cái gì?”

**Điều tra:** “Điều này có nghĩa gì?”

### Trạng thái điều tra

```
Đã quan sát
   ↓
Đã nhận ra
   ↓
Đã đặt câu hỏi
   ↓
Đã diễn giải
   ↓
Đã kết nối
   ↓
Đã hiểu lại
```

Không phải mọi khám phá đều cần đi qua mọi giai đoạn.

## 8.2.4 Hệ thống lõi 03 — Tương tác và lựa chọn

Hệ thống này nối:

> **Ý định người chơi → Trạng thái thế giới**

### Hành động

- Nói chuyện
- Giúp
- Sửa chữa
- Đưa
- Lấy
- Điều tra
- Từ chối
- Lựa chọn
- Quay lại
- Thay đổi vật thể / môi trường

### Quy tắc

Tương tác không nên chỉ là:

> Dùng vật thể → Phần thưởng

Thay vào đó, thường nên là:

> Tương tác → Trạng thái thế giới thay đổi

## 8.2.5 Hệ thống lựa chọn

Các lựa chọn **không chủ yếu là đạo đức Thiện / Ác**.

Các lựa chọn tạo ra những ký ức khác nhau.

Ví dụ:

- **A — Giúp:** NPC nhớ rằng người chơi đã giúp.
- **B — Từ chối:** NPC nhớ rằng người chơi đã bỏ đi.
- **C — Giải pháp khác:** Một trạng thái thế giới và một ký ức khác được tạo ra.

Vì vậy:

> **Lựa chọn là một đầu vào của trạng thái thế giới.**

## 8.2.6 Hệ thống lõi 04 — Trạng thái thế giới

Trạng thái thế giới là nền tảng cho sự lưu giữ có ý nghĩa.

Ví dụ:

- Cầu: gãy → đã sửa
- NPC: nghi ngờ → tin cậy
- Nhà: khóa → có lối vào
- Vật thể: mất → đã trả lại
- Ký ức: chưa biết → đã hình thành

### Trạng thái nhiều giai đoạn

Từ vựng trạng thái có thể dùng:

- UNKNOWN
- DISCOVERED
- ALTERED
- REMEMBERED
- CONTRADICTED
- RECONTEXTUALIZED

Không phải mọi trạng thái đều phải dùng mọi giai đoạn.

## 8.2.7 Hệ thống lõi 05 — Ký ức

Ký ức là một lớp nằm trên trạng thái thế giới.

> **Trạng thái thế giới = những gì đang tồn tại.**  
> **Ký ức = ai nhớ điều đó và nhớ theo cách nào.**

Ví dụ:

**Trạng thái thế giới:** Cầu đã được sửa.

**Ký ức A:** NPC A nhớ, “Bạn đã sửa cây cầu.”

**Ký ức B:** NPC B nhớ, “Cây cầu đã được sửa trước khi bạn đến.”

**Ký ức người chơi:** “Chính tôi đã sửa nó.”

Ba lớp có thể cùng tồn tại.

## 8.2.8 Chủ thể ký ức

Những nơi có thể giữ ký ức:

- NPC
- Nhân vật chính
- Bạn đồng hành / Thú cưng
- Địa điểm
- Vật thể
- Cộng đồng
- Các hệ thống thế giới

Tuy nhiên:

> **Ký ức phải có chọn lọc, không phải phổ quát.**

Không phải mọi thứ đều cần trở thành một cơ chế ký ức.

## 8.2.9 Hệ thống lõi 06 — Mâu thuẫn

Ký ức trở thành cách chơi thông qua mâu thuẫn.

Ví dụ:

- Ký ức người chơi: “Tôi đã giúp.”
- Ký ức NPC: “Bạn đã bỏ đi.”
- Bằng chứng môi trường gợi ý cả hai đều có thể đúng một phần.

### Mô hình mâu thuẫn

```
Ký ức A
   +
Ký ức B
   +
Bằng chứng
   ↓
Mâu thuẫn
```

Mâu thuẫn là cách chơi có chủ đích, không phải lỗi liên tục mạch truyện.

Tuy nhiên, các mâu thuẫn phải được kiểm soát và đủ dễ hiểu để người chơi điều tra chúng.

## 8.2.10 Hệ thống bằng chứng

Bằng chứng ngăn thế giới trở thành tùy tiện.

### Các loại bằng chứng

**Vật lý**
- Vật thể
- Địa điểm
- Hư hại
- Công trình đã sửa
- Dấu chân
- Thư
- Ảnh

**Xã hội**
- Lời kể của NPC
- Hội thoại
- Tin đồn
- Ký ức cộng đồng

**Trải nghiệm**
- Ký ức người chơi
- Tương tác trước đó
- Thay đổi đã quan sát

**Thời gian**
- Trạng thái trước
- Trạng thái sau
- Được nhớ lại sau này

### Quy tắc

> **Bằng chứng ≠ Sự thật**

Bằng chứng tạo ra giả thuyết.

```
Bằng chứng → Giả thuyết
```

Người chơi về sau có thể khám phá ra rằng một cách diễn giải là sai.

## 8.2.11 Bằng chứng ≠ Sự thật

Bằng chứng nên hỗ trợ việc diễn giải, thay vì tự động hé lộ câu trả lời.

Điều này giữ xung đột trung tâm:

> **Ký ức ≠ Sự thật**

Vì vậy người chơi không chỉ đơn thuần thu thập sự kiện.

Người chơi đang dựng lại những gì có thể đã xảy ra.

## 8.2.12 Hệ thống hệ quả

Hệ thống hệ quả biến:

> **Hành động người chơi → Cách chơi tương lai**

Ví dụ:

```
Phiên chơi 01
Sửa cầu
      ↓
Phiên chơi 03
NPC nhớ người chơi
      ↓
Phiên chơi 05
Một phiên bản câu chuyện khác
      ↓
Phiên chơi 08
Bằng chứng mới gần cây cầu
      ↓
Câu hỏi mới:
“Thực sự đã xảy ra chuyện gì?”
```

Đây là tính liên tục dài hạn.

## 8.2.13 Lưu giữ

Sự lưu giữ hoạt động ở nhiều tầng:

1. Tức thì
2. Cục bộ
3. Nhân vật
4. Xuyên phiên chơi
5. Mạch truyện

Không phải mọi hành động đều cần được lưu giữ dài hạn.

### Quy tắc

> **Sự lưu giữ được dành cho những gì có ý nghĩa.**

Hành động nhỏ có thể biến mất.

Hành động có ý nghĩa nên để lại dấu vết.

## 8.2.14 Hội thoại và hiểu biết nhân vật

Hệ thống phân biệt:

- Điều một NPC **biết**
- Điều một NPC **nhớ**
- Điều một NPC **tin**

Ví dụ:

**BIẾT:** Cây cầu đã được sửa.

**NHỚ:** Bạn đã sửa nó.

**TIN:** Bạn đã đến đây từ nhiều năm trước.

Những phát biểu này không cần khớp với nhau.

Sự phân biệt này cho phép hội thoại trở thành một cách biểu hiện ký ức trong cách chơi, thay vì một mẻ đổ thông tin tĩnh.

## 8.2.15 Thú cưng / Bạn đồng hành

Bạn đồng hành hoạt động như một:

> **Hệ thống chú ý tự nhiên**

Bạn đồng hành có thể:

- Nhìn về một địa điểm
- Phản ứng với một vật thể
- Dừng lại
- Đổi hành vi
- Phản ứng khác với những nơi quen thuộc
- Giúp người chơi nhận ra một bất thường

### Quy tắc

Bạn đồng hành hướng sự chú ý, nhưng không đưa ra câu trả lời.

Nó nên truyền đạt:

> “Có gì đó ở đây.”

Không phải:

> “Đi tới đây và nhặt vật phẩm X.”

## 8.2.16 Hệ thống hiểu biết / tiến trình

Tiến trình chính là:

> **Hiểu biết**

Không phải:

> điểm kinh nghiệm → cấp nhân vật → sát thương → kẻ địch mạnh hơn

Người chơi dần tích lũy:

- Địa điểm đã khám phá
- Nhân vật đã biết
- Bằng chứng
- Câu hỏi chưa giải
- Sự kiện đã nhớ
- Mâu thuẫn
- Cách diễn giải

Hiểu biết thay đổi những gì người chơi có thể nhận ra, đặt câu hỏi và có lối vào.

## 8.2.17 Hệ thống câu hỏi

Hệ thống câu hỏi là cầu nối giữa mạch truyện và cách chơi.

Một khám phá tạo ra một câu hỏi.

Một cuộc điều tra có thể trả lời một câu hỏi đồng thời tạo ra câu hỏi khác.

Vì vậy câu hỏi là đơn vị tiến trình mang tính ẩn dụ:

> Không phải tiền.  
> Không phải cấp nhân vật.  
> **Điều người chơi vẫn chưa hiểu.**

## 8.2.18 Hệ thống phiên chơi

Một phiên chơi tuân theo mô hình trừu tượng này:

```
THIẾT LẬP
  ↓
VẤN ĐỀ
  ↓
KHÁM PHÁ
  ↓
HÀNH ĐỘNG
  ↓
THAY ĐỔI THẾ GIỚI
  ↓
HỆ QUẢ
  ↓
CÂU HỎI MỚI
```

Điều này hỗ trợ triết lý phiên chơi đã được thiết lập:

> **Một vấn đề → Một hành động chính → Một thay đổi thế giới**

## 8.2.19 Quan hệ giữa các hệ thống

```
                 NGƯỜI CHƠI
                    │
                    ▼
                 KHÁM PHÁ
                    │
                    ▼
           QUAN SÁT / ĐIỀU TRA
                    │
                    ▼
                TƯƠNG TÁC
                    │
                    ▼
                LỰA CHỌN
                    │
                    ▼
           TRẠNG THÁI THẾ GIỚI
                    │
          ┌─────────┴─────────┐
          ▼                   ▼
        KÝ ỨC              HỆ QUẢ
          │                   │
          └─────────┬─────────┘
                    ▼
               MÂU THUẪN
                    │
                    ▼
               BẰNG CHỨNG
                    │
                    ▼
              DIỄN GIẢI
                    │
                    ▼
             CÂU HỎI MỚI
                    │
                    └──────→ KHÁM PHÁ
```

Đây là cách biểu hiện bằng hệ thống của vòng lặp lõi ở 8.1.

## 8.2.20 Lõi và hỗ trợ

### Lõi

- Khám phá
- Quan sát
- Điều tra
- Tương tác
- Lựa chọn
- Trạng thái thế giới
- Ký ức
- Mâu thuẫn
- Hệ quả
- Bằng chứng

### Hỗ trợ

- Hiểu biết hội thoại
- Thú cưng
- Tiến trình
- Phiên chơi
- Giao diện / Phản hồi

Các hệ thống hỗ trợ tồn tại để củng cố vòng lặp lõi, không cạnh tranh với nó.

## 8.2.21 Quy tắc thiết kế hệ thống

1. **Cơ chế phục vụ sự tò mò** — mọi cơ chế nên tạo ra một lý do để quan tâm.
2. **Trạng thái thế giới đi trước phần trình bày** — cho thấy trạng thái trước khi giải thích bằng hội thoại.
3. **Ký ức phải vẫn có chọn lọc** — không phải mọi thứ đều là cơ chế ký ức.
4. **Mâu thuẫn phải được tạo ra có cơ sở** — Bằng chứng → Ký ức → Xung đột.
5. **Hệ quả phải cảm nhận được** — thay đổi vô hình có rất ít giá trị trải nghiệm.
6. **Không bắt buộc bảng thám tử** — giao diện hiểu biết tùy chọn có thể hỗ trợ việc hiểu, nhưng không được thay thế quan sát.
7. **Không có nhánh hội thoại tùy tiện** — sự khác biệt phải đến từ hành động, trạng thái thế giới, hiểu biết của NPC, ký ức của NPC, quan hệ và hệ quả.

## 8.2.22 Cách chơi tối thiểu đủ để thử

Một đoạn chơi thử chỉ cần chứng minh bảy điều:

1. Khám phá
2. Nhận ra một bất thường
3. Tương tác để giải một vấn đề
4. Trạng thái thế giới thay đổi
5. Thay đổi đó được lưu giữ
6. Một NPC, địa điểm hoặc vật thể nhớ theo cách khác
7. Người chơi khám phá một mâu thuẫn và nhận một câu hỏi mới

Nếu một đoạn chơi thử chứng minh được bảy điểm này, nó chứng minh được cách chơi đặc trưng.

## 8.2.23 Bản chất hệ thống trong một câu

> **Các hệ thống cách chơi của Veyloria biến hành động của người chơi thành trạng thái thế giới được lưu giữ, chuyển những trạng thái đó thành những ký ức khác nhau, và dùng mâu thuẫn giữa ký ức và bằng chứng để tạo ra câu hỏi tiếp theo của người chơi.**

## 8.2.24 Đường cơ sở đã khóa

| Thành phần | Quyết định |
|---|---|
| Khám phá | Lõi |
| Quan sát | Lõi |
| Điều tra | Lõi |
| Tương tác | Lõi |
| Lựa chọn | Lõi |
| Trạng thái thế giới | Lõi |
| Ký ức | Lõi |
| Mâu thuẫn | Lõi |
| Hệ quả | Lõi |
| Bằng chứng | Lõi |
| Hiểu biết hội thoại | Hỗ trợ |
| Thú cưng | Hỗ trợ |
| Tiến trình | Hiểu biết |
| Phiên chơi | Vấn đề → Hành động → Thay đổi |
| Đơn vị chính | Câu hỏi / Hiểu biết |
| Tiến trình sức mạnh | Không phải tiến trình chính |
| Hệ thống đặc trưng | The World Remembers |
| Chuỗi hệ thống lõi | Hành động → Trạng thái thế giới → Ký ức → Mâu thuẫn → Câu hỏi |

---

**Tiếp theo:** 8.3 — Mô hình tương tác của người chơi.
