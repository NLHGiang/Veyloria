# 9.5 — Trạng thái nhiệm vụ, mục tiêu và cách nhiệm vụ diễn ra khi chơi

## Mục đích

9.5 định nghĩa mô hình khi chơi cho nhiệm vụ trong Veyloria.

Mục đích là chuyển các cấu trúc nhiệm vụ khái niệm đã định nghĩa ở 9.3 và 9.4 thành một hệ thống có thể:

- được biểu diễn trong dữ liệu;
- được các hệ thống trò chơi đánh giá;
- được kích hoạt;
- được tiến triển;
- được tạm dừng;
- được phân nhánh;
- được hoàn thành;
- bị thất bại;
- được hiểu lại;
- được lưu bền;
- được các hệ thống khác truy vấn.

Nguyên tắc trung tâm là:

> **Nhiệm vụ là một máy trạng thái bền vững, được dẫn dắt bởi hành động của người chơi và trạng thái thế giới.**

Hệ thống nhiệm vụ không được trở thành một tập hợp cứng các chuỗi kịch bản.

---

# 1. Mô hình nhiệm vụ khi chơi

Lúc chạy, mọi nhiệm vụ tồn tại dưới dạng:

> **Định nghĩa + Trạng thái + Điều kiện + Mục tiêu + Hiệu ứng**

Về mặt khái niệm:

```text
Định nghĩa nhiệm vụ
      │
      ├── Điều kiện
      ├── Mục tiêu
      ├── Nhánh
      ├── Hiệu ứng
      └── Siêu dữ liệu
             │
             ↓
        Nhiệm vụ khi chơi
             │
             ├── Trạng thái hiện tại
             ├── Trạng thái mục tiêu
             ├── Tiến trình
             ├── Lựa chọn
             └── Hiệu ứng bền vững
```

---

# 2. Định nghĩa nhiệm vụ so với thể hiện nhiệm vụ

Hai thứ này phải được tách riêng.

## Định nghĩa nhiệm vụ

Dữ liệu thiết kế tĩnh.

Ví dụ:

> QUEST_HOUSE_001

chứa:

- tên;
- loại;
- cách dựng;
- mục tiêu;
- phụ thuộc;
- điều kiện;
- kết quả có thể.

## Thể hiện nhiệm vụ

Phiên bản khi chơi của nhiệm vụ đó đối với người chơi.

Chứa:

- trạng thái hiện tại;
- mục tiêu đang hoạt động;
- mục tiêu đã hoàn thành;
- lựa chọn đã chọn;
- bằng chứng đã khám phá;
- nhánh hiện tại;
- dấu thời gian;
- hệ quả.

Vì vậy:

> **Một Định nghĩa nhiệm vụ có thể tạo ra nhiều Trạng thái nhiệm vụ.**

---

# 3. Máy trạng thái nhiệm vụ chuẩn

Máy trạng thái khi chơi chính là:

```text
HIDDEN
   ↓
AVAILABLE
   ↓
DISCOVERED
   ↓
ACTIVE
   ↓
SUSPENDED
   ↓
ACTIVE
   ↓
COMPLETED
```

Các kết quả thay thế:

```text
ACTIVE → FAILED
ACTIVE → ABANDONED
ACTIVE → BLOCKED
```

Sau này:

```text
COMPLETED → RECONTEXTUALIZED
```

Không phải mọi nhiệm vụ đều cần mọi trạng thái.

---

# 4. HIDDEN

Nhiệm vụ tồn tại trong cơ sở dữ liệu nội dung nhưng không được phơi bày cho người chơi.

Lý do:

- phụ thuộc chưa được thỏa;
- thông tin chưa được khám phá;
- sự kiện tự sự chưa xảy ra;
- NPC chưa giới thiệu khả năng đó.

Ví dụ:

```text
QUEST_HOUSE_TRUTH
State = HIDDEN
```

Người chơi không biết nó tồn tại.

---

# 5. AVAILABLE

Các điều kiện của nhiệm vụ đã được thỏa.

Nhiệm vụ giờ có thể được khám phá.

Tuy nhiên:

> **AVAILABLE ≠ Người chơi biết về nó.**

Hệ thống có thể phơi bày nhiệm vụ qua:

- NPC;
- địa điểm;
- vật thể;
- sự kiện môi trường;
- nhiệm vụ trước;
- thông tin đã khám phá.

---

# 6. DISCOVERED

Người chơi đã nhận biết nhiệm vụ.

Điều này có thể xảy ra qua:

- hội thoại nói thẳng;
- quan sát;
- tương tác;
- bằng chứng;
- khám phá.

Khám phá nên có ý nghĩa.

Nhật ký nhiệm vụ giờ có thể chứa:

> “Có điều gì đó lạ về ngôi nhà cũ.”

thay vì:

> “Điều tra ngôi nhà cũ.”

Điều này cho phép sự không chắc chắn vẫn là một phần của trải nghiệm.

---

# 7. ACTIVE

Người chơi đã bước vào tiến trình hoạt động của nhiệm vụ.

Tại thời điểm này:

- mục tiêu có thể trở thành hoạt động;
- thay đổi trạng thái nhiệm vụ có thể được theo dõi;
- điều kiện có thể được đánh giá;
- tương tác có thể phản ứng với nhiệm vụ.

