# 8.4 — World State & Memory Architecture

## 8.4.1 — Core Principle

> **The world does not merely change. It remembers why it changed.**

World State không chỉ lưu hiện trạng. Memory lưu lịch sử và interpretation của hiện trạng.

> **State ≠ Memory.**

## 8.4.2 — Four Layers of Memory

### ① Physical Memory
Thế giới nhớ bằng vật chất: căn nhà bị cháy, cây bị chặt, cửa bị phá, vật thể bị di chuyển, địa điểm được sửa chữa.

### ② Social Memory
Con người nhớ player và các sự kiện. Social Memory có thể mâu thuẫn.

### ③ Personal Memory
Player nhớ về chính mình. Player có thể tin một điều trong khi evidence cho thấy điều khác.

### ④ World Memory
World ghi nhận ý nghĩa mà event để lại, không chỉ event itself.

## 8.4.3 — Memory Is Not Truth

> **Memory is evidence, not absolute truth.**

Memory có thể đúng, sai, thiếu, bị diễn giải sai hoặc mâu thuẫn với memory khác.

> **CONTRADICTION = INVESTIGATION OPPORTUNITY**

## 8.4.4 — Event-Based World State

World State nên được xây quanh events thay vì chỉ boolean flags.

Một event nên có thể tạo ra nhiều state độc lập, ví dụ player cứu NPC A có thể khiến NPC A sống, NPC B tin player, NPC C distrust player và future events thay đổi.

## 8.4.5 — Causal Memory

Mỗi significant action có causal chain:

> **ACTION → EVENT → STATE CHANGE → MEMORY → CONSEQUENCE → FUTURE STATE**

Game không cần cho player thấy toàn bộ chain ngay lập tức. Một phần có thể được phát hiện nhiều giờ sau.

## 8.4.6 — Who Can Remember?

Memory có thể thuộc về:

### World-level
- locations;
- settlements;
- important objects;
- factions.

### Character-level
- NPCs;
- companions;
- important enemies;
- witnesses.

### Player-level
- known facts;
- personal memories;
- assumptions;
- discovered contradictions.

### System-level
- major events;
- persistent consequences;
- narrative flags.

## 8.4.7 — Memory Granularity

### Local Memory
Một NPC hoặc địa điểm nhớ.

### Regional Memory
Một cộng đồng nhớ.

### World Memory
Một sự kiện trở thành một phần lịch sử của Veyloria.

Không phải mọi action đều cần đạt World Memory.

## 8.4.8 — Persistent vs Temporary State

### Temporary
- NPC đang ở đâu;
- cửa đang mở;
- object đang được cầm;
- trạng thái combat.

### Persistent
- NPC đã chết;
- nhà đã cháy;
- player đã phản bội một nhân vật;
- sự thật đã được phát hiện;
- faction attitude đã thay đổi.

### Historical
Không còn trực tiếp ảnh hưởng hiện tại nhưng vẫn tồn tại như memory và có thể được nhắc lại.

## 8.4.9 — Memory Decay

Memory có thể được conceptualize:

> **Momentary → Recent → Persistent → Historical**

Memory decay chủ yếu phục vụ simulation và authenticity. Gameplay-critical memories không được biến mất chỉ vì thời gian trôi qua.

## 8.4.10 — Contradictory Memories

Ví dụ:

> PLAYER MEMORY: “I never entered the house.”

> WORLD EVIDENCE: Your belongings are inside.

> NPC MEMORY: “You lived here.”

> PHYSICAL MEMORY: A room has been preserved for you.

Game không lập tức xác nhận memory nào đúng. Contradiction trở thành gameplay.

## 8.4.11 — Memory Ownership

Một memory cần biết:

- WHO remembers?
- WHAT is remembered?
- WHEN did it happen?
- WHERE did it happen?
- HOW certain is the memory?
- HOW was it acquired?

Conceptual model:

> **MEMORY = Subject + Event + Source + Time + Location + Interpretation + Confidence + Consequences**

## 8.4.12 — Memory Source

Memory có thể đến từ:

- **Direct** — firsthand witness;
- **Testimony** — nghe người khác kể;
- **Artifact** — tài liệu / vật chứng;
- **Environment** — dấu vết vật lý;
- **Rumor** — thông tin truyền miệng;
- **Player Memory** — điều player tin rằng mình đã trải qua.

Các nguồn có độ tin cậy khác nhau.

## 8.4.13 — World Response

Khi significant event xảy ra:

> **PLAYER ACTION → EVENT CREATED → WORLD STATE UPDATED → MEMORY DISTRIBUTED → CONSEQUENCE PROPAGATED**

Propagation phải có giới hạn. Một hành động nhỏ không được khiến toàn bộ Veyloria thay đổi.

## 8.4.14 — Consequence Radius

### Immediate
Ảnh hưởng ngay tại interaction.

### Local
Ảnh hưởng NPC / location.

### Regional
Ảnh hưởng community / faction.

### Long-Term
Xuất hiện rất lâu sau.

### Historical
Trở thành một phần identity của world.

Một hành động có thể nhỏ ở hiện tại nhưng lớn trong ký ức.

## 8.4.15 — Player Memory vs World Memory

> **Player's memory and the world's memory are separate systems.**

Player có thể nhớ:

> “I saved him.”

World có thể nhớ:

> “He died.”

Gameplay bắt đầu từ khoảng cách đó.

## 8.4.16 — Save / Load Principle

Save/load phải bảo toàn causal world state:

- significant events;
- NPC memories;
- persistent consequences;
- discovered information.

Không được để load game làm mất persistent consequences, trừ khi đó là chủ đích của một mechanic cụ thể.

## 8.4.17 — Core Rules

> **Every significant player action creates a memory somewhere.**

> **Not every memory has to be visible immediately.**

> **Not every memory has to be true.**

## 8.4.18 — 8.4 Locked Direction

### WORLD STATE
> **What is true now.**

### MEMORY
> **What the world believes happened.**

### PLAYER MEMORY
> **What the player believes happened.**

### TRUTH
Truth không mặc định bằng bất kỳ lớp nào ở trên.

> **PLAYER MEMORY ↔ CONTRADICTION ↔ WORLD MEMORY ↔ EVIDENCE ↔ WORLD STATE → CONSEQUENCE → FUTURE WORLD**

## 8.4 North Star

> **The world remembers actions, people remember interpretations, and the player must discover where memory diverges from truth.**
