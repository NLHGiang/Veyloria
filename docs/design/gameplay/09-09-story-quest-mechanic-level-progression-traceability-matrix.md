# 9.9 — MA TRẬN TRUY VẾT CÂU CHUYỆN → NHIỆM VỤ → CƠ CHẾ → KHÔNG GIAN CHƠI → TIẾN TRÌNH

## Mục đích

9.9 thiết lập hệ thống truy vết nối các lớp chính trong thiết kế của Veyloria.

Các bước trước đã thiết lập:

- 9.1 — Khung ánh xạ câu chuyện → cách chơi
- 9.2 — Nhịp câu chuyện → cấu trúc nhiệm vụ
- 9.3 — Loại nhiệm vụ và cách dựng nhiệm vụ
- 9.4 — Chuỗi nhiệm vụ, phụ thuộc và tiến trình
- 9.5 — Trạng thái nhiệm vụ, mục tiêu và cách nhiệm vụ diễn ra khi chơi
- 9.6 — Phần thưởng, hệ quả và thay đổi trạng thái thế giới
- 9.7 — Nhiệm vụ → không gian chơi → tích hợp trạng thái thế giới
- 9.8 — Ánh xạ tiến trình: câu chuyện → nhiệm vụ → không gian chơi → tiến trình người chơi

9.9 trả lời một câu hỏi rộng hơn:

> **Mọi quyết định thiết kế quan trọng có truy vết được từ ý đồ kể chuyện tới trải nghiệm thực của người chơi không?**

Chuỗi chuẩn là:

```text
CÂU CHUYỆN
  ↓
NHIỆM VỤ
  ↓
CƠ CHẾ
  ↓
KHÔNG GIAN CHƠI
  ↓
HÀNH ĐỘNG NGƯỜI CHƠI
  ↓
THAY ĐỔI TRẠNG THÁI
  ↓
TIẾN TRÌNH
  ↓
KHẢ NĂNG TƯƠNG LAI
```

Chiều ngược cũng phải chạy được:

```text
CƠ CHẾ
  ↓
VÌ SAO NÓ TỒN TẠI?
  ↓
NÓ HỖ TRỢ TRẢI NGHIỆM NGƯỜI CHƠI NÀO?
  ↓
NHỮNG NHIỆM VỤ NÀO DÙNG NÓ?
  ↓
NÓ PHỤC VỤ MỤC ĐÍCH CÂU CHUYỆN NÀO?
```

Một thiết kế lành mạnh phải truy vết được theo cả hai chiều.

---

# 1. Vì sao truy vết quan trọng

Các dự án trò chơi lớn tích lũy nội dung.

Không có truy vết, dự án dễ sinh ra:

- nhịp câu chuyện không có cách chơi;
- nhiệm vụ không có mục đích kể chuyện đáng kể;
- cơ chế không có chỗ dùng đáng kể;
- không gian chơi không có trải nghiệm người chơi rõ;
- phần thưởng tiến trình không có hệ quả về sau;
- hệ thống bị trùng;
- nội dung rời nhau;
- tính năng được thêm chỉ vì chúng thường gặp ở trò chơi khác.

Truy vết ngăn sự trôi này.

---

# 2. Năm lớp chính

9.9 tập trung vào năm lớp chính.

## Lớp A — Câu chuyện

Người chơi nên trải nghiệm hoặc hiểu điều gì?

## Lớp B — Nhiệm vụ

Cấu trúc chơi được nào chuyển tải trải nghiệm đó?

## Lớp C — Cơ chế

Hành động hoặc hệ thống nào của người chơi làm trải nghiệm đó có thể xảy ra?

## Lớp D — Không gian chơi

Nó xảy ra ở đâu, và qua ngữ cảnh không gian nào?

## Lớp E — Tiến trình

Sau đó, điều gì đổi với người chơi hoặc với thế giới?

Quan hệ đầy đủ là:

```text
CÂU CHUYỆN
↓
NHIỆM VỤ
↓
CƠ CHẾ
↓
KHÔNG GIAN CHƠI
↓
TIẾN TRÌNH
```

---

# 3. Truy vết câu chuyện

Mỗi nhịp câu chuyện lớn nên có một biểu hiện cách chơi.

Ví dụ:

```text
NHỊP CÂU CHUYỆN:
Người chơi phát hiện một ngôi nhà bỏ hoang gắn với quá khứ của khu định cư.
```

Truy vết:

```text
Nhịp câu chuyện
    ↓
Nhiệm vụ điều tra
    ↓
Quan sát / Điều tra / So sánh
    ↓
Không gian chơi Nhà cũ
    ↓
Hiểu biết + Khả năng kể chuyện mới
```

Nếu nhịp câu chuyện không ánh xạ được sang cách chơi, thì một trong hai điều sau là đúng:

1. Nó cần một biểu hiện cách chơi.
2. Nó nên giữ thuần điện ảnh hoặc thuần kể chuyện, và được đánh dấu rõ như vậy.

Nội dung chỉ thuộc câu chuyện mà chưa được đánh dấu không nên tích lũy một cách tình cờ.

---

# 4. Truy vết nhiệm vụ

Mỗi nhiệm vụ quan trọng phải có lý do để tồn tại.

Một nhiệm vụ nên trả lời:

```text
Vì sao nhiệm vụ này tồn tại?
Nó phục vụ mục đích câu chuyện nào?
Nó tạo trải nghiệm người chơi nào?
Cơ chế nào hỗ trợ trải nghiệm đó?
Địa điểm nào hỗ trợ nó?
Điều gì đổi sau đó?
```

Nhiệm vụ không có câu trả lời rõ là ứng viên để bỏ, gộp hoặc thiết kế lại.

---

# 5. Truy vết cơ chế

Mỗi cơ chế đáng kể phải có một mục đích.

Với mỗi cơ chế:

```text
CƠ CHẾ
   ↓
TRẢI NGHIỆM NGƯỜI CHƠI
   ↓
CÁCH DÙNG TRONG NHIỆM VỤ
   ↓
CHỨC NĂNG CÂU CHUYỆN
```

Ví dụ:

```text
Điều tra
   ↓
Người chơi rút kết luận từ chứng cứ
   ↓
Nhiệm vụ điều tra
   ↓
Hỗ trợ khám phá và hiểu lại
```

Điều này ngăn cơ chế tồn tại chỉ vì chúng thú vị về kỹ thuật.

---

# 6. Truy vết không gian chơi

Mỗi không gian chơi lớn nên có mục đích trải nghiệm đã được xác định.

Một không gian chơi nên trả lời:

- Vì sao địa điểm này cần thiết?
- Những nhiệm vụ nào dùng nó?
- Những cơ chế nào xảy ra ở đây?
- Người chơi có thể khám phá điều gì?
- Những trạng thái thế giới nào có thể đổi ở đây?
- Người chơi nhớ điều gì khi quay lại?

Không gian chơi không có chức năng riêng nên được xem lại.

---

# 7. Truy vết tiến trình

Mỗi sự kiện tiến trình có nghĩa phải có một nguồn.

Ví dụ:

```text
Tiến trình:
Được vào Nhà cũ

Nguồn:
Quan hệ với Maria

Nguyên nhân:
Người chơi đã giúp Maria

Nhiệm vụ:
Vấn đề riêng của Maria

Cơ chế:
Đối thoại / Lựa chọn / Quan hệ

Hiệu ứng thế giới:
Maria cấp quyền vào
```

Tiến trình không bao giờ nên xuất hiện như một phần thưởng không được giải thích.

---

# 8. Truy vết hai chiều

Ma trận phải chạy được theo cả hai chiều.

## Chiều thuận

```text
Câu chuyện
→ Nhiệm vụ
→ Cơ chế
→ Không gian chơi
→ Tiến trình
```

## Chiều ngược

```text
Tiến trình
→ Nguyên nhân
→ Nhiệm vụ
→ Cơ chế
→ Mục đích câu chuyện
```

Điều này then chốt đối với sản xuất.

Nếu người thiết kế hỏi:

> “Vì sao chúng ta có cơ chế này?”

dự án phải trả lời được.

Nếu người viết hỏi:

> “Nhịp câu chuyện này được chơi như thế nào?”

dự án cũng phải trả lời được.

---

# 9. Bản ghi truy vết chuẩn

Mỗi đơn vị nội dung lớn, về sau, nên được biểu diễn bằng một bản ghi dạng như sau:

```text
ID TRUY VẾT

Nhịp câu chuyện:
Nhiệm vụ:
Loại nhiệm vụ:
Chuỗi nhiệm vụ:
Cơ chế:
Vai trò cơ chế:
Không gian chơi:
Địa điểm:
Hành động người chơi:
Khám phá:
Lựa chọn:
Thay đổi trạng thái thế giới:
Tiến trình:
Khả năng mới:
Quay lại:
Mục đích kể chuyện:
Trải nghiệm người chơi:
Phụ thuộc:
Hệ quả:
Trạng thái kiểm định:
```

Đây trở thành đơn vị truy vết nền tảng.

---

# 10. Ma trận truy vết

Ma trận lõi:

| ID truy vết | Câu chuyện | Nhiệm vụ | Cơ chế | Không gian chơi | Tiến trình |
|---|---|---|---|---|---|
| T-001 | Nhịp câu chuyện A | Q-001 | Điều tra | L-001 | Hiểu biết |
| T-002 | Nhịp câu chuyện B | Q-002 | Đối thoại / Lựa chọn | L-002 | Quan hệ |
| T-003 | Nhịp câu chuyện C | Q-003 | Khám phá | L-003 | Tiếp cận |
| T-004 | Nhịp câu chuyện D | Q-004 | Tương tác thế giới | L-004 | Ảnh hưởng thế giới |

Bảng này không chỉ là tài liệu.

Nó là công cụ kiểm định thiết kế.

---

# 11. ID truy vết

Hãy dùng các ID ổn định.

Cách đặt tên khái niệm nên dùng:

```text
STORY-###
QUEST-###
MECH-###
LEVEL-###
PROG-###
TRACE-###
```

Ví dụ:

```text
STORY-014
QUEST-027
MECH-INVESTIGATION
LEVEL-OLD-HOUSE
PROG-KNOWLEDGE-008
TRACE-014-027
```

ID phải giữ ổn định ngay cả khi tên hiển thị đổi.

---

# 12. Một nhịp câu chuyện → nhiều nhiệm vụ

Một nhịp câu chuyện có thể cần vài nhiệm vụ.

Ví dụ:

```text
NHỊP CÂU CHUYỆN
"Người chơi biết lịch sử của khu định cư."
        ↓
NHIỆM VỤ A
Tìm hồ sơ còn thiếu.
        ↓
NHIỆM VỤ B
Nói chuyện với nhân chứng còn sống.
        ↓
NHIỆM VỤ C
Quay lại địa điểm.
```

Nhịp câu chuyện do đó là một mục tiêu kể chuyện, không nhất thiết là một nhiệm vụ duy nhất.

---

# 13. Nhiều nhịp câu chuyện → một nhiệm vụ

Chiều ngược cũng đúng.

Một nhiệm vụ có thể đẩy vài nhịp câu chuyện.

Ví dụ:

```text
NHIỆM VỤ
Điều tra Nhà cũ

Làm tiến:
- Lịch sử khu định cư
- Quan hệ với Maria
- Cách người chơi hiểu nhân vật chính
```

Việc này phải có chủ đích.

Nhiệm vụ không được quá tải bởi các chức năng kể chuyện không liên quan.

---

# 14. Một nhiệm vụ → nhiều cơ chế

Một nhiệm vụ có thể gộp nhiều cơ chế.

Ví dụ:

```text
NHIỆM VỤ
Điều tra Nhà cũ

Cơ chế:
- Khám phá
- Quan sát
- Điều tra
- Tương tác
- Đối thoại
- Lựa chọn
```

Dù vậy, các cơ chế phải có vai trò tách bạch.

Không thêm cơ chế chỉ để tăng sự đa dạng.

---

# 15. Một cơ chế → nhiều nhiệm vụ

Một cơ chế vững nên dùng lại được.