Một nhiệm vụ có thể có nhiều mục tiêu đang hoạt động.

---

# 8. SUSPENDED

Một nhiệm vụ có thể tạm dừng tiến triển mà không bị thất bại.

Ví dụ:

- NPC cần thiết không có mặt;
- người chơi rời khỏi một tình huống đang diễn ra;
- một sự kiện khác tạm thời được ưu tiên;
- trạng thái thế giới thay đổi.

Các nhiệm vụ bị tạm dừng giữ nguyên trạng thái của chúng.

---

# 9. COMPLETED

Nhiệm vụ đã đạt một kết thúc thành công hợp lệ.

Hoàn thành có thể kích hoạt:

- thay đổi trạng thái;
- thay đổi quan hệ;
- thay đổi thế giới;
- thay đổi hiểu biết;
- nhiệm vụ mới;
- hội thoại mới;
- hệ quả trong tương lai.

Vì vậy hoàn thành là một sự kiện:

> **Nhiệm vụ hoàn thành → Đột biến trạng thái**

không đơn thuần là:

> **Nhiệm vụ hoàn thành → Phần thưởng**

---

# 10. FAILED

Thất bại xảy ra khi:

> Kết thúc dự định của nhiệm vụ không còn có thể đạt được.

Thất bại phải được dùng thận trọng.

Bất cứ khi nào có thể:

> **Thất bại nên tạo ra một trạng thái mới thay vì xóa tiến trình.**

Ví dụ:

```text
NHIỆM VỤ: Thuyết phục NPC

Người chơi thất bại
      ↓
Sự ngờ vực của NPC tăng
      ↓
Một hướng điều tra thay thế trở thành khả dụng
```

---

# 11. ABANDONED

Bỏ dở nghĩa là:

> Người chơi cố ý ngừng theo đuổi nhiệm vụ.

Điều này khác với thất bại.

Một nhiệm vụ bị bỏ dở sau này có thể:

- được tiếp tục;
- hết hạn;
- thay đổi;
- trở thành không khả dụng;
- tạo ra hệ quả.

---

# 12. BLOCKED

Bị chặn nghĩa là:

> Nhiệm vụ hiện không thể tiến triển vì một phụ thuộc chưa được thỏa.

Ví dụ:

```text
ACTIVE
  ↓
NPC rời thị trấn
  ↓
BLOCKED
  ↓
NPC trở lại
  ↓
ACTIVE
```

Bị chặn không nên tự động có nghĩa là thất bại.

---

# 13. RECONTEXTUALIZED

Một nhiệm vụ đã hoàn thành sau này có thể nhận ý nghĩa mới.

Ví dụ:

```text
COMPLETED
     ↓
Thông tin mới
     ↓
RECONTEXTUALIZED
```

Trạng thái này đặc biệt quan trọng đối với:

- Nhiệm vụ ký ức;
- Nhiệm vụ điều tra;
- Nhiệm vụ quay lại;
- các cung câu chuyện liên quan đến danh tính.

Kết quả ban đầu không thay đổi.

Cách diễn giải kết quả đó thay đổi.

---

# 14. Mô hình mục tiêu

Một nhiệm vụ gồm một hoặc nhiều mục tiêu.

Một mục tiêu là:

> **Một điều kiện khi chơi mô tả điều người chơi hiện có thể hoàn thành.**

Một mục tiêu không nên lúc nào cũng được diễn đạt như một mục trong danh sách kiểm.

Ví dụ:

Thay vì:

> “Nói chuyện với Maria.”

Mục tiêu nội bộ có thể là:

> `npc.maria.dialogue.truth_available = true`

Biểu diễn hướng tới người chơi có thể vẫn là:

> “Tìm hiểu Maria biết gì.”

---

# 15. Máy trạng thái mục tiêu

Mục tiêu dùng:

```text
INACTIVE
   ↓
AVAILABLE
   ↓
ACTIVE
   ↓
COMPLETED
```

Các trạng thái thay thế:

```text
ACTIVE → FAILED
ACTIVE → SKIPPED
ACTIVE → BLOCKED
```

---

# 16. Loại mục tiêu

Các loại mục tiêu chuẩn:

1. Tương tác;
2. Điều tra;
3. Khám phá;
4. Quan sát;
5. Thu thập;
6. Giao nhận;
7. Hộ tống;
8. Địa điểm;
9. Hội thoại;
10. Lựa chọn;
11. Quan hệ;
12. Trạng thái thế giới;
13. Hiểu biết;
14. Quay lại;
15. Sự kiện;
16. Tổng hợp.

Đây là các hạng mục triển khai.

Chúng không định nghĩa Loại nhiệm vụ.

---

# 17. Mục tiêu so với loại nhiệm vụ

Ví dụ:

Loại nhiệm vụ:

> Điều tra

Các mục tiêu có thể là:

- Khám phá địa điểm;
- Xem xét vật thể;
- Nói chuyện với NPC;
- So sánh bằng chứng;
- Quay lại địa điểm.

Vì vậy:

> **Loại nhiệm vụ = trải nghiệm**

> **Loại mục tiêu = hành động/điều kiện khi chơi**

---

# 18. Hoàn thành mục tiêu

Một mục tiêu nên hoàn thành khi một điều kiện trở thành đúng.

Ví dụ:

```text
Điều kiện:
player.knowledge.knows_old_house_history == true
```

