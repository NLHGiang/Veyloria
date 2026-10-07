# 9.7 — NHIỆM VỤ → KHÔNG GIAN CHƠI → TÍCH HỢP TRẠNG THÁI THẾ GIỚI

## Mục đích

9.7 xác định cách nhiệm vụ được chuyển thành không gian có thể chơi, và cách những không gian đó đáp lại các thay đổi trạng thái thế giới được lưu bền.

Các bước trước đã thiết lập:

- 9.1 — Khung ánh xạ câu chuyện → cách chơi
- 9.2 — Nhịp câu chuyện → cấu trúc nhiệm vụ
- 9.3 — Loại nhiệm vụ và cách dựng nhiệm vụ
- 9.4 — Chuỗi nhiệm vụ, phụ thuộc và tiến trình
- 9.5 — Trạng thái nhiệm vụ, mục tiêu và cách nhiệm vụ diễn ra khi chơi
- 9.6 — Phần thưởng, hệ quả và thay đổi trạng thái thế giới

9.7 nối những hệ thống đó với thế giới có thể chơi thực tế.

Mô hình cốt lõi là:

```text
NHIỆM VỤ
  ↓
Ý ĐỊNH NGƯỜI CHƠI
  ↓
ĐỊA ĐIỂM / KHÔNG GIAN CHƠI
  ↓
TRẢI NGHIỆM KHÔNG GIAN
  ↓
HÀNH ĐỘNG NGƯỜI CHƠI
  ↓
THAY ĐỔI TRẠNG THÁI THẾ GIỚI
  ↓
THAY ĐỔI TRẠNG THÁI KHÔNG GIAN CHƠI
  ↓
KHẢ NĂNG MỚI
```

Nguyên tắc trung tâm là:

> **Một không gian chơi không chỉ là nơi một nhiệm vụ diễn ra. Đó là một phần có trạng thái của thế giới, có thể thay đổi vì hành động của người chơi.**

---

# 1. Nhiệm vụ và không gian chơi là hai thứ khác nhau

Một nhiệm vụ là:

> **Một cấu trúc tự sự/cách chơi do người chơi dẫn dắt.**

Một không gian chơi là:

> **Một môi trường không gian có thể chơi.**

Một trạng thái thế giới là:

> **Điều hiện đang đúng về môi trường đó và các thực thể bên trong.**

Vì vậy:

```text
Nhiệm vụ ≠ Không gian chơi
Không gian chơi ≠ Trạng thái thế giới
Trạng thái thế giới ≠ Trạng thái nhiệm vụ
```

Chúng tương tác với nhau, nhưng phải vẫn là các hệ thống tách biệt.

---

# 2. Quan hệ chuẩn

Quan hệ là:

```text
NHIỆM VỤ
   │
   ├── đòi hỏi → ĐỊA ĐIỂM
   │
   ├── kích hoạt → MỤC TIÊU
   │
   ├── thay đổi → TRẠNG THÁI THẾ GIỚI
   │
   └── tạo ra → KHẢ NĂNG MỚI

ĐỊA ĐIỂM
   │
   ├── phơi bày → TƯƠNG TÁC
   ├── chứa → NPC / VẬT THỂ / MANH MỐI
   └── phản ánh → TRẠNG THÁI THẾ GIỚI
```

Không gian chơi vì vậy là phương tiện mà qua đó người chơi trải nghiệm nhiệm vụ.

---

# 3. Địa điểm và không gian chơi

Với Veyloria, các khái niệm này cũng cần được phân biệt.

## Địa điểm

Một nơi bền vững trong thế giới.

Ví dụ:

- khu định cư;
- ngôi nhà;
- khu rừng;
- con đường;
- đền thờ;
- xưởng.

## Không gian chơi

Một biểu diễn không gian có thể chơi của một địa điểm, hoặc của một nhóm địa điểm.

Vì vậy:

```text
Địa điểm trong thế giới
      ↓
Biểu diễn không gian chơi
```

Một địa điểm có thể có:

- một không gian chơi;
- nhiều không gian chơi;
- nhiều trạng thái;
- nhiều cấu hình di chuyển.

---

# 4. Trạng thái địa điểm

Một địa điểm cần có trạng thái bền vững.

Ví dụ:

```text
OLD_HOUSE

Trạng thái:
    ownership = UNKNOWN
    door = LOCKED
    interior_access = FALSE
    investigated = FALSE
    occupant = NONE
```

Sau hành động của người chơi:

```text
OLD_HOUSE

Trạng thái:
    ownership = KNOWN
    door = OPEN
    interior_access = TRUE
    investigated = TRUE
    occupant = MARIA
```

Người chơi không còn bước vào cùng một nơi như trước.

---

# 5. Trạng thái không gian chơi

Trạng thái không gian chơi mô tả hiện thân có thể chơi của trạng thái thế giới.

Ví dụ:

- cửa mở/đóng;
- NPC có mặt/vắng mặt;
- vật thể bị phá hủy/đã sửa;
- ánh sáng thay đổi;
- đạo cụ thay đổi;
- tương tác sẵn có;
- tuyến di chuyển thay đổi;
- cuộc gặp thay đổi;
- đối thoại bị đổi.

Vì vậy:

> **Trạng thái không gian chơi là hình chiếu của trạng thái thế giới chuẩn.**

---

# 6. Trạng thái chuẩn

Không gian chơi không nên tự quyết định điều gì là đúng.

Ví dụ:

Kém:

```text
HouseDoor.open = true
```

chỉ được lưu bên trong không gian chơi.

Tốt hơn:

```text
WorldState.house.door = OPEN
```

Không gian chơi đọc trạng thái đó.

Cách này ngăn sự không nhất quán giữa:

- chuyển cảnh;
- lưu/tải;
- nhiệm vụ;
- hệ thống NPC;
- đối thoại.

