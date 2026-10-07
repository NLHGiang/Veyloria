# 8.8 — Gameplay-to-Story Integration

## 8.8.1 — Core Integration Philosophy

Screenplay và gameplay không phải hai hệ thống song song.

> **STORY INTENT → PLAYER SITUATION → PLAYER ACTION → WORLD RESPONSE → PLAYER DISCOVERY → STORY MEANING**

Story cung cấp **meaningful situations**. Gameplay cung cấp **agency inside those situations**.

## 8.8.2 — Story Beat → Gameplay Beat

Mỗi screenplay beat có thể được chuyển thành:

1. **PLAY** — Player trực tiếp thực hiện hành động.
2. **OBSERVE** — Player phải nhìn thấy / nhận ra event.
3. **INVESTIGATE** — Story information trở thành mystery.
4. **CHOOSE** — Story beat trở thành decision.
5. **CONSEQUENCE** — Story beat được thể hiện sau player action.

> **Important story ≠ automatically cutscene.**

## 8.8.3 — Story Beat Conversion Matrix

| Story Beat | Gameplay Form |
|---|---|
| Character reveals information | Investigate / Dialogue |
| Character hides information | Investigate / Observe |
| Player discovers location | Explore |
| Player learns fact | Knowledge Unlock |
| Character changes opinion | Social Memory |
| Player makes decision | Choice |
| Decision affects world | World State |
| Past action returns | Revisit |
| Contradictory memory appears | Investigation |
| Major truth revealed | Recontextualization |

## 8.8.4 — The Player Must Own the Discovery

Nếu player có thể tự phát hiện, game không nên nói thay player.

Major identity / memory / truth revelations nên ưu tiên **player discovery hoặc inference**.

## 8.8.5 — Exposition Budget

Information có thể được:

- **SHOW**
- **LET PLAYER DISCOVER**
- **LET PLAYER INFER**
- **TELL**

Ưu tiên:

> **INFER > DISCOVER > SHOW > TELL**

Không phải mọi information đều cần infer, nhưng core mystery nên được player experience thay vì nhận exposition trực tiếp.

## 8.8.6 — Story as Evidence

Story information nên trở thành evidence.

Ví dụ một event có thể được thể hiện qua:

- dấu vết;
- object;
- NPC testimony;
- document;
- environmental state;
- conflicting dates.

Player phải tự hỏi:

> **“Which memory is correct?”**

## 8.8.7 — Contradiction as Gameplay

> **Memory ≠ Truth**

Contradiction phải trở thành playable question.

Ví dụ:

- NPC A: player đã cứu họ.
- NPC B: player đã bỏ rơi họ.
- Player Memory: không nhớ cả hai.

Không resolve ngay. Contradiction tạo investigation.

## 8.8.8 — Character Arc → Gameplay Relationship

Character development không nên chỉ nằm trong dialogue.

> **PLAYER ACTION → NPC MEMORY → NPC BELIEF → NPC BEHAVIOR → PLAYER DISCOVERY**

Character arc phải có thể được **played**, không chỉ watched.

## 8.8.9 — Screenplay Scene → Playable Situation

Chuyển:

> **“What happens?”**

thành:

> **“What situation does the player enter?”**

Một scene tuyến tính có thể trở thành player-authored experience nếu player có thể observe, investigate, interact, leave, return và interpret.

## 8.8.10 — Protecting Story Beats

### Fixed Beat
Không thay đổi; thường là canonical world truth.

### Variable Beat
Meaning giống nhau nhưng expression có thể thay đổi.

### Emergent Beat
Phát sinh từ player action.

Veyloria ưu tiên **Variable + Emergent** ở gameplay layer.

## 8.8.11 — Canon vs Player Memory

Phân biệt:

### Canonical Truth
Điều thực sự xảy ra trong world model.

### Character Memory
NPC tin điều gì đã xảy ra.

### Player Memory
Player tin điều gì đã xảy ra.

### Player Interpretation
Player hiện đang suy luận điều gì.

Bốn lớp này không bắt buộc giống nhau.

## 8.8.12 — Major Reveal Design

Major reveal lý tưởng:

> **OLD MEMORY → NEW EVIDENCE → CONTRADICTION → REINTERPRETATION → PLAYER REALIZES → OLD EVENTS CHANGE MEANING**