Khi đúng:

```text
Mục tiêu → COMPLETED
```

Cách này được ưu tiên hơn:

```text
DialogueNode42Finished == true
```

vì cách thứ nhất diễn đạt trạng thái trò chơi trong khi cách thứ hai diễn đạt chi tiết triển khai.

---

# 19. Điều kiện mục tiêu

Điều kiện có thể tham chiếu:

### Người chơi

- vị trí;
- túi đồ;
- năng lực;
- lựa chọn.

### Hiểu biết

- sự kiện đã khám phá;
- bằng chứng;
- ký ức;
- cách diễn giải.

### NPC

- quan hệ;
- sự có mặt;
- trạng thái;
- vị trí.

### Thế giới

- trạng thái địa điểm;
- trạng thái vật thể;
- trạng thái toàn cục.

### Nhiệm vụ

- trạng thái nhiệm vụ khác;
- trạng thái mục tiêu;
- trạng thái nhánh.

---

# 20. Logic điều kiện

Điều kiện nên hỗ trợ:

### AND

```text
A AND B
```

Cả hai đều bắt buộc.

### OR

```text
A OR B
```

Một trong hai đường đều hợp lệ.

### NOT

```text
NOT A
```

Điều kiện không được là đúng.

### Lồng nhau

```text
(A AND B) OR C
```

Mức này đủ cho hầu hết logic nhiệm vụ.

---

# 21. Ví dụ phụ thuộc

Một nhiệm vụ trở thành khả dụng khi:

```text
quest.intro.completed
AND
location.old_house.discovered
AND
knowledge.house_is_significant
```

Hệ thống nhiệm vụ đánh giá các điều kiện này.

Khi đúng:

> Nhiệm vụ trở thành AVAILABLE.

---

# 22. Logic nhiệm vụ theo sự kiện

Hệ thống nhiệm vụ nên phản ứng chủ yếu với các sự kiện.

Ví dụ:

```text
PlayerInspectedObject
PlayerEnteredLocation
DialogueCompleted
RelationshipChanged
KnowledgeDiscovered
WorldStateChanged
QuestCompleted
ChoiceMade
```

Hệ thống nhiệm vụ lắng nghe các sự kiện liên quan.

Sau đó hệ thống đánh giá các điều kiện bị ảnh hưởng.

Cách này được ưu tiên hơn việc liên tục kiểm tra mọi nhiệm vụ mỗi khung hình.

---

# 23. Sự kiện → Điều kiện → Trạng thái

Luồng khi chơi chuẩn:

```text
SỰ KIỆN TRÒ CHƠI
    ↓
THAY ĐỔI TRẠNG THÁI
    ↓
ĐÁNH GIÁ ĐIỀU KIỆN
    ↓
CẬP NHẬT MỤC TIÊU
    ↓
CẬP NHẬT TRẠNG THÁI NHIỆM VỤ
    ↓
SỰ KIỆN / HIỆU ỨNG MỚI
```

Ví dụ:

```text
Người chơi xem xét bức ảnh
        ↓
Bằng chứng được khám phá
        ↓
Trạng thái hiểu biết thay đổi
        ↓
Mục tiêu hoàn thành
        ↓
Nhiệm vụ tiến lên
        ↓
Mục tiêu mới được kích hoạt
```

---

# 24. Hiệu ứng nhiệm vụ

Một nhiệm vụ có thể tạo hiệu ứng khi trạng thái thay đổi.

Ví dụ:

- Đặt trạng thái thế giới;
- Sửa đổi quan hệ;
- Thêm hiểu biết;
- Mở khóa nhiệm vụ;
- Chặn nhiệm vụ;
- Thay đổi hành vi NPC;
- Thay đổi địa điểm;
- Thêm hội thoại;
- Kích hoạt sự kiện;
- Lên lịch quay lại;
- Ghi nhận ký ức.

Hiệu ứng nên được dẫn dắt bởi dữ liệu bất cứ khi nào có thể.

---

# 25. Đột biến trạng thái

Hoàn thành nhiệm vụ nên sửa đổi trạng thái trò chơi có thẩm quyền.

Ví dụ:

```text
Nhiệm vụ:
HELP_RESIDENT

Hiệu ứng hoàn thành:
resident.trust += meaningful_change
settlement.problem.resolved = true
knowledge.resident_secret = discovered
```

Các hệ thống khác sau đó phản ứng với các trạng thái này.

Điều này ngăn hệ thống nhiệm vụ sở hữu trực tiếp mọi hệ thống cách chơi.

---

# 26. Trách nhiệm của hệ thống nhiệm vụ

Hệ thống nhiệm vụ nên sở hữu:

- trạng thái nhiệm vụ;
- trạng thái mục tiêu;
- phụ thuộc;
- tiến trình;
- hiệu ứng nhiệm vụ;
- lịch sử nhiệm vụ;
- lưu bền nhiệm vụ.

Hệ thống không nên sở hữu:

- di chuyển của NPC;
- triển khai túi đồ;
- kết xuất hội thoại;
- kết xuất thế giới;
- trình bày quan hệ;
- hạ tầng lưu trò chơi.

Thay vào đó:

> **Hệ thống nhiệm vụ phát hành và tiêu thụ trạng thái/sự kiện.**

---

# 27. Nhiệm vụ ↔ Các hệ thống khác