---

# 7. Ánh xạ Nhiệm vụ → Địa điểm

Mọi nhiệm vụ cần xác định những địa điểm mà nó dùng.

Về khái niệm:

```text
Nhiệm vụ
 ├── Địa điểm chính
 ├── Địa điểm phụ
 └── Tham chiếu từ xa
```

Ví dụ:

```text
QUEST_HOUSE_INVESTIGATION

Chính:
    Old House

Phụ:
    Settlement

Từ xa:
    Forest Road
```

Địa điểm chính chứa trải nghiệm chơi chủ yếu.

---

# 8. Vai trò của địa điểm trong một nhiệm vụ

Một địa điểm có thể đảm nhận các vai trò khác nhau.

### Nguồn

Cung cấp thông tin.

### Không gian mục tiêu

Chứa thứ mà người chơi phải tương tác.

### Không gian điều tra

Chứa manh mối.

### Không gian quan hệ

Chủ trì các tương tác xã hội.

### Không gian chuyển tiếp

Nối các địa điểm khác.

### Không gian hệ quả

Cho thấy kết quả của những hành động trước.

### Không gian quay lại

Thay đổi theo thời gian và hé lộ ý nghĩa mới.

Một địa điểm có thể đảm nhận nhiều vai trò.

---

# 9. Ngữ pháp nhiệm vụ theo không gian

Ngữ pháp nhiệm vụ từ 9.3 cần có một tương đương theo không gian.

Ví dụ:

```text
CÂU HỎI
   ↓
VÀO KHÔNG GIAN
   ↓
ĐỊNH HƯỚNG
   ↓
THÁM HIỂM
   ↓
TƯƠNG TÁC
   ↓
KHÁM PHÁ
   ↓
HIỂU LẠI KHÔNG GIAN
   ↓
LỰA CHỌN
   ↓
RỜI ĐI / THAY ĐỔI KHÔNG GIAN
```

Điều này tạo quan hệ giữa:

> **Khám phá tự sự**

và

> **Khám phá không gian.**

---

# 10. Không gian như thông tin

Môi trường cần truyền thông tin mà không đòi hỏi đối thoại nói thẳng.

Ví dụ:

- đồ nội thất bị bỏ lại;
- vật thể hư hại;
- dấu vết hoạt động;
- phòng bị khóa;
- vị trí NPC đã đổi;
- dấu hiệu môi trường.

Người chơi vì vậy có thể điều tra bằng cách:

> **Đọc không gian.**

---

# 11. Không gian chơi như bằng chứng tự sự

Một địa điểm có thể hoạt động như bằng chứng.

Ví dụ:

Người chơi bước vào một ngôi nhà.

Họ quan sát:

- hai cái cốc;
- một phòng ngủ không dùng;
- một cửa sổ vừa được sửa;
- một bức ảnh giấu kín.

Không NPC nào cần giải thích mọi thứ.

Môi trường tạo ra câu hỏi:

> **Thực sự ai đã sống ở đây?**

Điều này hỗ trợ cách chơi hướng tới điều tra.

---

# 12. Câu hỏi không gian

Mọi địa điểm nhiệm vụ quan trọng cần có một câu hỏi không gian.

Ví dụ:

> Chuyện gì đã xảy ra ở đây?

> Thứ gì đang bị giấu ở đây?

> Vì sao nơi này bị bỏ hoang?

> Ai thuộc về nơi này?

> Điều gì đã đổi kể từ lần ghé trước?

Địa điểm cần giúp trả lời câu hỏi đó thông qua cách chơi.

---

# 13. Ý định người chơi và không gian

Cùng một địa điểm có thể hỗ trợ các ý định người chơi khác nhau.

Ví dụ:

```text
OLD_HOUSE
```

có thể hỗ trợ:

- điều tra;
- quan hệ;
- thám hiểm;
- ký ức;
- quay lại;
- thay đổi thế giới.

Vì vậy:

> **Một địa điểm không nên được soạn chỉ xoay quanh một nhiệm vụ.**

---

# 14. Địa điểm dùng lại được

Các địa điểm quan trọng cần hỗ trợ nhiều trạng thái và nhiều cuộc gặp.

Ví dụ:

```text
Settlement Square
```

có thể hỗ trợ:

- lần đến đầu tiên;
- đời sống thường nhật;
- điều tra;
- lễ hội;
- xung đột;
- hậu quả;
- hồi kết.

Điều này khiến thế giới có cảm giác bền vững.

---

# 15. Vòng đời địa điểm

Một địa điểm có thể tiến hóa qua:

```text
INTRODUCED
   ↓
DISCOVERED
   ↓
ACTIVE
   ↓
CHANGED
   ↓
REVISITED
   ↓
RECONTEXTUALIZED
```

Không phải mọi địa điểm đều cần đủ các trạng thái.

---

# 16. Trước / Trong khi / Sau

Mọi địa điểm quan trọng cần được xem xét ở ít nhất ba trạng thái.

### TRƯỚC

Người chơi gặp gì lúc ban đầu?

### TRONG KHI

Điều gì thay đổi khi nhiệm vụ đang hoạt động?

### SAU

Điều gì còn lại sau khi nhiệm vụ được giải quyết?

Ví dụ:

```text
Bridge

TRƯỚC:
Gãy

TRONG KHI:
Đang sửa

SAU:
Mở
```

---

# 17. Chuyển trạng thái địa điểm

Về khái niệm:

```text
LOCATION_STATE_A
      ↓
HÀNH ĐỘNG NGƯỜI CHƠI
      ↓
HỆ QUẢ NHIỆM VỤ
      ↓
THAY ĐỔI TRẠNG THÁI THẾ GIỚI
      ↓
LOCATION_STATE_B
```