Ví dụ:

```text
ĐIỀU TRA
   ├── Nhà cũ
   ├── Sự cố trong rừng
   ├── Người mất tích
   └── Hồ sơ lịch sử
```

Điều này tạo sự nhất quán về cơ chế.

Cơ chế có thể tăng độ phức tạp qua ngữ cảnh, thay vì bị làm lại từ đầu.

---

# 16. Một không gian chơi → nhiều nhiệm vụ

Một địa điểm thường trực nên đỡ được nhiều trải nghiệm.

Ví dụ:

```text
NHÀ CŨ
   ├── Điều tra ban đầu
   ├── Cảnh quan hệ
   ├── Quay lại
   └── Hé lộ cuối
```

Điều này đáng ưu tiên hơn việc dựng một không gian chơi dùng rồi bỏ cho mỗi nhiệm vụ, khi mạch kể được lợi từ tính liên tục.

---

# 17. Một tiến trình → nhiều nguyên nhân

Một trạng thái có thể tới được bằng những hành động người chơi khác nhau.

Ví dụ:

```text
TIẾP CẬN: VÙNG PHÍA BẮC

Các nguyên nhân có thể:
- Sửa cầu
- Tìm lối đi khác
- Có được thuyền
```

Đích tiến trình là chung.

Con đường và hệ quả có thể khác nhau.

---

# 18. Truy vết không phải quan hệ một–một

Hệ thống không được ép:

```text
1 Câu chuyện
→ 1 Nhiệm vụ
→ 1 Cơ chế
→ 1 Không gian chơi
→ 1 Tiến trình
```

Cấu trúc thật là nhiều–nhiều.

```text
Câu chuyện ─────┐
                ├── Nhiệm vụ ──── Cơ chế
Câu chuyện ─────┘        │           │
                         ↓           ↓
             Không gian chơi ← Trạng thái thế giới
                         │
                         ↓
                    Tiến trình
```

Sự linh hoạt này là thiết yếu.

---

# 19. Liên kết chính và liên kết phụ

Không phải quan hệ nào cũng nặng như nhau.

Mỗi truy vết nên tách:

### Chính

Mục đích chính của mối nối.

### Phụ

Một quan hệ đỡ có ý nghĩa.

Ví dụ:

```text
Nhiệm vụ:
Điều tra Nhà cũ

Cơ chế chính:
Điều tra

Cơ chế phụ:
Khám phá
Đối thoại

Tiến trình chính:
Hiểu biết

Tiến trình phụ:
Quan hệ
```

Điều này ngăn ma trận trở thành một danh sách liên kết vô nghĩa.

---

# 20. Phân loại mục đích câu chuyện

Mỗi nhiệm vụ nên có một mục đích kể chính.

Các mục đích có thể có:

- giới thiệu;
- điều tra;
- hé lộ;
- thiết lập;
- đào sâu;
- làm phức tạp;
- chuyển hóa;
- đối mặt;
- giải quyết;
- hiểu lại;
- kết thúc.

Một nhiệm vụ có thể có thêm mục đích phụ.

---

# 21. Phân loại trải nghiệm người chơi

Mỗi truy vết cũng nên chỉ ra trải nghiệm chủ đạo đã định.

Ví dụ:

- tò mò;
- khám phá;
- bất định;
- gắn kết;
- căng thẳng;
- suy ngẫm;
- hệ quả;
- nhận ra;
- mất mát;
- nhẹ nhõm;
- quyền chủ động.

Trải nghiệm người chơi là cầu nối giữa mạch kể và cách chơi.

---

# 22. Phân loại vai trò cơ chế

Một cơ chế có thể đóng những vai khác nhau.

### Khám phá

Giúp người chơi học được một điều.

### Biểu đạt

Để người chơi bày một lựa chọn.

### Tương tác

Để người chơi chạm thẳng vào thế giới.

### Di chuyển

Đỡ việc di chuyển hoặc việc hiểu không gian.

### Quan hệ

Đổi các khả năng xã hội.

### Hệ quả

Để người chơi đổi thế giới.

### Diễn giải

Để người chơi hiểu chứng cứ.

Cách phân loại này làm việc dùng cơ chế chính xác hơn.

---

# 23. Phân loại vai trò không gian chơi

Một không gian chơi cũng nên có một vai trò chính.

Ví dụ:

- trung tâm kể;
- điểm điều tra;
- không gian quan hệ;
- vùng khám phá;
- vùng chuyển;
- không gian ký ức;
- không gian hệ quả;
- không gian cao trào;
- không gian suy ngẫm.

Vai trò quyết định cách không gian chơi nên được thiết kế.

---

# 24. Phân loại vai trò tiến trình

Tiến trình có thể xếp thành:

- năng lực;
- hiểu biết;
- quan hệ;
- tiếp cận;
- ảnh hưởng thế giới;
- kể chuyện;
- khám phá;
- ký ức;
- hiểu biết chiến lược.

Ma trận nên chỉ ra cả tiến trình chính lẫn tiến trình phụ.

---

# 25. Ví dụ truy vết đầy đủ

```text
TRACE-014

CÂU CHUYỆN:
Nhân vật chính phát hiện ngôi nhà bỏ hoang chứa chứng cứ
mâu thuẫn với lịch sử được chấp nhận của khu định cư.

NHIỆM VỤ:
Q-027 — Ngôi nhà còn nhớ

LOẠI CHÍNH:
Điều tra

CƠ CHẾ:
Chính:
Điều tra

Phụ:
Khám phá
Quan sát
Tương tác

KHÔNG GIAN CHƠI:
L-011 — Nhà cũ

TRẢI NGHIỆM NGƯỜI CHƠI:
Tò mò → Khám phá → Nghi ngờ

HÀNH ĐỘNG NGƯỜI CHƠI:
Tìm, so sánh, xem kỹ, diễn giải.

KHÁM PHÁ:
Mâu thuẫn lịch sử.

LỰA CHỌN:
Có tiết lộ phát hiện ngay hay không.

TRẠNG THÁI THẾ GIỚI:
house.relevance = HIGH

TIẾN TRÌNH:
Chính:
Hiểu biết

Phụ:
Quan hệ

KHẢ NĂNG MỚI:
Đối thoại mới và lối điều tra mới.

QUAY LẠI:
Nhà cũ được hiểu lại.

MỤC ĐÍCH KỂ CHUYỆN:
Hé lộ + Hiểu lại.
```