Kiến trúc khái niệm:

```text
                         ┌─────────────────────┐
                         │ Hệ thống nhiệm vụ   │
                         └──────────┬──────────┘
                                    │
               ┌────────────────────┼────────────────────┐
               ↓                    ↓                    ↓
          Hội thoại         Trạng thái thế giới       Quan hệ
               │                    │                    │
               └────────────────────┼────────────────────┘
                                    ↓
                          Bus sự kiện / trạng thái
                                    ↑
               ┌────────────────────┼────────────────────┐
               ↓                    ↓                    ↓
           Người chơi            Khám phá              Ký ức
```

Hệ thống nhiệm vụ điều phối tiến trình.

Nó không nên trở thành chủ sở hữu trung tâm của mọi thứ.

---

# 28. Mục tiêu tổng hợp

Một số mục tiêu đòi hỏi nhiều điều kiện.

Ví dụ:

> Khám phá chuyện gì đã xảy ra tại ngôi nhà.

Bên trong:

```text
Bằng chứng A
AND
Bằng chứng B
AND
Lời khai của NPC
```

Người chơi có thể trải nghiệm điều này như một mục tiêu tự sự duy nhất.

Lúc chạy có thể theo dõi nhiều trạng thái bằng chứng.

---

# 29. Mục tiêu ẩn

Một số mục tiêu không nên được phơi bày.

Ví dụ:

Bên trong:

```text
objective.discover_contradiction
```

Hướng tới người chơi:

> “Có điều gì đó trong câu chuyện không khớp.”

Điều này bảo toàn sự khám phá.

---

# 30. Mục tiêu động

Mục tiêu nhiệm vụ có thể thay đổi dựa trên trạng thái người chơi.

Ví dụ:

Nếu NPC tin tưởng người chơi:

> “Hỏi Maria cô ấy nhớ gì.”

Nếu NPC không tin tưởng người chơi:

> “Tìm cách khác để biết Maria nhớ gì.”

Cùng một mục đích tự sự.

Mục tiêu khi chơi khác nhau.

---

# 31. Thay thế mục tiêu

Một mục tiêu có thể được thay thế thay vì bị thất bại.

Ví dụ:

```text
Nói chuyện với Maria
     ↓
Maria từ chối
     ↓
Mục tiêu được thay thế:
Tìm một nguồn thông tin khác
```

Cách này được ưu tiên hơn:

> QUEST FAILED

khi mục tiêu tự sự lớn hơn vẫn còn khả thi.

---

# 32. Mô hình nhánh khi chơi

Một nhánh nên được biểu diễn dưới dạng trạng thái.

Ví dụ:

```text
choice.house_truth = TOLD
```

hoặc:

```text
choice.house_truth = HIDDEN
```

Các điều kiện tiếp theo có thể tham chiếu nó.

Ví dụ:

```text
IF choice.house_truth == TOLD
    → Đường tin tưởng
ELSE
    → Đường nghi ngờ
```

---

# 33. Lưu bền trạng thái nhánh

Các lựa chọn quan trọng phải tồn tại bền vững vượt ra ngoài nhiệm vụ hiện tại.

Chúng có thể ảnh hưởng:

- hội thoại sau này;
- nhiệm vụ tương lai;
- quan hệ;
- trạng thái thế giới;
- các kết thúc;
- ký ức.

Vì vậy:

> **Lựa chọn cục bộ theo nhiệm vụ và lựa chọn cấp thế giới phải được phân biệt.**

---

# 34. Lựa chọn cục bộ theo nhiệm vụ

Chỉ ảnh hưởng nhiệm vụ hiện tại.

Ví dụ:

> Nên điều tra manh mối nào trước?

Khi nhiệm vụ kết thúc, lựa chọn không còn hiệu lực thêm.

---

# 35. Lựa chọn cấp thế giới

Ảnh hưởng trạng thái trò chơi trong tương lai.

Ví dụ:

> Tiết lộ sự thật cho khu định cư.

Điều này có thể ảnh hưởng:

- quan hệ với NPC;
- hội thoại tương lai;
- nhiệm vụ khả dụng;
- trạng thái khu định cư.

Các lựa chọn cấp thế giới phải được lưu bền.

---

# 36. Thứ tự mục tiêu

Mục tiêu có thể là:

### Tuần tự

```text
A → B → C
```

### Song song

```text
A
B
C
```

tất cả đang hoạt động.

### Tùy chọn

```text
A
B [tùy chọn]
C
```

### Thay thế

```text
A OR B → C
```

### Có điều kiện

```text
IF X → A
IF Y → B
```

---

# 37. Mục tiêu song song

Mục tiêu song song hữu ích cho khám phá.

Ví dụ:

```text
Điều tra ngôi nhà

[ ] Tìm trong nội thất
[ ] Nói chuyện với cư dân
[ ] Xem xét con đường cũ
```

Người chơi chọn thứ tự.

Hoàn thành bất kỳ mục nào cũng có thể tiết lộ thông tin thêm.

Điều này tránh tính tuyến tính quá mức.

---

# 38. Tiến trình mục tiêu

Tiến trình nên được biểu diễn bằng trạng thái, không bằng phần trăm tùy tiện khi có thể.

Ưu tiên:

```text
Đã tìm thấy bằng chứng A
Đã tìm thấy bằng chứng B
Thiếu bằng chứng C
```