Đây là phần tích hợp cốt lõi.

---

# 18. Thay đổi không gian chơi bền vững

Khi phù hợp, không gian chơi cần phản ánh bằng hình ảnh các thay đổi trạng thái.

Ví dụ:

- công trình đã sửa;
- cửa đã mở;
- NPC chuyển vào ở;
- vật thể mới;
- chướng ngại đã được dỡ;
- hoạt động thay đổi;
- bầu không khí thay đổi.

Người chơi cần thấy bằng chứng về hành động của mình.

---

# 19. Biến thể không gian chơi

Một địa điểm có thể có nhiều biến thể được soạn sẵn.

Ví dụ:

```text
Settlement
 ├── Settlement_Normal
 ├── Settlement_AfterConflict
 ├── Settlement_Rebuilt
 └── Settlement_Epilogue
```

Lúc chạy, hệ thống chọn biểu diễn đúng từ trạng thái thế giới.

Điều này không nhất thiết có nghĩa là các không gian chơi hoàn chỉnh tách riêng.

Các biến thể có thể được lắp ráp động.

---

# 20. Lắp ráp theo trạng thái

Về khái niệm:

```text
Trạng thái thế giới
    ↓
Trạng thái địa điểm
    ↓
Cấu hình không gian chơi
    ↓
NPC đang hoạt động
    ↓
Đạo cụ đang hoạt động
    ↓
Tương tác
    ↓
Không gian có thể chơi
```

Cách này khiến không gian chơi đáp lại thế giới.

---

# 21. Cổng không gian

Địa điểm có thể chứa cổng.

Ví dụ:

- cửa khóa;
- cầu sập;
- sự cho phép của NPC;
- thông tin còn thiếu;
- yêu cầu trạng thái thế giới.

Nhưng thứ bậc được ưu tiên vẫn là:

```text
Yêu cầu có ý nghĩa
        ↓
Hiểu biết / Quan hệ / Trạng thái thế giới
        ↓
Lối vào địa điểm
```

thay vì:

```text
YÊU CẦU CẤP 12
```

trừ khi trò chơi đặc biệt cần tiến trình bằng số.

---

# 22. Không gian bị chặn bởi hiểu biết

Ví dụ:

Người chơi không thể nhận ra một lối vào ẩn cho đến khi họ biết về nó.

```text
knowledge.hidden_entrance = FALSE
        ↓
Lối vào không thể được khám phá một cách có ý nghĩa
```

Sau khi khám phá manh mối:

```text
knowledge.hidden_entrance = TRUE
        ↓
Tương tác với lối vào trở nên sẵn có
```

Thế giới không thay đổi một cách kỳ diệu.

Khả năng nhận biết của người chơi đã thay đổi.

---

# 23. Không gian bị chặn bởi quan hệ

Ví dụ:

Một NPC từ chối lối vào.

Sau khi lòng tin tăng:

```text
relationship.maria.trust = HIGH
        ↓
NPC cấp lối vào
        ↓
Khu vực mới sẵn có
```

Cổng này mang tính xã hội, không mang tính cơ chế thuần túy.

---

# 24. Không gian bị chặn bởi trạng thái thế giới

Ví dụ:

```text
bridge.state = BROKEN
```

Người chơi sửa nó:

```text
bridge.state = REPAIRED
```

Khi đó:

```text
travel.route = OPEN
```

Đây là một cổng trạng thái thế giới.

---

# 25. Hệ quả không gian

Một nhiệm vụ có thể sửa đổi việc di chuyển.

Ví dụ:

```text
Nhiệm vụ:
Dọn đường bị chặn

Kết quả:
road.status = OPEN
```

Điều này thay đổi:

- điều hướng;
- thời gian di chuyển;
- các địa điểm sẵn có;
- các khả năng gặp gỡ.

Hệ quả trở thành hệ thống, không chỉ là bề mặt.

---

# 26. Nhiệm vụ và di chuyển

Bản thân việc di chuyển có thể truyền đạt tiến trình.

Trước:

> Một lối đi bị chặn.

Sau:

> Người chơi có thể băng qua.

Không cần điểm đánh dấu nhiệm vụ.

Thế giới nói với người chơi:

> Có điều gì đó đã thay đổi.

---

# 27. Trạng thái không gian chơi và trạng thái nhiệm vụ

Các trạng thái này phải vẫn tách biệt.

Ví dụ:

```text
Nhiệm vụ:
BRIDGE_REPAIR = COMPLETED

Thế giới:
bridge = REPAIRED
```

Nhiệm vụ ghi lại:

> Người chơi đã hoàn thành nhiệm vụ sửa chữa.

Thế giới ghi lại:

> Cầu đã được sửa.

Nhờ đó các hệ thống khác có thể quan tâm đến cây cầu mà không cần biết gì về nhiệm vụ gốc.

---

# 28. Nhiều nguyên nhân

Một trạng thái thế giới không nhất thiết phải phụ thuộc vào một nhiệm vụ.

Ví dụ:

```text
bridge = REPAIRED
```

có thể đạt được bằng cách:

- tự tay sửa;
- nhờ thợ;
- thuyết phục Settlement;
- khám phá một giải pháp khác.

Trạng thái thế giới quan tâm đến:

> **Điều gì là đúng**

không phải:

> **Nhiệm vụ nào đã gây ra điều đó.**

---

# 29. Giải pháp thay thế

Khi có thể:

```text
MỤC TIÊU:
Mở tuyến đường

Các giải pháp có thể:
A. Sửa cầu
B. Tìm đường khác
C. Thuyết phục NPC cung cấp thuyền
```

Tất cả đều có thể dẫn tới:

```text
route_to_region = AVAILABLE
```

nhưng với các hệ quả khác nhau.

---

# 30. Giải pháp và hệ quả