Đây là một truy vết đủ.

---

# 26. Độ phủ truy vết

Dự án nên đo độ phủ.

Với câu chuyện:

```text
Nhịp câu chuyện đã phủ
----------------------
Tổng nhịp câu chuyện lớn
```

Với cơ chế:

```text
Cơ chế có mục đích câu chuyện / trải nghiệm
-------------------------------------------
Tổng cơ chế đáng kể
```

Với không gian chơi:

```text
Không gian chơi có vai trò trải nghiệm đã xác định
--------------------------------------------------
Tổng không gian chơi lớn
```

Với tiến trình:

```text
Sự kiện tiến trình có nguyên nhân truy vết được
-----------------------------------------------
Tổng sự kiện tiến trình lớn
```

Các ngưỡng phần trăm chính xác nên được định trong lúc kiểm định sản xuất.

---

# 27. Độ phủ câu chuyện

Mỗi nhịp câu chuyện lớn nên được xếp vào một trong các loại:

```text
CHƠI ĐƯỢC
ĐIỆN ẢNH
ĐỐI THOẠI
MÔI TRƯỜNG
HỆ THỐNG
KẾT HỢP
```

Yêu cầu quan trọng là tính có chủ đích.

Một nhịp câu chuyện không bao giờ nên bị bỏ không làm chỉ vì không ai ánh xạ nó.

---

# 28. Độ phủ cách chơi

Mỗi nhịp câu chuyện lớn được định là chơi được nên có:

```text
Nhiệm vụ
+
Hành động người chơi
+
Cơ chế
+
Ngữ cảnh chơi được
```

Nếu thiếu một mắt xích, nhịp đó chưa được chuyển thể đầy đủ.

---

# 29. Độ phủ cơ chế

Mỗi cơ chế lớn nên có:

```text
Cơ chế
↓
Trải nghiệm người chơi
↓
Cách dùng trong nhiệm vụ
↓
Cách dùng trong không gian chơi
```

Cơ chế không có chỗ dùng nội dung đáng kể là ứng viên để:

- bỏ;
- hoãn lại;
- thiết kế lại;
- thử nghiệm tùy chọn.

---

# 30. Độ phủ không gian chơi

Mỗi không gian chơi lớn nên có:

```text
Không gian chơi
↓
Mục đích trải nghiệm
↓
Liên kết nhiệm vụ
↓
Liên kết cơ chế
↓
Vai trò trạng thái thế giới
```

Không gian chơi không đóng góp trạng thái hoặc trải nghiệm đáng kể nên bị chất vấn.

---

# 31. Độ phủ tiến trình

Mỗi sự kiện tiến trình lớn nên có:

```text
Tiến trình
↓
Điểm kích hoạt
↓
Trải nghiệm người chơi
↓
Khả năng tương lai
```

Một phần thưởng không đổi gì có ý nghĩa thì không nên tự động bị xếp là tiến trình.

---

# 32. Truy vết ngược: Cơ chế → Câu chuyện

Với mỗi cơ chế đáng kể, hãy hỏi:

> Câu chuyện hoặc trải nghiệm người chơi nào đòi cơ chế này?

Ví dụ:

```text
Cơ chế:
Quan sát

Câu hỏi:
Vì sao ta cần quan sát?

Câu trả lời:
Vì người chơi phải phát hiện các mâu thuẫn của môi trường
mà không cần thuyết minh thẳng.
```

Điều này cho cơ chế một lý do để tồn tại.

---

# 33. Truy vết ngược: Không gian chơi → Câu chuyện

Với mỗi không gian chơi lớn:

> Câu chuyện hoặc trải nghiệm người chơi nào không thể được chuyển tải tốt ngang bằng ở nơi khác?

Nếu câu trả lời là:

> Không có.

thì không gian chơi đó có thể là dư thừa.

Điều này không có nghĩa mọi địa điểm phải độc nhất về cơ chế.

Nghĩa là sự có mặt của nó phải có mục đích trải nghiệm rõ.

---

# 34. Truy vết ngược: Nhiệm vụ → Câu chuyện

Với mỗi nhiệm vụ:

> Nếu nhiệm vụ này bị gỡ bỏ, người chơi sẽ mất gì?

Các câu trả lời có thể có:

- hiểu biết cốt yếu về câu chuyện;
- phát triển quan hệ;
- hệ quả thế giới;
- khám phá;
- trải nghiệm cảm xúc;
- góc nhìn thay thế.

Nếu câu trả lời là:

> Không gì có ý nghĩa.

Nhiệm vụ đó nhiều khả năng là không cần thiết.

---

# 35. Truy vết ngược: Tiến trình → Nguyên nhân

Với mỗi lần mở khóa tiến trình:

> Người chơi đã làm gì để có được khả năng này?

Nếu không có câu trả lời có nghĩa, tiến trình có thể cảm thấy tùy tiện.

Ưu tiên:

```text
HÀNH ĐỘNG
→ HỆ QUẢ
→ KHẢ NĂNG
```

Không phải:

```text
XONG NHIỆM VỤ
→ MỞ KHÓA NGẪU NHIÊN
```

---

# 36. Truy vết và quyền chủ động của người chơi

Truy vết phải giữ được lựa chọn của người chơi.

Nếu hai người chơi tới cùng một địa điểm bằng những lối khác nhau:

```text
LỐI A
Sửa cầu
```

và:

```text
LỐI B
Tìm thuyền
```

bản truy vết nên giữ:

- nguyên nhân;
- lựa chọn;
- hệ quả;
- trạng thái thế giới liên quan.

Ma trận không được rút gọn cả hai lối thành:

```text
Xong nhiệm vụ → Mở vùng
```

rồi xóa mất khác biệt có nghĩa.

---

# 37. Truy vết nhánh

Với nội dung phân nhánh:

```text
TRACE-A
   ↓
LỰA CHỌN
 /    \
A      B
|      |
↓      ↓
TRẠNG THÁI A   TRẠNG THÁI B
 \            /
  \          /
 NỘI DUNG CHUNG
```

Mỗi nhánh phải xác định:

- cơ chế riêng;
- trạng thái riêng;
- hệ quả riêng;
- điểm hội tụ;
- khác biệt còn lại.

---

# 38. Truy vết hiểu lại

Một sự kiện được hiểu lại nên tham chiếu rõ nội dung gốc.

Ví dụ:

```text
TRACE-021
Diễn giải ban đầu

        ↓

TRACE-047
Chứng cứ mới

        ↓

TRACE-048
Diễn giải lại

        ↓

TRACE-021'
Sự kiện trước nhận nghĩa mới
```

Điều này cho phép tính liên tục của mạch kể được thiết kế, thay vì ứng biến.

---

# 39. Truy vết quay lại

Với các địa điểm được thiết kế quanh việc quay lại:

```text
Lần đến đầu
↓
Đổi trạng thái
↓
Đổi hiểu biết của người chơi
↓
Thời gian / Tiến câu chuyện
↓
Quay lại
↓
Tương tác mới
↓
Hiểu lại
```

Ma trận nên nối rõ trải nghiệm lần đầu với các lần sau.

---

# 40. Truy vết và trạng thái thế giới

Mỗi thay đổi trạng thái thế giới có nghĩa nên xác định:

```text
Nguyên nhân
↓
Trạng thái
↓
Đáp của không gian chơi
↓
Đáp của NPC
↓
Đáp của nhiệm vụ
↓
Phản hồi tới người chơi
```

Ví dụ:

```text
Nguyên nhân:
Người chơi đã sửa cầu.

Trạng thái:
bridge = REPAIRED

Không gian chơi:
Cầu đi qua được.

NPC:
Thương nhân trở lại.

Nhiệm vụ:
Nhiệm vụ của thương nhân mở ra.

Phản hồi:
Người chơi thấy hoạt động của khu định cư tăng.
```

---

# 41. Phát hiện nội dung không gắn vào đâu

Ma trận có thể chỉ ra **nội dung không gắn vào đâu**.

### Nhịp câu chuyện không gắn

Nhịp câu chuyện không có biểu hiện cách chơi.

### Nhiệm vụ không gắn

Nhiệm vụ không có mục đích câu chuyện hoặc trải nghiệm đáng kể.

### Cơ chế không gắn

Cơ chế không có chỗ dùng trong nhiệm vụ đáng kể.

### Không gian chơi không gắn

Không gian chơi không có vai trò cách chơi đáng kể.

### Tiến trình không gắn

Tiến trình không có nguyên nhân truy vết được.

Đây là các đích rà soát có giá trị cao.

---

# 42. Phát hiện trùng lặp

Ma trận cũng có thể chỉ ra sự trùng không cần thiết.

Ví dụ:

```text
NHIỆM VỤ A → Điều tra → Nhà cũ
NHIỆM VỤ B → Điều tra → Nhà cũ
NHIỆM VỤ C → Điều tra → Nhà cũ
```

Điều này không tự động là điều xấu.

Nhưng đội nên hỏi:

- Các trải nghiệm có khác nhau một cách có nghĩa không?
- Cùng một cơ chế có đang bị lặp mà không tiến hóa không?
- Các nhiệm vụ có thể được gộp không?
- Sự lặp lại có chủ đích xây sự quen thuộc không?

Sự trùng lặp phải là có chủ đích.

---

# 43. Độ bão hòa cơ chế

Truy vết có thể làm lộ việc dùng quá mức.

Ví dụ:

```text
Điều tra
████████████████████

Đối thoại
████████████

Khám phá
██████

Thay đổi thế giới
██
```

Điều này có thể cho thấy điều tra đang chiếm thế.

Điều đó không vốn đã sai.

Nó chỉ thành vấn đề khi trải nghiệm tạo ra xung đột với các trụ cột cách chơi hoặc nhịp độ đã định.

---

# 44. Phân bố tiến trình

Ma trận cũng có thể làm lộ sự lệch tiến trình.

Ví dụ:

```text
Hiểu biết            ███████████
Quan hệ              ███████
Tiếp cận             █████
Năng lực             ██
Ảnh hưởng thế giới   ███
Ký ức                ██████
```

Điều này cho một chẩn đoán thiết kế.

Mục tiêu không phải là phân bố đều.

Mục tiêu là phân bố có chủ đích.

---

# 45. Truy vết và nhịp độ

Ma trận cũng nên hỗ trợ việc phân tích nhịp độ.

Ví dụ:

```text
Nhiệm vụ 01
→ Hiểu biết

Nhiệm vụ 02
→ Quan hệ

Nhiệm vụ 03
→ Khám phá

Nhiệm vụ 04
→ Thay đổi thế giới

Nhiệm vụ 05
→ Hiểu lại
```

Điều này cho đội một nhịp tiến trình.

Một chuỗi dài những trải nghiệm giống hệt có thể được phát hiện trước khi triển khai.

---

# 46. Truy vết và phạm vi sản xuất

Truy vết giúp ước chi phí sản xuất.

Một nhiệm vụ đơn có thể đòi:

```text
Nhiệm vụ
+ 3 Cơ chế
+ 2 Địa điểm
+ 4 trạng thái NPC
+ 5 trạng thái đối thoại
+ 3 lần đổi trạng thái thế giới
+ 2 trạng thái quay lại
```

Nhiệm vụ ấy đắt hơn mức tên của nó gợi ra.

Ma trận vì thế trở thành công cụ lập kế hoạch sản xuất.

---

# 47. Điểm phức tạp

Một công cụ sản xuất về sau có thể tính độ phức tạp xấp xỉ từ:

```text
Độ phức tạp nhiệm vụ
=
Mục tiêu
+
Cơ chế
+
Địa điểm
+
Thay đổi trạng thái NPC
+
Thay đổi trạng thái thế giới
+
Nhánh
+
Lần quay lại
+
Phụ thuộc
```