hơn:

```text
Hoàn thành 67%
```

Phần trăm chỉ có thể được hiển thị cho người chơi khi phù hợp.

---

# 39. Triết lý nhật ký nhiệm vụ

Nhật ký nhiệm vụ không nên phơi bày toàn bộ đồ thị nhiệm vụ.

Nó nên cho thấy:

- điều người chơi hiện biết;
- điều họ tin;
- điều họ định làm;
- các câu hỏi quan trọng chưa được giải.

Vì vậy nhật ký nhiệm vụ nên là:

> **Biểu diễn hiểu biết của người chơi**

không phải:

> **Bản đổ triển khai của người phát triển.**

---

# 40. Thông tin nhiệm vụ chưa biết

Hệ thống có thể biết:

> Mục tiêu B tồn tại.

Người chơi có thể không biết.

Sự phân biệt này phải được bảo toàn.

Ví dụ:

Lúc chạy:

```text
Mục tiêu B = ACTIVE
```

Hướng tới người chơi:

> Không hiển thị mục tiêu hiện sẵn.

Người chơi phải khám phá bước tiếp theo qua thế giới.

---

# 41. Nhật ký

Một mục nhật ký có thể chứa:

### Đã biết

> “Ngôi nhà cũ đã bị bỏ hoang từ nhiều năm trước.”

### Nghi ngờ

> “Maria có vẻ biết nhiều hơn những gì cô ấy nói.”

### Câu hỏi

> “Vì sao cô ấy nhận ra bức ảnh?”

Điều này phù hợp với Veyloria hơn một danh sách kiểm thông thường.

---

# 42. Lịch sử nhiệm vụ khi chơi

Hệ thống nên bảo toàn lịch sử các chuyển trạng thái nhiệm vụ lớn.

Ví dụ:

```text
QUEST_STARTED
OBJECTIVE_COMPLETED
EVIDENCE_DISCOVERED
CHOICE_MADE
RELATIONSHIP_CHANGED
QUEST_COMPLETED
RECONTEXTUALIZED
```

Lịch sử này hỗ trợ:

- gỡ lỗi;
- lưu/tải;
- tham chiếu tự sự;
- phân tích;
- hệ quả tương lai.

---

# 43. Lưu bền

Trạng thái nhiệm vụ phải sống sót qua:

- lưu;
- tải;
- chuyển cảnh;
- chuyển địa điểm;
- khởi động lại trò chơi.

Trạng thái bền vững bao gồm:

- trạng thái nhiệm vụ;
- trạng thái mục tiêu;
- lựa chọn quan trọng;
- hiểu biết;
- hệ quả;
- thay đổi trạng thái thế giới.

---

# 44. Quy tắc lưu / tải

Hệ thống nhiệm vụ không nên tái dựng lịch sử chỉ từ trạng thái cảnh hiện tại.

Thay vào đó:

> **Trạng thái có thẩm quyền bền vững phải được tuần tự hóa.**

Ví dụ:

```text
quest.house.state = COMPLETED
choice.house_truth = HIDDEN
npc.maria.trust = LOW
knowledge.house_secret = TRUE
```

Việc tải khôi phục các trạng thái này.

---

# 45. Làm lại vẫn ra một kết quả

Hiệu ứng nhiệm vụ nên tránh bị nhân đôi ngoài ý muốn.

Tệ:

```text
Nhiệm vụ được tải
→ Trao phần thưởng lần nữa
→ Tăng quan hệ lần nữa
```

Tốt hơn:

```text
Hiệu ứng:
world.house.restored = true
```

Đặt một trạng thái an toàn hơn việc lặp lại một thao tác không kiểm soát.

Với hiệu ứng cộng dồn, hệ thống phải theo dõi liệu hiệu ứng đã được áp dụng hay chưa.

---

# 46. Kích hoạt nhiệm vụ

Kích hoạt nhiệm vụ nên đi theo:

```text
Phụ thuộc đã thỏa
        ↓
Nhiệm vụ khả dụng
        ↓
Kích hoạt khám phá
        ↓
Nhiệm vụ đã được khám phá
        ↓
Người chơi tham gia
        ↓
Nhiệm vụ đang hoạt động
```

Điều này tách:

> **Nhiệm vụ tồn tại**

khỏi:

> **Người chơi hiện đang theo đuổi nó.**

---

# 47. Kích hoạt tự động

Một số nhiệm vụ có thể tự động kích hoạt.

Dùng cho:

- các chuyển tiếp câu chuyện lớn;
- sự kiện thế giới khẩn cấp;
- những khoảnh khắc tự sự không thể tránh.

Không tự động kích hoạt mọi nhiệm vụ phụ.

---

# 48. Kích hoạt do người chơi khởi xướng

Được ưu tiên cho:

- khám phá;
- điều tra tùy chọn;
- quan hệ;
- nội dung đời thường.

Ví dụ:

Người chơi nhận thấy điều gì đó.

↓

Người chơi chọn điều tra.

↓

Nhiệm vụ trở thành hoạt động.

Điều này bảo toàn quyền chủ động.

---

# 49. Gián đoạn nhiệm vụ

Một nhiệm vụ có thể bị gián đoạn bởi:

- một sự kiện khác;
- chuyển địa điểm;
- thay đổi thế giới;
- NPC biến mất;
- lựa chọn của người chơi.