Hai người chơi có thể đạt cùng một mục tiêu trước mắt bằng các phương pháp khác nhau.

Thế giới kết quả vẫn có thể khác nhau.

Ví dụ:

```text
Sửa cầu:
settlement.trust = +1

Dùng thuyền:
merchant.relationship = +1

Ép lối vào:
settlement.trust = -1
```

Hệ thống giữ quyền tác giả của người chơi.

---

# 31. Mục tiêu không gian chơi

Mục tiêu cần có ý nghĩa về không gian.

Kém:

> “Đi tới điểm đánh dấu.”

Tốt hơn:

> “Tìm xem âm thanh phát ra từ đâu.”

Không gian chơi cung cấp trải nghiệm thực sự cần có để thỏa mục tiêu.

---

# 32. Mục tiêu không gian chơi như khám phá

Đôi khi mục tiêu cần là:

> Khám phá câu trả lời.

thay vì:

> Đi tới tọa độ chính xác.

Điều này đặc biệt quan trọng với:

- Điều tra;
- Thám hiểm;
- Ký ức;
- Quay lại.

---

# 33. Hướng dẫn không gian

Veyloria cần dùng hướng dẫn theo bậc.

### Mức 0 — Không hướng dẫn

Người chơi phải quan sát và suy ra.

### Mức 1 — Manh mối theo ngữ cảnh

Đối thoại hoặc gợi ý từ môi trường.

### Mức 2 — Hướng rộng

Khu lân cận / mốc địa hình.

### Mức 3 — Điểm đánh dấu mềm

Mục tiêu chung.

### Mức 4 — Điểm đánh dấu hiện rõ

Vị trí chính xác.

Hệ thống cần dùng mức thấp nhất vừa đủ.

---

# 34. Nguyên tắc chống GPS

Đừng tự động biến mọi nhiệm vụ thành:

```text
ĐI TỚI ĐÂY
↓
NHẤN NÚT
↓
QUAY VỀ
```

Cách này phá hủy:

- thám hiểm;
- suy luận;
- kể chuyện bằng môi trường;
- quyền chủ động của người chơi.

Thế giới thường cần trả lời:

> **Tôi nên đi đâu?**

bằng thông tin theo ngữ cảnh.

---

# 35. Khám phá không gian

Khám phá có thể xảy ra qua:

- mốc địa hình;
- âm thanh;
- hành vi NPC;
- manh mối môi trường;
- các địa điểm đã biết từ trước;
- bản đồ;
- ký ức;
- đối thoại;
- quan sát.

Các loại nhiệm vụ khác nhau có thể ưu tiên các kênh khám phá khác nhau.

---

# 36. Không gian điều tra

Không gian chơi điều tra cần hỗ trợ:

- nhiều nguồn bằng chứng;
- thông tin không đầy đủ;
- quan sát mơ hồ;
- quay lại;
- các cách diễn giải thay thế.

Người chơi không nhất thiết phải biết:

> Vật nào là manh mối đúng.

---

# 37. Không gian quan hệ

Nhiệm vụ quan hệ cần:

- ngữ cảnh xã hội phù hợp;
- không gian riêng tư/công cộng;
- lịch trình NPC;
- khả năng bị ngắt;
- đối thoại phụ thuộc trạng thái.

Bản thân không gian có thể ảnh hưởng cuộc trò chuyện.

Ví dụ:

Một cuộc trò chuyện riêng tư có thể hé lộ thông tin không thể chia sẻ công khai.

---

# 38. Không gian đời sống thường nhật

Nhiệm vụ đời sống thường nhật cần dùng:

- các thói quen lặp lại;
- các địa điểm quen thuộc;
- các tương tác nhỏ;
- tính liên tục của môi trường.

Cùng một không gian cần trở nên có ý nghĩa hơn nhờ sự quen thuộc.

---

# 39. Không gian ký ức

Nhiệm vụ ký ức cần khai thác:

- mốc địa hình quen thuộc;
- địa điểm đã đổi;
- sự vắng mặt;
- sự lặp lại;
- tiếng vọng hình ảnh.

Người chơi so sánh:

> **Điều đã từng là**

với:

> **Điều đang là.**

---

# 40. Không gian quay lại

Quay lại là một trong những cách dùng mạnh nhất của trạng thái không gian chơi bền vững.

Ví dụ:

### Lần ghé thứ nhất

Ngôi nhà bị bỏ hoang.

### Lần ghé thứ hai

Có người đã trở về.

### Lần ghé thứ ba

Người chơi khám phá ra vì sao.

Không gian vật lý trở thành một dòng thời gian tự sự.

---

# 41. Trạng thái không gian chơi như dòng thời gian

Một địa điểm có thể đại diện cho lịch sử tích lũy.

```text
TRẠNG THÁI QUÁ KHỨ
    ↓
HÀNH ĐỘNG NGƯỜI CHƠI
    ↓
TRẠNG THÁI MỚI
    ↓
THỜI GIAN TRÔI QUA
    ↓
MỘT TRẠNG THÁI KHÁC
```

Người chơi trải nghiệm lịch sử theo không gian.

---

# 42. Trạng thái không gian của NPC

NPC không nên bị gắn vĩnh viễn vào điểm đánh dấu nhiệm vụ.

Trạng thái của họ có thể quyết định:

- họ ở đâu;
- khi nào họ xuất hiện;
- họ ở cùng ai;
- họ đang làm gì;
- họ sẵn sàng bàn chuyện gì.

Ví dụ:

```text
NPC:
Maria

Bình thường:
Settlement

Sau xung đột:
Old House

Sau hòa giải:
Workshop
```

Địa điểm trở thành một phần trạng thái nhân vật.

---

# 43. Trạng thái xã hội theo không gian

