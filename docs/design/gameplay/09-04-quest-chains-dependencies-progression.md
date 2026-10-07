# 9.4 — CHUỖI NHIỆM VỤ, PHỤ THUỘC VÀ TIẾN TRÌNH

## Mục đích

9.4 định nghĩa cách các nhiệm vụ riêng được nối thành những cấu trúc chơi được lớn hơn.

Mục tiêu là ngăn Veyloria trở thành:

> **Nhiệm vụ A → Nhiệm vụ B → Nhiệm vụ C → Nhiệm vụ D**

khi mạch kể đáng ra phải vận hành như:

> **Người chơi khám phá → chọn điều sẽ theo đuổi → đổi thế giới → mở những khả năng mới → quay lại hiểu biết trước đó → tiến về một sự thật lớn hơn.**

9.4 vì vậy định nghĩa:

- Chuỗi nhiệm vụ;
- Phụ thuộc của nhiệm vụ;
- Điều kiện mở khóa;
- Cổng tiến trình;
- Nội dung tùy chọn;
- Phân nhánh;
- Hội tụ;
- Các tuyến nhiệm vụ song song;
- Mức ưu tiên nhiệm vụ;
- Phụ thuộc trạng thái thế giới;
- Phụ thuộc hiểu biết;
- Phụ thuộc quan hệ;
- Phụ thuộc quay lại;
- Thất bại và phục hồi;
- Tiến trình ở mức hồi.

Nguyên tắc lõi là:

> **Tiến trình nên được dẫn bởi trạng thái có nghĩa, không phải bởi việc hoàn thành tùy tiện.**

---

# 1. Định nghĩa chuỗi nhiệm vụ

Một chuỗi nhiệm vụ là:

> **Một trình tự hoặc một mạng các nhiệm vụ, nối với nhau bằng mạch kể, cách chơi, trạng thái thế giới, quan hệ hoặc hiểu biết.**

Một chuỗi có thể là:

- Tuyến tính;
- Phân nhánh;
- Song song;
- Hội tụ;
- Đệ quy;
- Được hiểu lại.

Một chuỗi nhiệm vụ không nhất thiết là một trình tự cố định.

---

# 2. Chuỗi nhiệm vụ và danh sách nhiệm vụ

Một danh sách nhiệm vụ là:

> Nhiệm vụ A  
> Nhiệm vụ B  
> Nhiệm vụ C  
> Nhiệm vụ D

Một chuỗi nhiệm vụ là:

> Nhiệm vụ A đổi trạng thái X.

↓

> Trạng thái X mở Nhiệm vụ B.

↓

> Nhiệm vụ B lộ thông tin Y.

↓

> Thông tin Y làm Nhiệm vụ C có nghĩa.

Vì vậy:

> **Chuỗi nhiệm vụ = quan hệ giữa các trạng thái nhiệm vụ**

không chỉ là:

> **các mục tiêu đã sắp thứ tự.**

---

# 3. Mô hình chuỗi nhiệm vụ chuẩn

Cấu trúc chuẩn là:

> **NHIỆM VỤ → ĐỔI TRẠNG THÁI → ĐIỀU KIỆN MỞ KHÓA → KHẢ NĂNG TIẾP THEO**

Mở rộng:

> **Hành động nhiệm vụ → Đổi thế giới / hiểu biết / quan hệ → Kiểm tra phụ thuộc → Nhiệm vụ mới sẵn có → Lựa chọn người chơi → Trạng thái mới**

Điều này có nghĩa tiến trình nhiệm vụ nên nảy ra từ trạng thái của thế giới.

---

# 4. Các loại chuỗi nhiệm vụ

Veyloria dùng sáu cấu trúc chuỗi chính.

## 4.1 Chuỗi tuyến tính

> A → B → C → D

Dùng khi:

- thứ tự kể chuyện đã cố định;
- thông tin phải được lộ lần lượt;
- tiến trình hồi đòi một trình tự cụ thể.

Tuyến tính không có nghĩa trải nghiệm người chơi phải cứng nhắc.

Khám phá tùy chọn vẫn có thể tồn tại giữa các nút.

---

## 4.2 Chuỗi phân nhánh

> A → B / C / D

Dùng khi một quyết định của người chơi tạo những hệ quả khác nhau một cách thực chất.

Các nhánh có thể đổi:

- quan hệ;
- hiểu biết;
- lối vào;
- cơ hội;
- trạng thái thế giới;
- điều kiện nhiệm vụ về sau.

---

## 4.3 Chuỗi hội tụ

> A → B / C → D

Những trải nghiệm người chơi khác nhau cuối cùng hướng về một điểm đến kể chuyện chung.

Đây là cấu trúc được ưu tiên cho các vòng câu chuyện lớn, khi phân nhánh kể chuyện đầy đủ sẽ trở nên đắt một cách không cần thiết.

---

## 4.4 Chuỗi song song

> A → B  
> A → C  
> A → D

Nhiều nhiệm vụ trở nên sẵn có cùng lúc.

Người chơi chọn điều sẽ theo đuổi trước.

Điều này tạo ra:

> **nhịp độ do người chơi dẫn**

mà không đòi phân nhánh kể chuyện lớn.

---

## 4.5 Chuỗi giao nhau

> Chuỗi A ───┐  
>            ├→ Nhiệm vụ X  
> Chuỗi B ───┘

Hai tuyến nhiệm vụ trước đó độc lập bắt đầu ảnh hưởng lẫn nhau.

Ví dụ:

Một nhiệm vụ quan hệ đổi mức tin cậy của một NPC.

Mức tin cậy ấy quyết định một nhiệm vụ điều tra diễn ra thế nào.

---

## 4.6 Chuỗi được hiểu lại

> Nhiệm vụ A → Nhiệm vụ B → thông tin mới → hiểu lại Nhiệm vụ A

Nhiệm vụ gốc vẫn đã hoàn thành.

Ý nghĩa của nó đổi.

Điều này đặc biệt quan trọng với:

- ký ức;
- danh tính;
- bí ẩn;
- lịch sử bị giấu.

---

# 5. Định nghĩa phụ thuộc

Một phụ thuộc là:

> **Một điều kiện phải được thỏa trước khi một nhiệm vụ, một trình tự hoặc một kết cục trở nên sẵn có.**

Phụ thuộc nên thể hiện trạng thái trò chơi có nghĩa.

Ví dụ:

- Nhiệm vụ trước đã hoàn thành;
- Quan hệ với NPC đạt một trạng thái;
- Địa điểm đã được khám phá;
- Bằng chứng đã có được;
- Trạng thái thế giới đã đổi;
- Người chơi đã học được một điều;
- Hồi đã tới;
- Quyết định trước đã được đưa ra.

---

# 6. Nhóm phụ thuộc

Veyloria dùng tám nhóm phụ thuộc.

### 1. Phụ thuộc kể chuyện

Một sự kiện câu chuyện trước đó phải xảy ra.

### 2. Phụ thuộc hiểu biết

Người chơi phải biết hoặc khám phá một điều.

### 3. Phụ thuộc quan hệ

Một NPC phải tin cậy, nhận ra hoặc đáp lại người chơi theo một cách nhất định.

### 4. Phụ thuộc trạng thái thế giới

Một địa điểm, vật thể hoặc trạng thái toàn cục phải đổi.

### 5. Phụ thuộc địa điểm

Người chơi phải đã khám phá hoặc vào được một địa điểm.

### 6. Phụ thuộc lựa chọn

Một quyết định trước của người chơi ảnh hưởng sự sẵn có.

### 7. Phụ thuộc tiến trình

Một hồi hoặc một trạng thái tiến trình lớn phải đã tới.

### 8. Phụ thuộc hệ thống

Một năng lực cách chơi phải tồn tại.

Phụ thuộc hệ thống nên được dùng thận trọng.

Ưu tiên:

> **Phụ thuộc kể chuyện / hiểu biết / thế giới**

hơn:

> **Bạn phải đạt Cấp 10.**

---

# 7. Thứ tự ưu tiên phụ thuộc

Khi có thể, dùng phụ thuộc theo thứ tự này:

1. Ý nghĩa câu chuyện;
2. Hiểu biết của người chơi;
3. Trạng thái thế giới;
4. Quan hệ;
5. Địa điểm;
6. Lựa chọn trước đó;
7. Trạng thái tiến trình;
8. Năng lực cơ chế;
9. Yêu cầu số tùy tiện.

Phụ thuộc càng ở thấp trong danh sách này, lý do biện minh càng phải mạnh.

---

# 8. Phụ thuộc cứng và phụ thuộc mềm

## Phụ thuộc cứng

Nhiệm vụ không thể tồn tại một cách có nghĩa cho đến khi điều kiện được thỏa.

Ví dụ:

> Người chơi không thể điều tra căn phòng giấu trước khi khám phá ra rằng căn phòng ấy tồn tại.

## Phụ thuộc mềm

Nhiệm vụ có thể tồn tại, nhưng thông tin, hội thoại hoặc kết cục bổ sung chỉ sẵn có sau khi điều kiện được thỏa.

Ví dụ:

> Người chơi có thể nói chuyện với một NPC trước khi có được tin cậy của họ.

Sau khi có tin cậy:

> cuộc trò chuyện sâu hơn trở nên sẵn có.

Phụ thuộc mềm được ưu tiên khi chúng tạo quyền chủ động phong phú hơn cho người chơi.

---

# 9. Điều kiện mở khóa

Một nhiệm vụ có thể mở khóa vì:

### Sự kiện

> Nhiệm vụ trước đã hoàn thành.

### Khám phá

> Người chơi đã khám phá địa điểm.

### Hiểu biết

> Người chơi đã học được một sự thật cụ thể.

### Quan hệ

> NPC tin người chơi.

### Trạng thái thế giới

> Khu định cư được sửa.

### Lựa chọn

> Người chơi đã từ chối một NPC khác.

### Quay lại

> Người chơi đã trở lại sau một sự kiện liên quan.

### Thời gian / Tiến trình

> Hồi đã tới một trạng thái nhất định.