Nên dùng nó như một trợ giúp khi lập kế hoạch, không thay phán đoán thiết kế.

---

# 48. Truy vết và kiểm thử

Mỗi truy vết, về sau, nên sinh ra các điều kiện kiểm thử được.

Ví dụ:

```text
TRACE-014

Cho trước:
house.state = ABANDONED

Khi:
người chơi phát hiện bức ảnh giấu kín

Thì:
knowledge.house_history = TRUE

Và:
quest.Q027.state = RECONTEXTUALIZED

Và:
đối thoại mới mở ra
```

Điều này tạo một cầu nối trực tiếp từ tài liệu thiết kế tới QA.

---

# 49. Ánh xạ từ thiết kế sang kiểm thử

Chuỗi sản xuất lý tưởng là:

```text
Ý ĐỒ THIẾT KẾ
     ↓
BẢN GHI TRUY VẾT
     ↓
TRIỂN KHAI
     ↓
ĐIỀU KIỆN KIỂM THỬ
     ↓
KIỂM ĐỊNH QA
```

Điều này giảm rủi ro triển khai đúng các cơ chế nhưng vô tình làm sai trải nghiệm người chơi đã định.

---

# 50. Truy vết và triển khai

Ma trận không nên áp đặt kiến trúc triển khai.

Nó định nghĩa các quan hệ.

Ví dụ:

```text
TRUY VẾT:
Cầu đã được sửa
```

không quy định:

- lớp cụ thể;
- lược đồ cơ sở dữ liệu;
- bus sự kiện;
- kiến trúc cảnh;
- cách làm trong engine.

Những việc đó thuộc giai đoạn thiết kế kỹ thuật.

Ma trận định nghĩa:

> **Điều gì phải vẫn đúng xuyên các hệ thống.**

---

# 51. Truy vết và người chịu trách nhiệm nội dung

Mỗi truy vết, về sau, có thể có người chịu trách nhiệm trong sản xuất.

Ví dụ:

```text
Câu chuyện:
Kể chuyện

Nhiệm vụ:
Thiết kế nhiệm vụ

Cơ chế:
Thiết kế hệ thống

Không gian chơi:
Thiết kế không gian chơi

Đối thoại:
Viết lời

Trạng thái thế giới:
Hệ thống / Cách chơi

Kiểm định:
QA
```

Điều này ngăn các lỗ hổng về người chịu trách nhiệm.

---

# 52. Trạng thái rà soát truy vết

Mỗi truy vết, về sau, nên có một trạng thái rà soát.

Các trạng thái gợi ý:

```text
NHÁP
ĐÃ ÁNH XẠ
ĐÃ RÀ SOÁT
ĐÃ PHÊ DUYỆT
ĐÃ TRIỂN KHAI
ĐÃ KIỂM ĐỊNH
ĐÃ ĐỔI
NGỪNG DÙNG
```

Một truy vết không nên được coi là xong về sản xuất chỉ vì nó có mặt trong tài liệu.

---

# 53. Tác động của thay đổi

Truy vết trở nên đặc biệt có giá trị khi một thiết kế đổi.

Ví dụ:

Một nhịp câu chuyện bị gỡ.

Ma trận có thể làm lộ:

```text
Nhịp câu chuyện
 ├── Nhiệm vụ A
 ├── Nhiệm vụ B
 ├── Cơ chế X
 ├── Không gian chơi Y
 └── Tiến trình Z
```

Đội khi đó xác định được những gì cũng phải đổi.

Không có truy vết, các phụ thuộc này dễ bị bỏ sót.

---

# 54. Tác động ngược

Chiều ngược cũng vậy.

Giả sử một cơ chế bị gỡ.

Truy vết làm lộ:

```text
Cơ chế X
 ├── Nhiệm vụ A
 ├── Nhiệm vụ C
 ├── Không gian chơi B
 └── Tiến trình D
```

Đội có thể thiết kế lại nội dung bị ảnh hưởng một cách có chủ đích.

---

# 55. Đồ thị truy vết chuẩn

Hệ thống đầy đủ là:

```text
                         ┌───────────────────────┐
                         │      CÂU CHUYỆN       │
                         └───────────┬───────────┘
                                     ↓
                         ┌───────────────────────┐
                         │       NHIỆM VỤ        │
                         └───────────┬───────────┘
                                     ↓
                         ┌───────────────────────┐
                         │        CƠ CHẾ         │
                         └───────────┬───────────┘
                                     ↓
                         ┌───────────────────────┐
                         │    KHÔNG GIAN CHƠI    │
                         └───────────┬───────────┘
                                     ↓
                         ┌───────────────────────┐
                         │ HÀNH ĐỘNG NGƯỜI CHƠI  │
                         └───────────┬───────────┘
                                     ↓
                         ┌───────────────────────┐
                         │  TRẠNG THÁI THẾ GIỚI  │
                         └───────────┬───────────┘
                                     ↓
                         ┌───────────────────────┐
                         │      TIẾN TRÌNH       │
                         └───────────┬───────────┘
                                     ↓
                         ┌───────────────────────┐
                         │     KHẢ NĂNG MỚI      │
                         └───────────┬───────────┘
                                     ↓
                                 CÂU CHUYỆN
```

Điều này tạo một vòng thiết kế khép.

---

# 56. Nguyên tắc vòng khép

Chu kỳ thiết kế lý tưởng của Veyloria là:

```text
Câu chuyện tạo ra một câu hỏi.
       ↓
Nhiệm vụ trao cho người chơi một tình huống.
       ↓
Cơ chế để người chơi hành động.
       ↓
Không gian chơi cho hành động một ngữ cảnh.
       ↓
Người chơi đổi một điều gì đó.
       ↓
Thế giới đáp lại.
       ↓
Tiến trình tạo ra một khả năng mới.
       ↓
Khả năng mới tạo ra một câu hỏi mới.
```

Đây là vòng truy vết nền tảng.

---

# 57. Mẫu ma trận truy vết

Bản dùng cho sản xuất, về sau, nên chứa ít nhất:

| Trường | Mô tả |
|---|---|
| ID truy vết | Định danh truy vết ổn định |
| ID câu chuyện | Nhịp câu chuyện nguồn |
| Mục đích câu chuyện | Chức năng kể chuyện |
| ID nhiệm vụ | Nhiệm vụ liên kết |
| Loại nhiệm vụ | Loại nhiệm vụ chính |
| ID cơ chế | Cơ chế chính |
| Vai trò cơ chế | Cơ chế hoàn thành việc gì |
| ID không gian chơi | Không gian chơi chính |
| Vai trò không gian chơi | Chức năng không gian |
| Hành động người chơi | Người chơi thực sự làm gì |
| Khám phá | Người chơi biết được gì |
| Lựa chọn | Người chơi quyết định gì |
| Trạng thái thế giới | Điều gì đổi |
| Loại tiến trình | Người chơi nhận được hoặc mất gì |
| Khả năng mới | Điều gì mở ra sau đó |
| Quay lại | Quan hệ về sau với nội dung |
| Phụ thuộc | Các trạng thái bắt buộc |
| Hệ quả | Hiệu ứng còn lại |
| Kiểm định | Cách nó được kiểm thử |
| Trạng thái | Trạng thái sản xuất hiện tại |

---

# 58. Kiểm tra sức khỏe truy vết

Một truy vết là lành mạnh khi:

- Mục đích câu chuyện rõ.
- Trải nghiệm người chơi rõ.
- Mục đích nhiệm vụ rõ.
- Cơ chế là cần thiết.
- Không gian chơi có mục đích không gian.
- Hành động người chơi có nghĩa.
- Trạng thái thế giới có thể đổi.
- Tiến trình nhận ra được.
- Có khả năng tương lai, hoặc trải nghiệm khép lại có chủ đích.
- Hệ quả được hiểu.
- Phụ thuộc được biện minh.
- Hành vi khi quay lại được xác định ở những chỗ liên quan.
- Kết quả cảm thấy nhất quán với Veyloria.

---

# 59. Dấu hiệu cần xem lại

Một truy vết nên được rà soát khi:

```text
Câu chuyện → không có Nhiệm vụ
Nhiệm vụ → không có Cơ chế có nghĩa
Cơ chế → không có mục đích Câu chuyện / Trải nghiệm
Không gian chơi → không có mục đích riêng
Tiến trình → không có nguyên nhân
Thay đổi thế giới → không có phản hồi người chơi thấy được
Lựa chọn → không có hệ quả
Quay lại → không có khác biệt có nghĩa
Phần thưởng → không có khả năng tương lai
```

Chúng không tự động là lỗi.

Chúng là tín hiệu cần rà soát.

---

# 60. Chấm điểm truy vết

Một hệ thống kiểm định về sau có thể chấm mỗi truy vết theo:

```text
Độ rõ của kể
Mức dính với cách chơi
Mức cần của cơ chế
Mức dính với không gian
Mức dính với tiến trình
Tính nhất quán của trạng thái
Quyền chủ động của người chơi
Độ bền
Giá trị khi quay lại
Khả năng kiểm thử
```

Điểm nên hỗ trợ thảo luận, thay vì trở thành một phán xét máy cứng nhắc.

---

# 61. Truy vết tối thiểu khả dụng

Không phải mọi mảnh nội dung nhỏ đều cần một bản ghi truy vết đầy đủ.

Với nội dung nhỏ:

```text
Mục đích câu chuyện
Nhiệm vụ
Cơ chế
Không gian chơi
Kết quả
```

có thể là đủ.

Với nội dung lớn:

```text
Bản ghi truy vết đầy đủ
```

nên được yêu cầu.

Điều này giữ tài liệu tương xứng với tầm quan trọng trong sản xuất.

---

# 62. Nội dung lớn đòi hỏi truy vết đầy đủ

Truy vết đầy đủ nên là bắt buộc đối với:

- nhịp câu chuyện lớn;
- nhiệm vụ chính;
- chuỗi nhiệm vụ tùy chọn lớn;
- địa điểm lớn;
- cơ chế lõi;
- thay đổi trạng thái thế giới đáng kể;
- trạng thái quan hệ lớn;
- cổng tiến trình lớn;
- các kết thúc;
- sự kiện hiểu lại.

---

# 63. Truy vết các kết thúc

Các kết thúc đòi hỏi truy vết đặc biệt chặt.

Kết cục cuối nên truy vết được ngược lại:

```text
KẾT THÚC
  ↓
TRẠNG THÁI THẾ GIỚI CUỐI
  ↓
LỰA CHỌN NGƯỜI CHƠI
  ↓
HỆ QUẢ NHIỆM VỤ
  ↓
QUAN HỆ
  ↓
HIỂU BIẾT
  ↓
HÀNH ĐỘNG TRƯỚC ĐÓ
```

Kết thúc nên cảm thấy là hệ quả của trải nghiệm người chơi đã tích lại.

Nó không nên cảm thấy như một bộ chọn nhánh cuối không dính gì.

---

# 64. Truy vết phần mở đầu

Cùng nguyên tắc áp dụng cho phần đầu.

```text
Lời hứa của câu chuyện mở đầu
        ↓
Cách chơi ban đầu
        ↓
Lần đưa cơ chế lõi
        ↓
Nhiệm vụ đầu
        ↓
Lựa chọn có nghĩa đầu tiên
        ↓
Hệ quả đầu tiên
```

Phần mở đầu lập cam kết cho cả trò chơi.

---

# 65. Truy vết vòng lõi

Vòng cách chơi lõi của trò chơi cũng nên truy vết được.

```text
Fantasy người chơi
      ↓
Trụ cột cách chơi
      ↓
Vòng lõi
      ↓
Ngữ pháp nhiệm vụ
      ↓
Cơ chế
      ↓
Cấu trúc không gian chơi
      ↓
Tiến trình
```

Nếu một cơ chế lõi không góp vào chuỗi này, nó nên bị chất vấn.

---

# 66. Truy vết ngược về Bước 8

Bước 8 đã định nghĩa các hệ thống cách chơi.

Bước 9 giờ phải chứng minh các hệ thống đó thực sự được dùng.