Gián đoạn nên bảo toàn trạng thái trừ khi tự sự thay đổi trạng thái đó một cách nói rõ.

---

# 50. Mức ưu tiên nhiệm vụ

Nhiệm vụ khi chơi có thể có mức ưu tiên:

### Tới hạn

Bắt buộc cho tiến trình.

### Quan trọng

Gắn chặt với trạng thái tự sự hiện tại.

### Tùy chọn

Khả dụng nhưng không thiết yếu.

### Môi trường

Nổi lên một cách tự nhiên từ tương tác với thế giới.

Mức ưu tiên ảnh hưởng:

- giao diện;
- thông báo;
- thứ tự nhật ký nhiệm vụ.

Nó không nên tự động quyết định tự do của người chơi.

---

# 51. Hết hạn nhiệm vụ

Một số nhiệm vụ có thể hết hạn.

Việc hết hạn nên được dẫn dắt bởi tự sự.

Ví dụ:

> Giúp chuẩn bị sự kiện trước khi mặt trời lặn.

Sau khi mặt trời lặn:

> Sự kiện đã xảy ra rồi.

Kết quả trở thành:

> Thay đổi trạng thái thế giới

không nhất thiết là:

> Nhiệm vụ thất bại.

---

# 52. Logic nhiệm vụ theo thời gian

Nhiệm vụ theo thời gian có thể dùng:

- pha thế giới;
- pha câu chuyện;
- trạng thái sự kiện;
- ngày/đêm;
- sự kiện đã lên lịch.

Tránh các đếm ngược thời gian thực không cần thiết.

Mục tiêu là:

> **Thời gian tự sự**

thay vì:

> **cơ chế đồng hồ gây căng thẳng**

trừ khi được chủ đích rõ ràng.

---

# 53. Đánh giá phụ thuộc nhiệm vụ

Việc đánh giá phụ thuộc nên là gia tăng.

Khi:

```text
KnowledgeChanged
```

đánh giá các nhiệm vụ phụ thuộc vào:

> Hiểu biết.

Khi:

```text
RelationshipChanged
```

đánh giá các nhiệm vụ phụ thuộc quan hệ.

Điều này tránh đánh giá toàn cục không cần thiết.

---

# 54. Ví dụ sự kiện khi chơi

```text
Người chơi xem xét bức ảnh
        ↓
SỰ KIỆN:
EvidenceDiscovered(photo_01)
        ↓
Hệ thống hiểu biết:
photo_01_known = true
        ↓
Hệ thống nhiệm vụ:
Đánh giá các mục tiêu phụ thuộc
        ↓
Mục tiêu:
"Hiểu bức ảnh"
        ↓
COMPLETED
        ↓
Nhiệm vụ tiến lên
        ↓
Mục tiêu mới:
"Tìm ra đứa trẻ là ai"
        ↓
Các hệ thống hội thoại / khám phá nhận trạng thái mới
```

Điều này minh họa kiến trúc dự định.

---

# 55. Ví dụ hoàn thành nhiệm vụ

```text
Mục tiêu A → COMPLETE
Mục tiêu B → COMPLETE
Mục tiêu C → COMPLETE
        ↓
Điều kiện hoàn thành = TRUE
        ↓
Nhiệm vụ → COMPLETE
        ↓
Hiệu ứng:
    knowledge += X
    relationship += Y
    world_state = Z
        ↓
SỰ KIỆN:
QuestCompleted
        ↓
Các nhiệm vụ phụ thuộc được đánh giá
```

---

# 56. Ví dụ thất bại nhiệm vụ

```text
Người chơi chọn giấu bằng chứng
        ↓
NPC phát hiện sự lừa dối
        ↓
Sự tin tưởng giảm
        ↓
Mục tiêu ban đầu trở thành không thể
        ↓
Mục tiêu → REPLACED
        ↓
Mục tiêu mới:
"Tìm một nguồn bằng chứng khác"
```

Nhiệm vụ tiếp tục.

Thất bại của người chơi trở thành:

> **Trạng thái tự sự**

thay vì:

> **Xóa nội dung**

---

# 57. Hiểu lại khi chơi

Thông tin sau này có thể kích hoạt:

```text
SỰ KIỆN:
MajorTruthDiscovered
        ↓
Tìm trong lịch sử nhiệm vụ
        ↓
Tìm thấy nhiệm vụ đã hoàn thành liên quan
        ↓
Nhiệm vụ → RECONTEXTUALIZED
        ↓
Nhật ký / Hội thoại / Thế giới phản ứng
```

Điều này cho phép nội dung trước đó nhận ý nghĩa mới mà không cần chơi lại.

---

# 58. Trạng thái nhiệm vụ so với trạng thái thế giới

Trạng thái nhiệm vụ trả lời:

> **Nhiệm vụ này đang ở đâu?**

Trạng thái thế giới trả lời:

> **Điều gì là đúng trong thế giới?**

Ví dụ:

```text
Nhiệm vụ:
HOUSE_INVESTIGATION = COMPLETED

Thế giới:
house.owner = unknown
house.door = unlocked
maria.trust = high
truth_about_house = partially_known
```

Hoàn thành nhiệm vụ không thay thế trạng thái thế giới.

---

# 59. Hệ thống nhiệm vụ như bộ điều phối