Hệ thống nên tránh dựa chủ yếu vào bộ đếm thời gian vô hình.

---

# 10. Cổng hiểu biết

Một cổng hiểu biết có nghĩa là:

> **Người chơi chỉ có thể tiến một cách có nghĩa sau khi đã học được một điều.**

Ví dụ:

Người chơi gặp một cánh cửa khóa.

Một trò chơi thông thường có thể dùng:

> Cần chìa khóa.

Veyloria có thể dùng thay vào đó:

> Cần hiểu biết.

Người chơi khám phá:

> Cửa chỉ mở khi một người cụ thể có mặt.

Cổng do đó là:

> **Thấu hiểu → Hành động**

thay vì:

> **Vật phẩm → Hành động**

---

# 11. Cổng quan hệ

Một cổng quan hệ nên thể hiện logic xã hội thực.

Ví dụ:

Một NPC từ chối tiết lộ một bí mật.

Sau những tương tác trước:

> Tin cậy tăng.

NPC trở nên sẵn lòng nói.

Cổng là:

> **Trạng thái quan hệ → Lối vào thông tin**

không phải:

> **Cấp quan hệ 3 → Hội thoại #17**

Khi có thể, trạng thái nên được thể hiện trong thế giới.

---

# 12. Cổng trạng thái thế giới

Cổng trạng thái thế giới được kích bởi những thay đổi tồn tại.

Ví dụ:

> Ngôi nhà được sửa.

→ Tương tác cư dân mới.

---

> Sự kiện khu định cư đã hoàn thành.

→ Tình huống xã hội mới.

---

> Lối cũ được mở lại.

→ Khám phá trở nên có thể.

---

> NPC đã rời thị trấn.

→ Cơ hội hội thoại trước đó biến mất.

Nguyên tắc quan trọng là:

> **Trạng thái thế giới nên tạo nội dung, không chỉ mở khóa bảng chọn.**

---

# 13. Trạng thái sẵn có của nhiệm vụ

Một nhiệm vụ có thể ở một trong các trạng thái sau:

- Ẩn;
- Được đồn;
- Sẵn có;
- Đã khám phá;
- Đang làm;
- Tạm dừng;
- Bị chặn;
- Đã hoàn thành;
- Đã thất bại;
- Đã hiểu lại;
- Đã lưu trữ.

Không phải nhiệm vụ nào cũng cần đủ mọi trạng thái.

---

# 14. Ẩn và không sẵn có

Đây là hai việc khác nhau.

### Ẩn

Người chơi không biết nhiệm vụ tồn tại.

### Không sẵn có

Người chơi biết có một điều tồn tại, nhưng hiện chưa thể theo đuổi.

Ví dụ:

> NPC nói họ sẽ nói chuyện sau.

Nhiệm vụ là:

> **Đã biết nhưng chưa sẵn**

Phân biệt này quan trọng cho sự nhập vai.

---

# 15. Đồ thị sẵn có của nhiệm vụ

Tiến trình nhiệm vụ nên được hình dung như một đồ thị.

Ví dụ:

```text
                 ┌── Nhiệm vụ quan hệ
                 │
MỞ ĐẦU       ────┼── Nhiệm vụ khám phá
                 │
                 └── Nhiệm vụ điều tra
                           │
                           ↓
                     Bằng chứng mới
                           │
                 ┌─────────┴─────────┐
                 ↓                   ↓
         Nhiệm vụ quay lại     Nhiệm vụ ký ức
                 │                   │
                 └─────────┬─────────┘
                           ↓
                      Tiết lộ lớn
```

Cách này đáng ưu tiên hơn một danh sách nhiệm vụ tuyến tính đơn giản.

---

# 16. Nút chuỗi nhiệm vụ

Mọi nhiệm vụ trong một chuỗi nên có:

- Mã nhiệm vụ;
- Loại chính;
- Loại phụ;
- Nhiệm vụ cha;
- Nhiệm vụ con;
- Phụ thuộc bắt buộc;
- Phụ thuộc tùy chọn;
- Điều kiện mở khóa;
- Điều kiện chặn;
- Đổi trạng thái;
- Đổi hiểu biết;
- Đổi quan hệ;
- Đổi thế giới;
- Hệ quả;
- Khả năng quay lại.

---

# 17. Quan hệ cha / con

Một nhiệm vụ cha tạo ra một hoặc nhiều khả năng tiếp theo.

Ví dụ:

> QUEST A — NGƯỜI LẠ

có thể mở khóa:

- QUEST B — AI BIẾT TÊN TÔI?
- QUEST C — CON ĐƯỜNG CŨ
- QUEST D — NGÔI NHÀ

Người chơi không nhất thiết phải hoàn thành cả ba.

Thông tin quan trọng là:

> **A đã tạo không gian khả năng.**

---

# 18. Chuỗi nhiệm vụ tùy chọn

Nội dung tùy chọn không nên cảm giác như phần đệm dùng rồi bỏ.

Một nhiệm vụ tùy chọn có thể đem lại:

- bằng chứng bổ sung;
- chiều sâu quan hệ;
- cách diễn giải khác;
- lịch sử thế giới;
- ngữ cảnh bổ sung;
- hệ quả về sau.

