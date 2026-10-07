# 8.3 — Player Interaction Model

## 8.3.1 — Mục tiêu

8.3 định nghĩa cách người chơi thực sự tương tác với Veyloria.

Nếu 8.1 trả lời **Player đang cố làm gì?** và 8.2 trả lời **Game có những hệ thống nào để hỗ trợ việc đó?**, thì 8.3 trả lời **Player làm những việc đó bằng cách nào, và game phản hồi ra sao?**

Interaction model của Veyloria không được biến thành một adventure game point-and-click đơn thuần. Người chơi phải cảm thấy mình đang đọc một thế giới sống, chứ không phải chỉ tìm đúng object để kích hoạt đúng dialogue.

## 8.3.2 — Interaction Philosophy

Interaction trong Veyloria xoay quanh 5 hành động:

> **OBSERVE → INVESTIGATE → INTERACT → CHOOSE → REMEMBER**

- **Observe** — nhìn và nhận biết.
- **Investigate** — đặt câu hỏi và thu thập bằng chứng.
- **Interact** — tác động vào người, vật, địa điểm hoặc hệ thống.
- **Choose** — quyết định hành động.
- **Remember** — thế giới ghi nhận hành động đó.

Remember không phải action button. Nó là hậu quả của tất cả các action phía trước.

## 8.3.3 — Layer 1: OBSERVE

Player có thể:

- nhìn môi trường;
- đọc spatial clues;
- nhận biết object bất thường;
- quan sát NPC;
- nhận biết thay đổi trong environment;
- phát hiện những thứ không khớp với ký ức hiện tại.

Environment phải tạo ra câu hỏi thay vì liên tục nói “Press E to investigate”.

> **“Tại sao thứ này lại ở đây?”**

Sự mâu thuẫn chính là invitation để interact.

## 8.3.4 — Layer 2: INVESTIGATE

Investigation biến observation thành gameplay.

Player có thể:

### Examine
Kiểm tra object, environment, dấu vết, tài liệu, hình ảnh, địa điểm, NPC reaction.

### Compare
Đặt các nguồn thông tin cạnh nhau:

> NPC A nói X.  
> Document nói Y.  
> Environment cho thấy Z.

### Question
Hỏi NPC hoặc hệ thống về một thông tin cụ thể.

### Revisit
Quay lại địa điểm sau một thay đổi.

Một địa điểm không nhất thiết chỉ được thiết kế để khám phá một lần.

## 8.3.5 — Layer 3: INTERACT

Interaction quan trọng phải có khả năng thuộc một trong ba loại:

### A. Reveal
Giúp player biết thêm.

### B. Alter
Thay đổi trạng thái thế giới.

### C. Contradict
Tạo ra hoặc làm rõ mâu thuẫn.

Loại C là interaction đặc trưng nhất của Veyloria.

## 8.3.6 — Layer 4: CHOOSE

Choice trong Veyloria không nên chủ yếu là Good / Evil hoặc A / B dialogue option.

Choice nên trả lời:

> **“Player tin điều gì đủ để hành động?”**

Có thể có:

- tin một nhân vật;
- tin một ký ức;
- tin bằng chứng vật lý;
- từ chối quyết định;
- hành động dù chưa chắc chắn;
- chấp nhận một phiên bản sự thật.

> **Uncertainty itself becomes part of decision-making.**

## 8.3.7 — Interaction Feedback

Mỗi interaction quan trọng cần tạo ra ít nhất một dạng feedback.

### Immediate Feedback
Player biết mình vừa làm gì: object thay đổi, NPC phản ứng, animation, dialogue, sound hoặc environmental change.

### Knowledge Feedback
Player hiểu mình vừa biết thêm gì: memory fragment, contradiction hoặc connection.

### World Feedback
Player nhận thấy thế giới đã thay đổi: NPC nhớ player khác đi, địa điểm thay đổi, nhân vật xuất hiện/biến mất hoặc dialogue thay đổi.

### Delayed Feedback
Player làm việc đó từ lâu nhưng bây giờ thế giới mới cho thấy hậu quả.

Đây là nơi **The World Remembers** trở thành gameplay.

## 8.3.8 — Interaction State Model

Mỗi interaction quan trọng có thể được mô hình hóa:

**PLAYER INTENT → ACTION → WORLD RESPONSE → MEMORY RECORD → FUTURE STATE → PLAYER DISCOVERY**

Ví dụ:

> Player tin NPC A  
> ↓  
> Player giúp NPC A  
> ↓  
> NPC A sống sót  
> ↓  
> World ghi nhận player là người đã giúp  
> ↓  
> NPC khác nhớ player theo cách khác  
> ↓  
> Player quay lại sau này  
> ↓  
> phát hiện một phiên bản quá khứ mà chính mình không nhớ.