Hệ thống nhiệm vụ nên chủ yếu điều phối:

> **Điều kiện → Mục tiêu → Trạng thái → Hiệu ứng**

Nó không nên trở thành:

> **Toàn bộ hệ thống logic trò chơi.**

Sự tách biệt này là then chốt cho khả năng mở rộng.

---

# 60. Mô hình dữ liệu nhiệm vụ khi chơi

Cấu trúc khái niệm:

```text
QuestDefinition
{
    id
    type
    secondaryTypes
    dependencies
    discoveryConditions
    objectives
    branches
    completionConditions
    failureConditions
    effects
    metadata
}
```

Lúc chạy:

```text
QuestInstance
{
    questId
    state
    activeObjectives
    completedObjectives
    choices
    branchState
    effectState
    timestamps
}
```

Đây là khái niệm và chưa quy định ngôn ngữ lập trình hay khung triển khai.

---

# 61. Mô hình dữ liệu mục tiêu

Khái niệm:

```text
ObjectiveDefinition
{
    id
    type
    activationConditions
    completionConditions
    failureConditions
    optional
    hidden
    presentation
}
```

Lúc chạy:

```text
ObjectiveInstance
{
    objectiveId
    state
    progressState
    discovered
    completed
}
```

---

# 62. Mô hình dữ liệu điều kiện

Khái niệm:

```text
Condition
{
    operator
    operands
}
```

Ví dụ:

```text
AND
├── quest.intro == COMPLETED
├── location.house == DISCOVERED
└── knowledge.photo == TRUE
```

Điều này cung cấp một hệ thống điều kiện dùng lại được.

---

# 63. Mô hình dữ liệu hiệu ứng

Khái niệm:

```text
Effect
{
    type
    target
    value
}
```

Ví dụ:

```text
SET_WORLD_STATE
SET_KNOWLEDGE
CHANGE_RELATIONSHIP
UNLOCK_QUEST
BLOCK_QUEST
TRIGGER_EVENT
ADD_DIALOGUE_STATE
```

---

# 64. Quy tắc an toàn khi chơi

Logic nhiệm vụ phải bảo vệ chống lại:

- hoàn thành trùng lặp;
- chuyển trạng thái không thể;
- phụ thuộc vòng;
- phụ thuộc thiếu;
- điều kiện mâu thuẫn;
- nhiệm vụ không gắn;
- đường tới hạn bị chặn vĩnh viễn;
- hiệu ứng trùng lặp;
- lệch đồng bộ lưu/tải.

---

# 65. Phụ thuộc vòng

Tệ:

```text
Nhiệm vụ A yêu cầu Nhiệm vụ B
Nhiệm vụ B yêu cầu Nhiệm vụ A
```

Không nhiệm vụ nào có thể kích hoạt.

Hệ thống kiểm định nội dung phải phát hiện điều này trước khi chơi.

---

# 66. Nhiệm vụ không gắn

Một nhiệm vụ không còn gắn vào đâu khi:

> Không gì có thể thỏa các điều kiện kích hoạt của nó.

Mọi nhiệm vụ được soạn nên có ít nhất một đường kích hoạt có thể đạt tới.

---

# 67. Kiểm định đường tới hạn

Hệ thống nên kiểm định:

> Người chơi có luôn đạt được trạng thái tự sự bắt buộc tiếp theo không?

Với mọi nhiệm vụ tới hạn:

```text
BẮT ĐẦU
 ↓
Kích hoạt
 ↓
Tiến trình
 ↓
Hoàn thành
 ↓
Trạng thái tới hạn tiếp theo
```

Phải có một đường hợp lệ.

---

# 68. Ngăn kẹt tiến trình

Kẹt tiến trình xảy ra khi:

> Người chơi có thể tiếp tục chơi nhưng không thể tiến triển tự sự chính.

Hệ thống nhiệm vụ nên phát hiện hoặc ngăn:

- mục tiêu bắt buộc không thể thực hiện;
- NPC tới hạn không có mặt vĩnh viễn;
- các lựa chọn bắt buộc loại trừ lẫn nhau;
- địa điểm bắt buộc không thể vào;
- chuỗi phụ thuộc bị gãy.

---

# 69. Gỡ lỗi logic nhiệm vụ

Công cụ phát triển nên phơi bày:

- trạng thái nhiệm vụ hiện tại;
- trạng thái mục tiêu;
- kết quả phụ thuộc;
- điều kiện không đạt;
- nhánh đang hoạt động;
- hiệu ứng đã áp dụng;
- lịch sử sự kiện.

Ví dụ:

```text
QUEST: HOUSE_001

STATE: BLOCKED

Lý do:
knowledge.house_significance = FALSE

Yêu cầu:
TRUE

Hiện tại:
FALSE
```

Điều này thiết yếu để gỡ lỗi các hệ thống tự sự phức tạp.

---

# 70. Vết khi chơi

Một vết gỡ lỗi hữu ích:

```text
[20:41:02] EvidenceDiscovered(photo_01)
[20:41:02] KnowledgeChanged(photo_01=true)
[20:41:02] Objective house.investigate_photo → COMPLETE
[20:41:02] Objective house.identify_child → ACTIVE
[20:41:02] Quest HOUSE_001 → ACTIVE
```

Điều này làm cho lỗi nhiệm vụ có thể giải thích được.