Tùy chọn không có nghĩa là:

> vô nghĩa.

---

# 19. Nhiệm vụ chính và nhiệm vụ tùy chọn

Sự phân biệt trước hết nên là:

### Nhiệm vụ chính

Bắt buộc cho tiến trình kể chuyện lớn.

### Nhiệm vụ tùy chọn

Không bắt buộc cho lối tiến trình chính.

Cả hai vẫn có thể:

- đổi quan hệ;
- đổi trạng thái thế giới;
- lộ thông tin;
- ảnh hưởng nội dung về sau.

Vì vậy:

> **Tùy chọn ≠ không liên quan.**

---

# 20. Thông tin then chốt và thông tin bổ trợ

Không phải mọi thông tin đều nên bị khóa sau nhiệm vụ tùy chọn.

### Thông tin then chốt

Cần để hiểu mạch kể chính.

Phải vẫn lấy lại được qua lối chính hoặc một lối hợp lệ khác.

### Thông tin bổ trợ

Làm sâu cách diễn giải, nhưng là tùy chọn.

Có thể chỉ tồn tại trong:

- nhiệm vụ phụ;
- khám phá;
- hội thoại NPC;
- những lần quay lại;
- bằng chứng môi trường.

Điều này ngăn người chơi vô tình không còn hiểu được câu chuyện chính vì đã bỏ qua nội dung tùy chọn.

---

# 21. Lối then chốt

Lối then chốt là:

> **Chuỗi trải nghiệm tối thiểu cần có để tới trạng thái kể chuyện lớn tiếp theo.**

Nó không nhất thiết phải là:

> Nhiệm vụ 1 → Nhiệm vụ 2 → Nhiệm vụ 3.

Nó có thể là:

> Khám phá X  
> VÀ hiểu Y  
> VÀ tới địa điểm Z.

Vì vậy:

> **Lối then chốt = các điều kiện trạng thái bắt buộc**

thay vì:

> **Lối then chốt = danh sách đánh dấu nhiệm vụ**

---

# 22. Tiến trình song song

Khi nhiều nhiệm vụ cùng sẵn có:

> **Người chơi chọn thứ tự.**

Ví dụ:

```text
                 ┌── Điều tra ngôi nhà
                 │
Khu định cư ─────┼── Giúp cư dân
                 │
                 └── Khám phá rừng
```

Hoàn thành nhiệm vụ nào cũng có thể đổi thế giới.

Các nhiệm vụ còn lại nên phản ứng ở chỗ thích hợp.

---

# 23. Thứ tự mềm

Thứ tự mềm có nghĩa là:

> Trò chơi gợi một trình tự dự định mà không ép buộc chặt.

Ví dụ:

Người chơi có thể điều tra ngôi nhà ngay.

Hoặc:

Họ có thể nói chuyện với cư dân già trước.

Cả hai đều hợp lệ.

Lối thứ hai có thể đem thêm ngữ cảnh.

Điều này tạo ra:

> **Thứ tự khám phá do người chơi tạo.**

---

# 24. Thứ tự cứng

Thứ tự cứng là phù hợp khi:

- hiểu biết phải được thiết lập trước;
- một địa điểm thực sự chưa tồn tại;
- một sự kiện mức hồi chưa xảy ra;
- một quyết định trước quyết định căn bản tình huống.

Thứ tự cứng nên có một lý do kể chuyện.

Tránh:

> “Nhiệm vụ không sẵn vì nhiệm vụ trước chưa hoàn thành.”

Ưu tiên:

> “NPC vẫn chưa trở về.”

hoặc:

> “Địa điểm vẫn chưa vào được.”

---

# 25. Luật phân nhánh chuỗi nhiệm vụ

Một nhánh chỉ nên được tạo khi nó đổi một điều có nghĩa.

Nhánh hợp lệ:

> Nói sự thật với NPC.

→ NPC tin người chơi.

Hoặc:

> Nói dối.

→ NPC trở nên nghi ngờ.

Nhánh không hợp lệ:

> Lựa chọn A: “Có.”

> Lựa chọn B: “Chắc chắn.”

Cả hai tạo ra cùng một trạng thái.

Đó không phải phân nhánh có nghĩa.

---

# 26. Kiểm soát chi phí nhánh

Phân nhánh kể chuyện có thể đắt lên theo cấp số nhân.

Vì vậy Veyloria ưu tiên:

> **Phân nhánh ở hệ quả, hội tụ ở cấu trúc.**

Ví dụ:

```text
             ┌── Sự thật ──→ NPC tin người chơi ───┐
Quest A ────┤                                      ├→ Quest C
             └── Nói dối ──→ NPC nghi người chơi ──┘
```

Nhiệm vụ C được dùng chung.

Nhưng:

- hội thoại;
- bằng chứng;
- quan hệ;
- thông tin sẵn có

có thể khác nhau.

---

# 27. Hội tụ mà không xóa lựa chọn

Hội tụ không có nghĩa là:

> “Không có gì quan trọng.”

Nó có nghĩa là:

> **Những trải nghiệm khác nhau tới một điểm đến kể chuyện chung, với trạng thái khác nhau.**

Nhiệm vụ C do đó có thể bắt đầu với:

- thái độ NPC khác nhau;
- thông tin sẵn có khác nhau;
- bằng chứng khác nhau;
- quan hệ khác nhau;
- cách diễn giải khác nhau.

Điểm đến có thể được dùng chung.

Trải nghiệm thì không.

---

# 28. Phụ thuộc nhiệm vụ và ký ức

Mọi phụ thuộc nên xét:

> **Người chơi biết gì?**

Một nhiệm vụ có thể sẵn có về mặt kỹ thuật, nhưng còn sớm về mặt kể chuyện.

Ví dụ:

Người chơi khám phá một bức ảnh cũ.

Hệ thống nhiệm vụ có thể mở khóa ngay:

> “Điều tra tuổi thơ của nhân vật chính.”

Nhưng người chơi có thể chưa đủ ngữ cảnh.

Một cấu trúc tốt hơn có thể là:

> Bức ảnh được khám phá.

↓

> Nghi ngờ được tạo ra.

↓

> Bằng chứng về sau xác nhận tầm quan trọng của nó.

↓

> Cuộc điều tra trở nên sẵn có.

Cách này giữ bí ẩn.

---

# 29. Phụ thuộc nhiệm vụ và hiểu biết của người chơi

Nhiệm vụ sẵn có không phải lúc nào cũng bằng thấu hiểu của người chơi.

Người chơi có thể có:

- lối vào mà chưa thấu hiểu;
- thấu hiểu mà chưa có lối vào;
- nghi ngờ mà chưa có bằng chứng;
- bằng chứng mà chưa có diễn giải.

Điều này tạo sự chưa chắc có nghĩa.

Ví dụ:

> Người chơi biết ngôi nhà là quan trọng.

Nhưng:

> không biết vì sao.

Nhiệm vụ có thể vẫn đang làm, mà không giải bí ẩn quá sớm.

---

# 30. Mô hình tiến trình chuỗi nhiệm vụ

Một chuỗi lớn có thể được mô hình hóa thành:

> **KHÁM PHÁ → ĐIỀU TRA → PHÁT TRIỂN → BIẾN CHỨNG → QUYẾT ĐỊNH → HỆ QUẢ → HIỂU LẠI**

Đây nên là kiến trúc mặc định cho các vòng kể chuyện lớn.

---

# 31. Tiến trình nhiệm vụ ở mức hồi

Mỗi hồi nên chứa:

### Vào hồi

Người chơi bước vào một trạng thái kể chuyện mới.

↓

### Định hướng

Người chơi biết điều gì đã đổi.

↓

### Khám phá

Người chơi khám phá những câu hỏi tại chỗ.

↓

### Phát triển

Các chuỗi nhiệm vụ mở rộng.

↓

### Biến chứng

Thấu hiểu trước đó trở nên không vững.

↓

### Hội tụ

Nhiều mạch bắt đầu nối với nhau.

↓

### Quyết định của hồi

Một hành động lớn của người chơi xảy ra.

↓

### Hệ quả

Trạng thái thế giới đổi.

↓

### Chuyển hồi

Hồi tiếp theo bắt đầu từ trạng thái mới.

---

# 32. Mật độ nhiệm vụ

Không phải khoảnh khắc nào cũng nên sinh ra một nhiệm vụ.

Mật độ nhiệm vụ nên xen kẽ với:

- khám phá;
- di chuyển;
- quan sát môi trường;
- tương tác NPC;
- những khoảnh khắc yên;
- quan sát trạng thái thế giới;
- các cảnh kể.

Quá nhiều nhiệm vụ tạo ra:

> **Nhiệm vụ hóa**

khi mọi tương tác giữa người với người đều trở thành một mục tiêu.

Veyloria nên cưỡng lại điều này.

---

# 33. Mẫu cần tránh: nhiệm vụ hóa

Xấu:

> NPC nhìn thấy người chơi.

> NHIỆM VỤ BẮT ĐẦU.

> Mang 3 vật phẩm.

> Quay về.

> NHIỆM VỤ HOÀN THÀNH.

Tốt hơn:

> NPC nói chuyện một cách tự nhiên.

> Người chơi nhận ra một điều bất thường.

> Người chơi điều tra.

> Một nhiệm vụ có thể có nảy ra từ sự tò mò của người chơi.

Cấu trúc thứ hai giữ sự chân thực của thế giới.

---

# 34. Phụ thuộc nhiệm vụ không thỏa

Khi một phụ thuộc không sẵn, hệ thống nên phân biệt:

### Chưa biết

Người chơi chưa khám phá thông tin liên quan.

### Chưa thể

Trạng thái thế giới ngăn tiến trình.

### Không còn thể

Hệ quả trước đó đã đóng cơ hội vĩnh viễn.

### Có lối khác

Một lối khác có thể thỏa cùng nhu cầu kể chuyện.

Điều này quan trọng cho cách kể do hệ quả dẫn.

---

# 35. Thất bại và phục hồi