Player không chỉ learn new information.

> **Player must reinterpret old information.**

## 8.8.13 — Act Structure → Gameplay Structure

> **ACT → THEMATIC QUESTION → GAMEPLAY QUESTION → QUEST CLUSTER → WORLD STATE CHANGES → MEMORY CONSEQUENCES → ACT RECONTEXTUALIZATION**

Một Act là một giai đoạn trong **understanding progression**, không nhất thiết là một gameplay chapter tuyến tính.

## 8.8.14 — Gameplay Should Carry Narrative Weight

Gameplay action có thể có mechanical complexity thấp nhưng narrative meaning cao.

> **Low mechanical complexity, high narrative meaning.**

## 8.8.15 — Narrative Actions vs Mechanical Actions

### Mechanical Action
- Walk
- Jump
- Open
- Pick up

### Narrative Action
- Believe
- Accuse
- Hide
- Reveal
- Forgive
- Refuse
- Investigate
- Revisit

Veyloria cần:

> **Mechanical actions as vehicles for narrative actions.**

## 8.8.16 — Cutscene Rule

Cutscene chỉ nên dùng khi:

1. Information không thể gameplay hóa tốt.
2. Cần bảo vệ major canonical beat.
3. Cần pacing / emotional transition.
4. Event cần xảy ra độc lập với player action.

Không dùng cutscene chỉ vì information quan trọng.

## 8.8.17 — Story-Gated vs Understanding-Gated

Traditional:

> **Reach Level 10 → Unlock Story**

Veyloria:

> **Understand X → Recognize Y → Gain ability to interact with Z**

Feedback loop:

> **STORY → KNOWLEDGE → UNDERSTANDING → NEW INTERACTION → NEW STORY POSSIBILITY**

## 8.8.18 — No Narrative Orphan

Mọi major story event nên có ít nhất một gameplay footprint:

- world state;
- NPC memory;
- object;
- location;
- dialogue;
- quest;
- future consequence.

Ngược lại, significant gameplay action cũng nên có khả năng tạo narrative footprint.

> **Gameplay happened, but story never remembers it** là anti-pattern.

## 8.8.19 — Story Integration Test

Mỗi story beat cần trả lời:

1. Player có làm gì không?
2. Player có hiểu gì không?
3. Player có lựa chọn không?
4. World có nhớ không?
5. Beat có thể tạo contradiction không?
6. Beat có thay đổi interpretation không?

Nếu không có meaningful answer, cần xem lại narrative/gameplay integration.

## 8.8.20 — Gameplay-to-Story Pipeline

> **SCREENPLAY BEAT → THEMATIC INTENT → PLAYER SITUATION → PLAYER INTERACTION → PLAYER INTERPRETATION → PLAYER ACTION → WORLD RESPONSE → MEMORY → CONSEQUENCE → STORY RECONTEXTUALIZATION**

Đây là cầu nối giữa **Step 7 — Screenplay** và **Step 8 — Gameplay Adaptation**.

## 8.8.21 — 8.8 Locked Direction

### STORY ROLE
> **Provide meaningful situations and questions.**

### GAMEPLAY ROLE
> **Give the player agency inside those situations.**

### PLAYER ROLE
> **Discover, interpret, choose, act.**

### STORY DELIVERY
> **Infer > Discover > Show > Tell**

### MAJOR REVEALS
> **Recontextualization, not exposition dump.**

### CHARACTER ARCS
> **Must be reflected in memory, behavior, and consequence.**

### CANON
> **Canonical truth is separate from player / NPC memory.**

### CUTSCENES
> **Support gameplay; do not replace discoverable gameplay.**

### INTEGRATION RULE
> **Every major story event leaves a gameplay footprint, and every significant gameplay action can leave a narrative footprint.**

## 8.8.22 — North Star

> **The player should not merely watch Veyloria's story happen. The player should cause events, interpret what they mean, and later discover that the world remembers them differently.**

### Quan hệ 8.7 → 8.8

> **SESSION → PLAYER ACTION → STORY EVENT → WORLD RESPONSE → MEMORY → FUTURE SESSION → RECONTEXTUALIZATION**