Thế giới cần phản ánh các thay đổi xã hội.

Ví dụ:

- NPC tụ họp theo cách khác;
- một số người tránh nhau;
- một địa điểm trước đây công cộng trở thành riêng tư;
- lễ ăn mừng diễn ra;
- tang tóc diễn ra.

Đây là các hệ quả nhìn thấy được qua không gian.

---

# 44. Trạng thái môi trường

Trạng thái môi trường có thể gồm:

- thời tiết;
- ánh sáng;
- hư hại;
- vật thể;
- thảm thực vật;
- xây dựng;
- hoạt động;
- dân số;
- cảnh âm.

Những yếu tố này cần được dùng có chọn lọc.

Mục tiêu không phải là cảnh tượng thị giác.

Mục tiêu là:

> **Trạng thái thế giới có thể đọc được.**

---

# 45. Thứ tự ưu tiên trạng thái không gian chơi

Khi thay đổi một không gian chơi sau một nhiệm vụ, ưu tiên:

1. Mức liên quan tới cách chơi
2. Khả năng đọc được của tự sự
3. Quan hệ nhân quả với người chơi
4. Tính liên tục của môi trường
5. Độ bóng thị giác

Một thay đổi nhỏ có ý nghĩa tốt hơn một thay đổi lớn chỉ để trang trí.

---

# 46. Hợp đồng Nhiệm vụ → Không gian chơi

Mỗi nhiệm vụ tương tác với một địa điểm cần xác định:

```text
ID nhiệm vụ
ID địa điểm
Trạng thái vào
Tương tác bắt buộc
Nhân vật liên quan
Vật thể liên quan
Điều kiện không gian
Thay đổi trạng thái dự kiến
Trạng thái ra
Trạng thái quay lại
```

Điều này tạo một hợp đồng chính thức giữa thiết kế nhiệm vụ và thiết kế không gian chơi.

---

# 47. Ví dụ hợp đồng nhiệm vụ–không gian chơi

```text
NHIỆM VỤ:
HOUSE_INVESTIGATION

ĐỊA ĐIỂM:
OLD_HOUSE

TRẠNG THÁI VÀO:
bỏ hoang
khóa
trống

TƯƠNG TÁC:
ảnh
bàn
phòng ẩn

KHÁM PHÁ:
house_history

HỆ QUẢ:
house.relevance = HIGH

TRẠNG THÁI RA:
người chơi biết lịch sử ngôi nhà

QUAY LẠI:
NPC có thể xuất hiện
```

---

# 48. Hợp đồng trạng thái không gian chơi

Không gian chơi cần xác định:

```text
ĐỊA ĐIỂM:
OLD_HOUSE

TRẠNG THÁI THẾ GIỚI:
LOCKED
OPEN
OCCUPIED
ABANDONED
REVEALED

THAY ĐỔI HÌNH ẢNH:
cửa
đạo cụ
NPC
ánh sáng

THAY ĐỔI TƯƠNG TÁC:
bàn
ảnh
phòng ẩn

PHẢN ỨNG NHIỆM VỤ:
HOUSE_INVESTIGATION
HOUSE_REVISIT
```

---

# 49. Tải không gian chơi theo trạng thái

Về khái niệm:

```text
Vào địa điểm
      ↓
Đọc trạng thái thế giới
      ↓
Xác định trạng thái địa điểm
      ↓
Tải cấu hình phù hợp
      ↓
Sinh nhân vật / đạo cụ liên quan
      ↓
Đăng ký tương tác
      ↓
Kích hoạt nội dung phụ thuộc trạng thái
```

Người chơi thấy đúng phiên bản của thế giới.

---

# 50. Tải luồng và lưu bền

Nếu một địa điểm bị dỡ khỏi bộ nhớ:

```text
TRẠNG THÁI ĐỊA ĐIỂM
```

phải vẫn được lưu bền.

Khi vào lại:

```text
Trạng thái đã lưu
      ↓
Dựng lại địa điểm
```

Không gian chơi không được đặt lại chỉ vì người chơi đã rời đi.

---

# 51. Quyền sở hữu trạng thái địa điểm

Mỗi biến trạng thái địa điểm cần có một chủ sở hữu rõ ràng.

Ví dụ:

```text
house.door
→ Trạng thái thế giới

maria.location
→ Hệ thống NPC

house.investigated
→ Trạng thái nhiệm vụ / hiểu biết

house.visual_variant
→ Trình bày không gian chơi
```

Trình bày được suy ra từ trạng thái.

---

# 52. Biến thể không gian chơi và trạng thái động

Dùng một biến thể không gian chơi tĩnh khi:

- thay đổi kiến trúc lớn;
- phá hủy quy mô lớn;
- dịch chuyển dân số lớn;
- bố cục không gian khác về căn bản.

Dùng trạng thái động khi:

- cửa;
- vật thể;
- NPC;
- đối thoại;
- tương tác;
- thay đổi môi trường nhỏ.

Cách này tránh nhân bản không gian chơi không cần thiết.

---

# 53. Biến đổi không gian chơi do nhiệm vụ dẫn dắt

Một nhiệm vụ có thể biến đổi một không gian chơi.

Ví dụ:

```text
NHIỆM VỤ:
Khôi phục Workshop

Trước:
hư hại
đóng
trống

Sau:
đã sửa
mở
có người ở
```

Sự biến đổi cần tồn tại sau khi nhiệm vụ kết thúc.

---

# 54. Kích hoạt nhiệm vụ do trạng thái thế giới dẫn dắt

Chiều ngược lại cũng quan trọng không kém.

Một thay đổi không gian chơi có thể tạo ra nhiệm vụ.

Ví dụ:

```text
Cầu đã được sửa
     ↓
Thương nhân trở lại
     ↓
Nhiệm vụ liên quan thương nhân trở nên sẵn có
```