Thất bại nhiệm vụ không nên tự động có nghĩa là:

> Tải lại mốc lưu.

Thất bại có thể tạo ra:

> **Trạng thái mới → Nhiệm vụ mới**

Ví dụ:

Người chơi không thuyết phục được một NPC.

Thay vì:

> NHIỆM VỤ THẤT BẠI

thế giới tạo ra:

> NPC không tin người chơi.

Điều này có thể mở khóa:

> **Tìm cách khác để có được thông tin.**

Vì vậy:

> **Thất bại có thể trở thành tiến trình.**

---

# 36. Nội dung bị lỡ

Một số nội dung có thể thực sự trở nên không còn sẵn.

Điều này chấp nhận được khi:

- cơ hội rõ ràng gắn với ngữ cảnh;
- hệ quả hiểu được;
- người chơi vẫn tiếp tục được;
- nội dung đã mất không chứa thấu hiểu bắt buộc.

Đôi khi thế giới nên truyền đạt:

> **Thời gian đã trôi.**

---

# 37. Phục hồi chuỗi nhiệm vụ

Khi một nhiệm vụ bắt buộc trở nên không sẵn, hệ thống nên thử:

1. Nhiệm vụ thay thế;
2. Bằng chứng thay thế;
3. NPC thay thế;
4. Lối thay thế;
5. Quay lại bị trì hoãn;
6. Cách diễn giải đã đổi.

Chỉ khi không cách nào thích hợp, mạch kể mới nên tách vĩnh viễn.

---

# 38. Cổng tiến trình

Cổng tiến trình nên thể hiện một trong bốn việc:

### Cổng hiểu biết

> Bạn cần hiểu một điều gì đó.

### Cổng quan hệ

> Ai đó phải tin cậy / nhận ra / hợp tác với bạn.

### Cổng thế giới

> Môi trường phải đổi.

### Cổng kể chuyện

> Một sự kiện câu chuyện lớn phải xảy ra.

Những cổng này được ưu tiên hơn:

> Cổng cấp.

---

# 39. Chặn theo cấp

Yêu cầu cấp truyền thống nên được giảm tối đa.

Tránh:

> Cấp yêu cầu: 15

trừ khi trò chơi thực sự cần một năng lực cơ chế.

Ưu tiên:

> Hiểu biết yêu cầu;
> Công cụ yêu cầu;
> Quan hệ yêu cầu;
> Trạng thái thế giới yêu cầu.

Người chơi nên hiểu vì sao tiến trình bị chặn.

---

# 40. Đơn vị tiến trình

Nguồn tiến trình chính của Veyloria mang tính khái niệm, hơn là thuần số.

Các trạng thái tiến trình có thể có:

- Hiểu biết;
- Lối vào;
- Tin cậy;
- Được nhận ra;
- Thấu hiểu;
- Trạng thái thế giới;
- Ký ức;
- Quan hệ.

Điểm kinh nghiệm truyền thống có thể tồn tại, nhưng không nên là ngôn ngữ tiến trình duy nhất.

---

# 41. Phần thưởng chuỗi nhiệm vụ

Một chuỗi nhiệm vụ nên dần đem lại:

### Ngay

- thông tin;
- lối vào;
- đổi quan hệ.

### Trung hạn

- nhiệm vụ mới;
- địa điểm mới;
- thế giới đã đổi;
- tương tác mới.

### Dài hạn

- diễn giải lại;
- tiến trình hồi;
- hệ quả lớn;
- thấu hiểu mới về nhân vật chính.

Điều này tạo tiến trình nhiều lớp.

---

# 42. Ví dụ trạng thái chuỗi nhiệm vụ

```text
QUEST A
  ↓
Người chơi khám phá ngôi nhà
  ↓
STATE: house_known
  ↓
QUEST B được mở khóa
  ↓
Người chơi điều tra cư dân
  ↓
STATE: resident_suspicious
  ↓
QUEST C sẵn có
  ↓
Người chơi quay lại ngôi nhà
  ↓
STATE: evidence_found
  ↓
QUEST D được mở khóa
  ↓
Tiết lộ lớn
  ↓
STATE: protagonist_identity_questioned
  ↓
Tiến trình hồi
```

Phần quan trọng là:

> **Hoàn thành nhiệm vụ đổi trạng thái.**

---

# 43. Ví dụ đồ thị phụ thuộc

```text
                   [Ngôi nhà được khám phá]
                              │
                              ↓
                   [Nói chuyện với cư dân]
                        /          \
                      /              \
                    ↓                  ↓
             [Đã có tin cậy]    [Đã nảy nghi ngờ]
                    │                  │
                    ↓                  ↓
            [Hội thoại riêng]  [Bằng chứng khác]
                    \                  /
                      \              /
                        ↓          ↓
                     [Quay lại ngôi nhà]
                              │
                              ↓
                      [Mâu thuẫn ký ức]
                              │
                              ↓
                        [Điều tra lớn]
```

Những trải nghiệm người chơi khác nhau hội tụ mà không trở thành giống hệt nhau.

---

# 44. Mẫu tài liệu chuỗi nhiệm vụ