Về khái niệm:

```text
8.1 Fantasy người chơi
      ↓
8.2 Hệ thống cách chơi
      ↓
8.3 Mô hình tương tác
      ↓
...
8.x Ràng buộc
      ↓
9.x Ánh xạ nhiệm vụ / thế giới
```

Điều này bảo đảm việc chuyển thể cách chơi không bị đứt khỏi bản sắc cách chơi ban đầu.

---

# 67. Truy vết ngược về câu chuyện

Tương tự:

```text
Nền câu chuyện
      ↓
Kịch bản
      ↓
Chuyển thể cách chơi
      ↓
Ánh xạ nhiệm vụ
      ↓
Ánh xạ không gian chơi
      ↓
Tiến trình
```

Điều này ngăn việc triển khai cách chơi âm thầm đổi ý nghĩa nền của câu chuyện.

---

# 68. Bất biến truy vết

Một yếu tố thiết kế lớn nên thỏa:

```text
Ý ĐỒ
=
TRẢI NGHIỆM
=
TRIỂN KHAI
```

Không trùng hình thức theo nghĩa đen, nhưng cùng mục đích.

Phần triển khai có thể khác về kỹ thuật so với thiết kế gốc.

Trải nghiệm đã định cho người chơi thì không được lệch.

---

# 69. Phép thử truy vết cuối

Với bất kỳ tính năng lớn nào, hãy hỏi:

> **Vì sao thứ này tồn tại?**

Rồi trả lời:

```text
Vì câu chuyện đòi hỏi...
→ điều đó tạo ra nhiệm vụ...
→ nhiệm vụ đó đòi hỏi người chơi...
→ điều đó được mở ra bởi cơ chế...
→ điều đó diễn ra tại...
→ điều đó đổi...
→ điều đó trao cho người chơi...
→ điều đó tạo ra...
```

Nếu chuỗi không đi hết được, tính năng cần được rà soát.

---

# 70. Chuỗi chủ của Bước 9

Khi 9.9 hoàn tất, chuỗi Bước 9 có thể được biểu diễn như sau:

```text
9.1 Khung ánh xạ câu chuyện → cách chơi
        ↓
9.2 Nhịp câu chuyện → cấu trúc nhiệm vụ
        ↓
9.3 Loại nhiệm vụ và cách dựng nhiệm vụ
        ↓
9.4 Chuỗi nhiệm vụ, phụ thuộc và tiến trình
        ↓
9.5 Trạng thái nhiệm vụ, mục tiêu và cách nhiệm vụ diễn ra khi chơi
        ↓
9.6 Phần thưởng, hệ quả và thay đổi trạng thái thế giới
        ↓
9.7 Nhiệm vụ → không gian chơi → tích hợp trạng thái thế giới
        ↓
9.8 Ánh xạ tiến trình: câu chuyện → nhiệm vụ → không gian chơi → tiến trình người chơi
        ↓
9.9 Ma trận truy vết câu chuyện → nhiệm vụ → cơ chế → không gian chơi → tiến trình
        ↓
9.10 Bản chốt nội dung cách chơi
```

---

# 71. Tiêu chí hoàn thành 9.9

9.9 hoàn tất khi các yếu tố thiết kế lớn của Veyloria truy vết được theo cả hai chiều.

### Chiều thuận

```text
Câu chuyện
→ Nhiệm vụ
→ Cơ chế
→ Không gian chơi
→ Hành động người chơi
→ Trạng thái thế giới
→ Tiến trình
→ Khả năng tương lai
```

### Chiều ngược

```text
Cơ chế
→ Trải nghiệm người chơi
→ Nhiệm vụ
→ Mục đích câu chuyện

Không gian chơi
→ Trải nghiệm người chơi
→ Nhiệm vụ
→ Mục đích câu chuyện

Tiến trình
→ Nguyên nhân
→ Nhiệm vụ
→ Cơ chế
→ Mục đích câu chuyện
```

Phép thử cuối là:

> **Đội có giải thích được vì sao mọi mảnh cách chơi lớn tồn tại, và chỉ ra được mọi ý đồ câu chuyện lớn trở thành chơi được ở đâu không?**

Nếu có, khung ánh xạ của Bước 9 là mạch lạc.

---

# 72. TRẠNG THÁI CUỐI BƯỚC 9

Đã hoàn thành:

- **9.1 — Khung ánh xạ câu chuyện → cách chơi**
- **9.2 — Nhịp câu chuyện → cấu trúc nhiệm vụ**
- **9.3 — Loại nhiệm vụ và cách dựng nhiệm vụ**
- **9.4 — Chuỗi nhiệm vụ, phụ thuộc và tiến trình**
- **9.5 — Trạng thái nhiệm vụ, mục tiêu và cách nhiệm vụ diễn ra khi chơi**
- **9.6 — Phần thưởng, hệ quả và thay đổi trạng thái thế giới**
- **9.7 — Nhiệm vụ → không gian chơi → tích hợp trạng thái thế giới**
- **9.8 — Ánh xạ tiến trình: câu chuyện → nhiệm vụ → không gian chơi → tiến trình người chơi**
- **9.9 — MA TRẬN TRUY VẾT CÂU CHUYỆN → NHIỆM VỤ → CƠ CHẾ → KHÔNG GIAN CHƠI → TIẾN TRÌNH**

Dự án giờ có một chuỗi khái niệm:

```text
CÂU CHUYỆN
  ↓
Ý ĐỒ CÁCH CHƠI
  ↓
NHIỆM VỤ
  ↓
CHUỖI NHIỆM VỤ
  ↓
CÁCH NHIỆM VỤ DIỄN RA
  ↓
CƠ CHẾ
  ↓
KHÔNG GIAN CHƠI
  ↓
HÀNH ĐỘNG NGƯỜI CHƠI
  ↓
TRẠNG THÁI THẾ GIỚI
  ↓
TIẾN TRÌNH
  ↓
KHẢ NĂNG MỚI
  ↓
CÂU HỎI CÂU CHUYỆN MỚI
```

## Tiếp theo

**9.10 — Bản chốt nội dung cách chơi**