Vì vậy:

> **Nhiệm vụ thay đổi thế giới; thế giới tạo ra nhiệm vụ.**

Điều này tạo một vòng phản hồi.

---

# 55. Vòng phản hồi chuẩn

```text
NHIỆM VỤ
  ↓
HÀNH ĐỘNG
  ↓
TRẠNG THÁI THẾ GIỚI
  ↓
TRẠNG THÁI KHÔNG GIAN CHƠI
  ↓
PHẢN HỒI CỦA NPC / MÔI TRƯỜNG
  ↓
QUAN SÁT CỦA NGƯỜI CHƠI
  ↓
CÂU HỎI MỚI
  ↓
NHIỆM VỤ MỚI
```

Đây là vòng hệ thống cốt lõi của Bước 9.

---

# 56. Thế giới như máy sinh nhiệm vụ

Không phải mọi nhiệm vụ đều phải được sinh từ người giao nhiệm vụ.

Một thế giới đã đổi có thể sinh nhiệm vụ tiếp theo.

Ví dụ:

```text
Người chơi sửa cầu
       ↓
Quay lại sau
       ↓
Thấy hoạt động của thương nhân
       ↓
Nghe cuộc trò chuyện mới
       ↓
Khám phá vấn đề mới
       ↓
Nhiệm vụ mới nảy sinh
```

Người chơi trải nghiệm quan hệ nhân quả một cách tự nhiên.

---

# 57. Nhiệm vụ nảy sinh

Một nhiệm vụ vì vậy có thể bắt nguồn từ:

- NPC;
- địa điểm;
- thay đổi thế giới;
- hiểu biết;
- quan hệ;
- quay lại;
- sự tò mò của người chơi.

Điều này mở rộng vượt khỏi:

> **NPC mang dấu chấm than.**

---

# 58. Địa điểm như trung tâm bền vững

Một số địa điểm cần đóng vai trung tâm tự sự.

Ví dụ:

```text
SETTLEMENT
 ├── NPC
 ├── Cửa hàng
 ├── Nhà
 ├── Sự kiện xã hội
 ├── Nhiệm vụ
 ├── Tin đồn
 └── Thay đổi trạng thái thế giới
```

Trung tâm tiến hóa khi người chơi thay đổi thế giới.

---

# 59. Tiến hóa trung tâm

Một trung tâm có thể tiến qua các trạng thái:

```text
SETTLEMENT
   ↓
GIỚI THIỆU
   ↓
QUEN THUỘC
   ↓
BỊ PHÁ VỠ
   ↓
ĐÃ ĐỔI
   ↓
ĐANG HỒI PHỤC
   ↓
ĐANG NHỚ LẠI
```

Trải nghiệm của người chơi về cùng một nơi tiến hóa.

---

# 60. Mật độ nhiệm vụ

Đừng chất quá tải nhiệm vụ lên mọi địa điểm.

Mỗi địa điểm cần có mật độ nội dung có chủ đích.

Các vai trò có thể:

- trung tâm tự sự chính;
- trung tâm phụ;
- địa điểm điều tra;
- không gian di chuyển;
- không gian tĩnh để suy ngẫm;
- không gian chuyển tiếp.

Sự im lặng cũng là nội dung.

---

# 61. Không gian trống

Không phải mọi không gian đều cần:

- nhiệm vụ;
- vật sưu tầm;
- NPC;
- mục tiêu.

Một số không gian tồn tại để:

- tạo bầu không khí;
- di chuyển;
- suy ngẫm;
- giữ nhịp;
- kể chuyện bằng môi trường.

Điều này bảo vệ thế giới khỏi cảm giác như một công viên giải trí.

---

# 62. Nhịp nhiệm vụ qua không gian

Thiết kế không gian chơi có thể điều khiển nhịp tự sự.

Ví dụ:

```text
KHÔNG GIAN XÃ HỘI
   ↓
DI CHUYỂN
   ↓
THÁM HIỂM TĨNH
   ↓
KHÁM PHÁ
   ↓
ĐỐI ĐẦU
   ↓
SUY NGẪM
```

Thiết kế nhiệm vụ và nhịp không gian chơi vì vậy cần được thiết kế cùng nhau.

---

# 63. Tương phản không gian

Một thế giới có cảm giác sống hơn khi các trạng thái tương phản.

Ví dụ:

```text
Trước:
khu định cư yên tĩnh

Sau:
khu định cư nhộn nhịp
```

hoặc:

```text
Trước:
ngôi nhà ấm

Sau:
ngôi nhà trống
```

Các thay đổi cần củng cố ý nghĩa cảm xúc.

---

# 64. Ký ức không gian

Một địa điểm mạnh cần nhận ra được qua:

- bố cục;
- mốc địa hình;
- vật thể;
- âm thanh;
- thói quen NPC;
- bầu không khí.

Khi người chơi quay lại, họ cần nghĩ:

> **“Mình nhớ nơi này.”**

Điều này tạo ký ức không gian.

---

# 65. Hiểu lại theo không gian

Một địa điểm quen thuộc có thể trở nên khác về cảm xúc mà gần như không đổi về vật lý.

Ví dụ:

Lần ghé đầu:

> Một ngôi nhà gia đình bình thường.

Sau này:

> Nơi người chơi biết được bí mật của gia đình.

Cùng một hình học.

Ý nghĩa khác.

Đây là thiết kế tự sự rất hiệu quả.

---

# 66. Trạng thái không gian chơi và sự thật tự sự

Môi trường đôi khi có thể hé lộ nhiều hơn đối thoại.

Ví dụ:

NPC nói:

> “Không ai sống ở đây nhiều năm rồi.”

Nhưng người chơi nhận thấy:

- thức ăn còn tươi;
- lò sưởi còn ấm;
- đồ đạc vừa được dịch chuyển.

Không gian chơi tạo ra mâu thuẫn.

Mâu thuẫn này trở thành yếu tố kích hoạt nhiệm vụ.

---

# 67. Mâu thuẫn môi trường

Mâu thuẫn môi trường là công cụ điều tra mạnh.

```text
Phát biểu của NPC
      ↓
Quan sát của người chơi
      ↓
Mâu thuẫn
      ↓
Câu hỏi
      ↓
Điều tra
```

Cách này biến thiết kế không gian chơi thành cách chơi chủ động.

---

# 68. Không gian chơi → Kích hoạt nhiệm vụ

Một tương tác trong không gian chơi có thể kích hoạt nhiệm vụ một cách hữu cơ.

Ví dụ:

```text
Người chơi nhận ra vật giấu kín
      ↓
Tương tác với vật
      ↓
Hiểu biết được khám phá
      ↓
Nhiệm vụ trở nên sẵn có
```

Không cần người giao nhiệm vụ.

---

# 69. Nhiệm vụ → Kích hoạt không gian chơi

Chiều ngược:

```text
Trạng thái nhiệm vụ thay đổi
      ↓
Trạng thái địa điểm thay đổi
      ↓
Không gian chơi cập nhật
```

Ví dụ:

```text
Nhiệm vụ:
Thuyết phục NPC trở về

Thành công
↓
NPC trở về Settlement
↓
NPC xuất hiện ở địa điểm mới
```

---

# 70. Phụ thuộc trạng thái không gian

Địa điểm có thể phụ thuộc vào:

- trạng thái nhiệm vụ;
- trạng thái thế giới;
- trạng thái NPC;
- thời gian/pha câu chuyện;
- hiểu biết;
- quan hệ.

Nhưng các phụ thuộc cần có ý nghĩa.

Tránh những thứ không cần thiết như:

```text
Nhiệm vụ 17 đã hoàn thành
VÀ
Nhiệm vụ 21 đã hoàn thành
VÀ
cấp người chơi > 12
```

khi yêu cầu tự sự thực sự chỉ là:

> Cây cầu đã được sửa.

---

# 71. Trừu tượng hóa trạng thái

Ưu tiên trạng thái ngữ nghĩa.

Kém:

```text
Quest_12_completed = TRUE
```

khi một hệ thống khác thực sự cần:

```text
bridge.repaired = TRUE
```

Tốt:

```text
bridge.repaired = TRUE
```

Trạng thái ngữ nghĩa dùng lại được.

---

# 72. Dùng lại xuyên hệ thống

Khi:

```text
bridge.repaired = TRUE
```

đã tồn tại, nhiều hệ thống có thể dùng nó.

### Hệ thống nhiệm vụ

Mở khóa nhiệm vụ thương nhân.

### Hệ thống NPC

Cho phép thương nhân di chuyển.

### Hệ thống không gian chơi

Mở tuyến đường.

### Hệ thống đối thoại

Cư dân nhắc tới việc sửa chữa.

### Mô phỏng thế giới

Lịch trình thương nhân tiếp tục.

Một trạng thái tạo sự mạch lạc hệ thống.

---

# 73. Đồ thị trạng thái

Thế giới có thể được hiểu như một đồ thị:

```text
TRẠNG THÁI THẾ GIỚI
   │
   ├── Settlement
   │     ├── Trạng thái NPC
   │     └── Trạng thái địa điểm
   │
   ├── Người chơi
   │     ├── Hiểu biết
   │     ├── Ký ức
   │     └── Lựa chọn
   │
   └── Tự sự
         ├── Trạng thái nhiệm vụ
         └── Trạng thái câu chuyện
```

Hành động của người chơi đưa thế giới đi qua đồ thị này.

---

# 74. Chuyển trạng thái thế giới

Chuyển chuẩn:

```text
TRẠNG THÁI HIỆN TẠI
      ↓
HÀNH ĐỘNG NGƯỜI CHƠI
      ↓
QUY TẮC / HỆ QUẢ
      ↓
TRẠNG THÁI MỚI
      ↓
KHÔNG GIAN CHƠI PHẢN ÁNH TRẠNG THÁI
      ↓
TƯƠNG TÁC MỚI
```

Đây là nền tảng cho tự sự hệ thống.

---

# 75. Kiểm thử tích hợp không gian chơi

Với mọi nhiệm vụ quan trọng:

### Vào

Người chơi thấy gì khi vào?

### Tương tác

Họ có thể làm gì?

### Khám phá

Họ có thể biết được gì?

### Thay đổi

Hành động của họ làm đổi điều gì?

### Ra

Trạng thái nào còn lại?

### Quay lại

Điều gì khác đi về sau?

Nếu các câu hỏi này có câu trả lời rõ, nhiệm vụ và không gian chơi đã được tích hợp đúng.

---

# 76. Kiểm thử tích hợp trạng thái thế giới

Với mọi hệ quả lớn:

1. Trạng thái chuẩn nào thay đổi?
2. Không gian chơi nào phản ánh nó?
3. NPC nào phản ánh nó?
4. Đối thoại nào phản ánh nó?
5. Nhiệm vụ nào phản ứng với nó?
6. Người chơi có quan sát được không?
7. Nó có tồn tại sau khi tải lại không?
8. Nó có tạo khả năng tương lai không?

---

# 77. Mẫu cần tránh giữa nhiệm vụ và không gian chơi

Tránh:

### Bong bóng nhiệm vụ

Nhiệm vụ xảy ra bên trong một địa điểm nhưng không bao giờ ảnh hưởng địa điểm đó.

### Không gian chơi dùng một lần

Địa điểm mất hết mức liên quan ngay sau khi nhiệm vụ hoàn thành.