---

# 71. Ngôn ngữ hướng tới người chơi so với ngôn ngữ khi chơi

Lúc chạy:

> `knowledge.house_identity = TRUE`

Hướng tới người chơi:

> “Người trong bức ảnh có thể có liên hệ với bạn.”

Lúc chạy:

> `relationship.maria.trust < threshold`

Hướng tới người chơi:

> “Maria không đủ tin tưởng bạn để kể cho bạn.”

Hai lớp này phải được giữ tách biệt.

---

# 72. Nguyên tắc nhiệm vụ khi chơi

### Nguyên tắc 1

> **Trạng thái hơn kịch bản.**

### Nguyên tắc 2

> **Sự kiện hơn thăm dò liên tục.**

### Nguyên tắc 3

> **Điều kiện có ý nghĩa hơn cổng tùy tiện.**

### Nguyên tắc 4

> **Trạng thái thế giới hơn cờ hoàn thành nhiệm vụ.**

### Nguyên tắc 5

> **Hệ quả bền vững hơn phần thưởng tạm thời.**

### Nguyên tắc 6

> **Thất bại có thể phục hồi hơn thất bại cứng không cần thiết.**

### Nguyên tắc 7

> **Hiểu biết của người chơi khác với hiểu biết của hệ thống.**

---

# 73. Tích hợp với các bước trước

9.3 cung cấp:

> **Loại nhiệm vụ + Ngữ pháp nhiệm vụ**

9.4 cung cấp:

> **Chuỗi nhiệm vụ + Phụ thuộc + Tiến trình**

9.5 cung cấp:

> **Trạng thái khi chơi + Mục tiêu + Điều kiện + Sự kiện + Hiệu ứng**

Vì vậy:

```text
Nhịp câu chuyện
    ↓
Trải nghiệm người chơi
    ↓
Cấu trúc nhiệm vụ
    ↓
Loại nhiệm vụ / Ngữ pháp
    ↓
Chuỗi nhiệm vụ / Phụ thuộc
    ↓
Trạng thái nhiệm vụ khi chơi
    ↓
Sự kiện cách chơi
    ↓
Trạng thái thế giới
    ↓
Khả năng nhiệm vụ tương lai
```

Đây là đường ống đầy đủ từ thiết kế đến khi chơi.

---

# 74. Công thức khi chơi chuẩn

Thời gian chạy nhiệm vụ của Veyloria đi theo:

> **SỰ KIỆN → THAY ĐỔI TRẠNG THÁI → ĐIỀU KIỆN → MỤC TIÊU → TRẠNG THÁI NHIỆM VỤ → HIỆU ỨNG → TRẠNG THÁI MỚI**

Ví dụ:

> Người chơi khám phá bằng chứng

→ Hiểu biết thay đổi

→ Điều kiện được thỏa

→ Mục tiêu hoàn thành

→ Nhiệm vụ tiến lên

→ Mục tiêu mới được kích hoạt

→ Thế giới phản ứng

→ Nhiệm vụ mới trở thành khả thi.

---

# 75. Tiêu chí hoàn thành 9.5

9.5 hoàn thành khi mọi nhiệm vụ về lý thuyết có thể được biểu diễn dưới dạng:

- một Định nghĩa nhiệm vụ tĩnh;
- một Thể hiện nhiệm vụ khi chơi;
- trạng thái mục tiêu;
- điều kiện phụ thuộc;
- chuyển trạng thái theo sự kiện;
- lựa chọn của người chơi;
- đột biến trạng thái;
- hiệu ứng bền vững;
- hành vi thất bại/phục hồi;
- trạng thái lưu/tải;
- thông tin gỡ lỗi.

Phép thử cuối cùng là:

> **Hệ thống nhiệm vụ có thể xác định điều nên xảy ra tiếp theo hoàn toàn từ trạng thái trò chơi có thẩm quyền và các sự kiện, thay vì từ các giả định cứng về việc người chơi đã làm gì không?**

Nếu có, nhiệm vụ có một mô hình khi chơi hợp lệ.

---

# 76. Trạng thái Bước 9

Tại thời điểm này:

### 9.1 — Khung ánh xạ câu chuyện → cách chơi

Định nghĩa:

> **Câu chuyện trở thành cách chơi như thế nào.**

### 9.2 — Nhịp câu chuyện → cấu trúc nhiệm vụ

Định nghĩa:

> **Nhịp câu chuyện trở thành nhiệm vụ như thế nào.**

### 9.3 — Loại nhiệm vụ và cách dựng nhiệm vụ

Định nghĩa:

> **Những loại nhiệm vụ nào tồn tại và chúng diễn tiến như thế nào.**

### 9.4 — Chuỗi nhiệm vụ, phụ thuộc và tiến trình

Định nghĩa:

> **Các nhiệm vụ kết nối và tạo tiến trình như thế nào.**

### 9.5 — Trạng thái nhiệm vụ, mục tiêu và cách nhiệm vụ diễn ra khi chơi

Định nghĩa:

> **Nhiệm vụ thực sự vận hành trong khi chơi của trò chơi như thế nào.**

---

## Chuyển sang 9.6

> **9.6 — PHẦN THƯỞNG, HỆ QUẢ VÀ THAY ĐỔI TRẠNG THÁI THẾ GIỚI**