Mọi chuỗi nhiệm vụ lớn cuối cùng nên xác định:

- Mã chuỗi;
- Tên chuỗi;
- Mục đích kể chuyện;
- Hồi;
- Chủ đề chính;
- Loại nhiệm vụ chính;
- Loại nhiệm vụ phụ;
- Điều kiện vào;
- Lối then chốt;
- Các lối tùy chọn;
- Các nút nhiệm vụ;
- Phụ thuộc;
- Điều kiện mở khóa;
- Điều kiện chặn;
- Nội dung song song;
- Các nhánh;
- Các điểm hội tụ;
- Thay đổi trạng thái thế giới;
- Đổi hiểu biết;
- Đổi quan hệ;
- Trạng thái thất bại;
- Các lối phục hồi;
- Các điểm quay lại;
- Hệ quả lớn;
- Hiểu lại;
- Điều kiện thoát;
- Chuỗi tiếp theo.

---

# 45. Mẫu nút nhiệm vụ

Mỗi nút nên chứa:

| Trường | Định nghĩa |
|---|---|
| Mã nhiệm vụ | Định danh duy nhất |
| Chuỗi cha | Chuỗi nhiệm vụ |
| Loại chính | Loại nhiệm vụ chính |
| Loại phụ | Các loại bổ trợ |
| Điều kiện vào | Điều làm nó sẵn có |
| Câu hỏi người chơi | Câu hỏi lõi |
| Mục tiêu | Sự rõ ngay lúc này |
| Hoạt động | Người chơi làm gì |
| Khám phá | Người chơi học được gì |
| Lựa chọn | Quyết định có nghĩa |
| Đổi trạng thái | Hiệu ứng tồn tại |
| Phản hồi của thế giới | Phản ứng ngay hoặc về sau |
| Hệ quả | Điều còn lại |
| Mở khóa | Khả năng mới |
| Chặn | Khả năng bị đóng |
| Ký ức | Thế giới nhớ gì |
| Quay lại | Liên quan về sau |
| Điều kiện thoát | Nút được giải quyết thế nào |

---

# 46. Kiểm tra chất lượng chuỗi nhiệm vụ

Trước khi duyệt một chuỗi:

### 1. Mỗi nhiệm vụ có lý do để tồn tại không?

### 2. Việc hoàn thành có đổi trạng thái có nghĩa không?

### 3. Nhiệm vụ tiếp theo có nảy ra một cách tự nhiên không?

### 4. Các phụ thuộc có hiểu được không?

### 5. Người chơi có thể tiếp cận một số nội dung theo những thứ tự khác nhau không?

### 6. Nhiệm vụ tùy chọn có đóng góp thông tin hoặc quan hệ có nghĩa không?

### 7. Các nhánh có nghĩa không?

### 8. Hội tụ có giữ các hệ quả trước đó không?

### 9. Thất bại có thể tạo một trạng thái mới không?

### 10. Chuỗi có tạo hiểu lại không?

### 11. Thế giới có nhớ hành động của người chơi không?

### 12. Chuỗi có cảm giác đúng chất Veyloria không?

---

# 47. Mẫu cần tránh của chuỗi nhiệm vụ

Bác các chuỗi trở thành:

### Chuỗi danh sách đánh dấu

> Hoàn thành A → B → C → D

mà không có đổi trạng thái có nghĩa.

### Chuỗi chìa khóa

> Nhiệm vụ A đưa chìa khóa cho B.  
> Nhiệm vụ B đưa chìa khóa cho C.

### Chuỗi cấp

> Cấp 5 → Nhiệm vụ A  
> Cấp 10 → Nhiệm vụ B  
> Cấp 15 → Nhiệm vụ C

### Chuỗi thuyết minh

> Hội thoại → Hội thoại → Cảnh dựng → Hội thoại.

### Nhánh giả

> Lựa chọn A / Lựa chọn B

nhưng cả hai tạo ra cùng một trạng thái.

### Chuỗi đặt lại

> Hệ quả trước đó biến mất khi nhiệm vụ tiếp theo bắt đầu.

### Bức tường nhiệm vụ

> Mười nhiệm vụ trở nên sẵn có cùng lúc, không có thứ bậc hoặc ngữ cảnh.

### Chuỗi nhiệm vụ phụ bắt buộc

> Câu chuyện chính bất ngờ đòi nội dung tùy chọn không liên quan.

---

# 48. Nguyên tắc bản sắc chuỗi nhiệm vụ

Một chuỗi nhiệm vụ tốt nên tạo cảm giác:

> **“Hành động của mình đã gây ra tình huống tiếp theo.”**

Không phải:

> **“Trò chơi giao cho mình nhiệm vụ tiếp theo.”**

Quan hệ lý tưởng là:

> **Hành động → Trạng thái → Khả năng**

thay vì:

> **Hoàn thành → Phần thưởng → Nhiệm vụ tiếp theo**

---

# 49. Triết lý tiến trình

Tiến trình của Veyloria vì vậy là:

> **Do trạng thái dẫn**

thay vì:

> **Do danh sách đánh dấu dẫn**