Đây là interaction model cốt lõi.

## 8.3.9 — Không có “Wrong Interaction”

Player không nên bị phạt chỉ vì đã tương tác theo cách designer không dự đoán.

Veyloria không nên có:

- một puzzle chỉ có một đáp án;
- một NPC chỉ phản ứng với một câu trả lời;
- một object chỉ tồn tại để player tìm đúng sequence;
- game over vì một lựa chọn narrative nhỏ.

Sai lầm trở thành memory của thế giới.

Nếu player tin nhầm người, bỏ qua một nhân vật, phá hủy một vật hoặc đưa thông tin sai, game không nói “Wrong”.

> **“Now Veyloria remembers that you did this.”**

## 8.3.10 — Player Agency Model

Agency của Veyloria có 3 tầng:

### ① Physical Agency
Player có thể di chuyển, quan sát, lấy, sử dụng, nói chuyện và tác động môi trường.

### ② Investigative Agency
Player quyết định muốn tìm hiểu điều gì: ai đúng, chuyện gì xảy ra, tại sao world nhớ khác nhau và quá khứ của chính mình.

### ③ Interpretive Agency
Player quyết định mình tin điều gì.

Đây là tầng agency quan trọng nhất.

Game không nhất thiết phải nói cho player “Đây là sự thật”. Player tự xây dựng interpretation từ evidence, memory, testimony, consequence và contradiction.

## 8.3.11 — Interaction Hierarchy

> **LOOK → NOTICE → EXAMINE → QUESTION → CONNECT → ACT → WORLD REMEMBERS → REVISIT → DISCOVER CONTRADICTION**

Không phải mọi interaction đều cần đi hết chuỗi. Interaction quan trọng nên có khả năng tạo ra chuỗi này.

## 8.3.12 — NPC Interaction

NPC không chỉ là:

> quest giver → dialogue → quest complete

NPC phải có:

**Memory of Player**

và:

**Belief about Player**

Hai thứ này không nhất thiết giống nhau.

Ví dụ:

> NPC A: “You saved me.”  
> NPC B: “You abandoned me.”

Cả hai có thể cùng tồn tại.

Player không được biết ngay NPC nào đúng. Player phải investigate contradiction.

## 8.3.13 — Environmental Interaction

Environment là một narrative interface.

Player phải có thể đọc:

- placement;
- absence;
- damage;
- restoration;
- repetition;
- traces;
- changed objects.

Một căn phòng sau khi player quay lại có thể nói:

> **“Something happened here.”**

mà không cần dialogue giải thích.

> **World State is UI.**

## 8.3.14 — Core Interaction Rule

> **The player should rarely interact with something merely to progress.**

> **The player interacts because they are curious, uncertain, or trying to change something.**

Progression xảy ra sau interaction, không phải là lý do duy nhất để interaction tồn tại.

## 8.3.15 — Interaction Anti-Patterns

Veyloria cần tránh:

- **Object Hunt** — tìm 5 object để mở cửa.
- **Dialogue Dump** — NPC nói dài để giải thích lore.
- **Binary Moral Choice** — Good / Evil.
- **Fake Choice** — lựa chọn nhưng kết quả giống hệt nhau và không có memory consequence.
- **Quest Marker Dependency** — chỉ biết phải làm gì vì waypoint.
- **Puzzle Detached From Story** — puzzle không liên quan memory, identity hoặc contradiction.
- **Interaction Without Consequence** — player làm nhiều thứ nhưng thế giới không phản ứng.

## 8.3.16 — 8.3 Locked Direction

### PLAYER INTERACTION MODEL

**Primary interaction verbs:**

> **Observe → Investigate → Interact → Choose → Revisit**

**Primary interaction target:**

> **World + People + Evidence + Memory**

**Primary player agency:**

> **Decide what to believe, then act on that belief.**

**Primary feedback:**

> **Immediate → Knowledge → World State → Delayed Consequence**

**Primary design principle:**

> **There are no “wrong” narrative actions. There are only actions Veyloria remembers differently.**

**Signature interaction:**

> **Do something now. Discover much later how the world remembers it.**

## 8.3.17 — Quan hệ với 8.1 và 8.2

8.1 — Player Fantasy  
↓  
The Forgotten One  
↓  
8.2 — Gameplay Systems & Mechanics  
↓  
Memory / Investigation / World State / NPC Belief / Consequence / Contradiction  
↓  
8.3 — Player Interaction Model  
↓  
Observe → Investigate → Interact → Choose → World Remembers → Revisit → Discover Contradiction

8.3 xác định interaction grammar của Veyloria.