### Thế giới tĩnh

Người chơi không đổi được điều gì có ý nghĩa.

### Thế giới điểm đánh dấu nhiệm vụ

Không gian chơi chỉ tồn tại để dẫn người chơi tới mục tiêu.

### Trạng thái trùng lặp

Nhiệm vụ và không gian chơi giữ các phiên bản mâu thuẫn của cùng một sự thật.

### Thế giới đặt lại

Trở lại một địa điểm sẽ khôi phục trạng thái ban đầu của nó.

---

# 78. Mô hình được ưu tiên

Thay vào đó:

```text
NHIỆM VỤ
 ↓
HÀNH ĐỘNG NGƯỜI CHƠI
 ↓
TRẠNG THÁI THẾ GIỚI
 ↓
PHẢN HỒI KHÔNG GIAN CHƠI
 ↓
QUAN SÁT CỦA NGƯỜI CHƠI
 ↓
CÂU HỎI MỚI
 ↓
NHIỆM VỤ MỚI
```

Cách này tạo một thế giới tự sự tự củng cố.

---

# 79. Ví dụ tích hợp đầy đủ

## Trạng thái ban đầu

```text
SETTLEMENT
bridge = BROKEN

OLD_HOUSE
abandoned = TRUE

MARIA
trust = LOW
location = SETTLEMENT
```

## Nhiệm vụ

> Điều tra vì sao Settlement tránh Old House.

Người chơi thám hiểm.

## Khám phá

```text
knowledge.house_history = TRUE
```

## Hệ quả

```text
maria.trust = +1
house.relevance = HIGH
```

## Hành động sau đó

Người chơi nói sự thật với Maria.

## Phản hồi của thế giới

```text
maria.trust = HIGH
maria.location = OLD_HOUSE
```

## Phản hồi của không gian chơi

Old House giờ có Maria.

Tương tác mới xuất hiện.

## Quay lại

Người chơi trở lại.

Cùng một không gian giờ có cảm giác khác.

## Nhiệm vụ mới

Maria hé lộ một câu hỏi mới.

Một nhiệm vụ mới nảy sinh.

Đây là vòng lặp Veyloria được nhắm tới.

---

# 80. Đường ống chuẩn Nhiệm vụ → Không gian chơi

```text
NHỊP CÂU CHUYỆN
    ↓
NHIỆM VỤ
    ↓
MỤC TIÊU NHIỆM VỤ
    ↓
YÊU CẦU ĐỊA ĐIỂM
    ↓
TRẢI NGHIỆM KHÔNG GIAN
    ↓
HÀNH ĐỘNG NGƯỜI CHƠI
    ↓
KẾT QUẢ NHIỆM VỤ
    ↓
THAY ĐỔI TRẠNG THÁI THẾ GIỚI
    ↓
THAY ĐỔI TRẠNG THÁI KHÔNG GIAN CHƠI
    ↓
PHẢN HỒI CỦA NPC / ĐỐI THOẠI / MÔI TRƯỜNG
    ↓
QUAN SÁT CỦA NGƯỜI CHƠI
    ↓
KHẢ NĂNG MỚI
```

---

# 81. Hợp đồng thiết kế không gian chơi

Với Bước 9, mọi không gian chơi quan trọng cuối cùng cần có:

```text
ID địa điểm
Mục đích
Liên kết nhiệm vụ
Trạng thái vào
Câu hỏi không gian
Nhân vật then chốt
Vật thể then chốt
Cơ hội khám phá
Điểm tương tác
Phụ thuộc trạng thái
Chuyển trạng thái
Trạng thái ra
Trạng thái quay lại
Hệ quả môi trường
Hệ quả tự sự
```

Đây trở thành cầu nối giữa thiết kế nhiệm vụ và sản xuất không gian chơi thực tế.

---

# 82. Tiêu chí hoàn thành 9.7

9.7 hoàn thành khi mọi nhiệm vụ lớn có thể trả lời:

1. Nó xảy ra ở đâu?
2. Vì sao nó xảy ra ở đó?
3. Không gian truyền đạt điều gì?
4. Người chơi có thể khám phá gì ở đó?
5. Người chơi có thể thay đổi gì?
6. Trạng thái chuẩn nào thay đổi?
7. Không gian chơi phản ánh thay đổi đó thế nào?
8. Chuyện gì xảy ra khi người chơi rời đi?
9. Chuyện gì xảy ra khi người chơi quay lại?
10. Những nhiệm vụ tương lai nào nảy sinh từ trạng thái đã đổi?

Phép thử cuối cùng là:

> **Nếu người chơi quay lại địa điểm này sau đó, họ có cảm được rằng những hành động trước của mình thực sự đã xảy ra ở đây không?**

Nếu có, nhiệm vụ và không gian chơi đã được tích hợp đúng.

---

# 83. Trạng thái Bước 9

Đã hoàn thành:

- **9.1 — Khung ánh xạ câu chuyện → cách chơi**
- **9.2 — Nhịp câu chuyện → cấu trúc nhiệm vụ**
- **9.3 — Loại nhiệm vụ và cách dựng nhiệm vụ**
- **9.4 — Chuỗi nhiệm vụ, phụ thuộc và tiến trình**
- **9.5 — Trạng thái nhiệm vụ, mục tiêu và cách nhiệm vụ diễn ra khi chơi**
- **9.6 — Phần thưởng, hệ quả và thay đổi trạng thái thế giới**
- **9.7 — Nhiệm vụ → Không gian chơi → Tích hợp trạng thái thế giới**

Bước tiếp theo cần nối các cấu trúc này với tiến trình người chơi.

## Tiếp theo

> **9.8 — Ánh xạ tiến trình: Câu chuyện → Nhiệm vụ → Không gian chơi → Tiến trình người chơi**