Người chơi tiến lên vì:

- họ đã khám phá một điều;
- họ đã hiểu một điều;
- có người tin họ;
- thế giới đã đổi;
- một quan hệ đã đổi;
- một lựa chọn trước đã tạo hệ quả;
- họ đã trở lại với hiểu biết mới.

---

# 50. Chuỗi nhiệm vụ và quyền chủ động của người chơi

Quyền chủ động tồn tại ở ba mức.

## Quyền chủ động tại chỗ

Người chơi làm gì ngay lúc này?

> Xem xét / nói chuyện / khám phá / chọn.

## Quyền chủ động trình tự

Người chơi theo đuổi gì tiếp theo?

> Ngôi nhà / cư dân / rừng / khu định cư.

## Quyền chủ động kể chuyện

Hành động của người chơi đổi điều gì?

> Tin cậy / lối vào / bằng chứng / quan hệ / trạng thái thế giới.

Những chuỗi nhiệm vụ mạnh của Veyloria nên cung cấp cả ba ở chỗ thích hợp.

---

# 51. Chuỗi nhiệm vụ và việc quay lại

Một chuỗi không nhất thiết kết thúc khi mục tiêu cuối đã hoàn thành.

Những nhiệm vụ quan trọng có thể vẫn:

> **Còn hoạt động về mặt kể chuyện**

vì thông tin về sau có thể diễn giải lại chúng.

Ví dụ:

> Nhiệm vụ A đã hoàn thành.

Về sau:

> Ký ức mới được khám phá.

Hệ thống đánh dấu:

> Nhiệm vụ A = Có thể hiểu lại.

Người chơi có thể quay lại địa điểm hoặc NPC.

---

# 52. Hoàn thành chuỗi

Một chuỗi có thể được xem là hoàn thành khi:

- câu hỏi kể chuyện của nó đã tới một giải quyết có nghĩa;
- trạng thái thế giới bắt buộc của nó đã được thiết lập;
- hệ quả lớn của nó đã xảy ra;
- trạng thái kể chuyện tiếp theo của nó đã sẵn có.

Hoàn thành không có nghĩa là:

> **Không còn điều gì liên quan đến chuỗi này có thể xảy ra nữa.**

Một chuỗi đã hoàn thành về sau có thể trở thành:

> **Nội dung được hiểu lại**

---

# 53. Công thức tiến trình chuẩn

Mô hình tiến trình của Veyloria là:

> **KHÁM PHÁ → THEO ĐUỔI → HÀNH ĐỘNG → ĐỔI TRẠNG THÁI → TẠO KHẢ NĂNG → CHỌN → TRẢI NGHIỆM HỆ QUẢ → HIỂU LẠI**

Công thức này thay thế:

> **NHẬN NHIỆM VỤ → HOÀN THÀNH MỤC TIÊU → NHẬN PHẦN THƯỞNG**

làm triết lý tiến trình chính.

---

# 54. Đầu ra 9.4

Mô hình chuỗi nhiệm vụ chuẩn là:

> **Nhiệm vụ → Đổi trạng thái → Phụ thuộc → Mở khóa → Lựa chọn người chơi → Trạng thái mới**

Các nhóm phụ thuộc chuẩn là:

1. Kể chuyện;
2. Hiểu biết;
3. Quan hệ;
4. Trạng thái thế giới;
5. Địa điểm;
6. Lựa chọn;
7. Tiến trình;
8. Hệ thống.

Các cấu trúc chuỗi chuẩn là:

1. Tuyến tính;
2. Phân nhánh;
3. Hội tụ;
4. Song song;
5. Giao nhau;
6. Được hiểu lại.

Nguyên tắc tiến trình chuẩn là:

> **Tiến trình là sự xuất hiện của những khả năng mới từ trạng thái tồn tại.**

---

# 55. Tiêu chí hoàn thành 9.4

9.4 hoàn thành khi mọi vòng câu chuyện lớn có thể được thể hiện thành một mạng nhiệm vụ trong đó:

- nhiệm vụ có những phụ thuộc có nghĩa;
- lựa chọn người chơi ảnh hưởng trạng thái;
- nội dung tùy chọn vẫn có nghĩa;
- nhiều nhiệm vụ có thể cùng tồn tại;
- các nhánh có thể hội tụ mà không xóa hệ quả;
- thất bại có thể tạo tiến trình mới;
- trạng thái thế giới dẫn sự sẵn có;
- hiểu biết có thể hoạt động như một cổng tiến trình;
- quan hệ có thể hoạt động như tiến trình;
- nhiệm vụ đã hoàn thành có thể được hiểu lại về sau.

Phép thử cuối là:

> **Người chơi có cảm thấy nhiệm vụ tiếp theo tồn tại vì điều họ đã làm, đã khám phá, đã hiểu, hoặc đã đổi không?**

Nếu có, chuỗi nhiệm vụ đã đạt mô hình tiến trình mà Veyloria hướng tới.

---

## Chuyển sang 9.5

> **9.5 — Trạng thái nhiệm vụ, mục tiêu và cách nhiệm vụ diễn ra khi chơi**
