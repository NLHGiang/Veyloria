# Veyloria — DNA V2 Proposal

> **Trạng thái:** Proposal — chưa canon.  
> Nội dung này là đề xuất để tranh luận/chốt, không tự động trở thành Veyloria V1 chính thức.

## 1. Core Fantasy

> **Bạn tỉnh dậy trong một thế giới mà chính bạn đã từng sống, nhưng thế giới không còn nhớ bạn theo cùng một cách mà bạn nhớ nó.**

Người chơi không đơn thuần khám phá Veyloria.

Người chơi khám phá **mối quan hệ giữa ký ức của mình và ký ức của thế giới**.

Cảm giác cốt lõi cần tạo ra:

> "Mình chắc chắn chuyện này đã xảy ra."

→

> "Nhưng tại sao không ai nhớ?"

→

> "Nếu thế giới nhớ khác mình thì cái nào mới là sự thật?"

→

> "Khoan... nếu ký ức của mình cũng sai thì sao?"

Đây nên là **core fantasy** của Veyloria.

---

# 2. Veyloria là gì?

Mình đề xuất Veyloria **không phải một thế giới fantasy bình thường**.

Nó là một thế giới có khả năng **lưu giữ dấu vết của những gì đã xảy ra**.

Không phải theo nghĩa:

> "Thế giới có AI và biết mọi thứ."

Mà giống một quy luật tự nhiên:

> **Mọi hành động đều để lại một "memory" trong thực tại.**

Con người nhớ bằng tâm trí.

Địa điểm nhớ bằng hình dạng.

Đồ vật nhớ bằng trạng thái.

Sinh vật nhớ bằng hành vi.

Thế giới nhớ bằng **World State**.

Và đôi khi...

**những ký ức đó mâu thuẫn với nhau.**

---

# 3. Memory không phải vật phẩm

Đây là nguyên tắc mình đề xuất giữ tuyệt đối.

Không có gameplay kiểu:

> Memory Fragment x 17/50.

Thay vào đó:

### Memory là thông tin.

Ví dụ:

Người chơi nhớ:

> "Ở đây từng có một cây cầu."

Thế giới hiện tại:

> Không có cây cầu.

NPC:

> "Cậu đang nói về cái gì?"

Một vài giờ gameplay sau:

> Người chơi tìm thấy một mảnh gỗ trong kho.

Description:

> "Một phần của cây cầu đã biến mất."

Không có popup:

> **MEMORY DISCOVERED**

Người chơi **tự ghép sự thật**.

---

# 4. World State là gameplay cốt lõi

Đây là điểm mình muốn đẩy mạnh hơn DNA hiện tại.

Mỗi khu vực không chỉ có:

```
map
NPC
items
quests
```

mà còn có:

```
WORLD STATE
```

Ví dụ:

```
Bridge:
    existed = false
    repaired_by = unknown
    remembered_by = villagers
    player_memory = true
```

Và có thể xảy ra:

```
player_memory != world_state
```

Đây chính là **Memory Conflict**.

---

# 5. Người chơi không biết mình đáng tin đến đâu

Đây là một thay đổi mình đề xuất khá mạnh.

Ban đầu người chơi mặc định:

> "Mình mất trí nhớ nên mình không biết sự thật."

Nhưng càng chơi:

> "NPC có thể sai."

Sau đó:

> "Thế giới có thể sai."

Cuối cùng:

> **"Ký ức của chính mình cũng có thể không đáng tin."**

Đây sẽ tạo thành mystery nhiều tầng.

### Tầng 1

**Tôi đã quên điều gì?**

### Tầng 2

**Thế giới đã quên điều gì?**

### Tầng 3

**Ai đang thay đổi ký ức?**

### Tầng 4

**Tại sao ký ức lại có thể thay đổi thực tại?**

### Tầng 5

**Nếu ký ức tạo ra thực tại, vậy "sự thật" có tồn tại không?**

Đây có thể là escalation chính của story.

---

# 6. The Forgotten One

Mình **chưa muốn chốt** nhân vật chính là người tốt.

Cũng chưa muốn chốt là người xấu.

Đề xuất:

> **The Forgotten One là người có liên quan trực tiếp đến biến cố làm Veyloria mất ổn định.**

Nhưng nhân vật đã tự mất ký ức.

Do đó người chơi cũng không biết:

```
Hero
?
Victim
?
Cause
?
Witness
?
Prisoner
?
Creator
?
Destroyer
?
```

Story sẽ từ từ loại bỏ từng khả năng.

Điểm hay là:

**người chơi đang điều tra chính mình.**

---

# 7. Một twist mình đề xuất

Có thể rất mạnh nếu:

> **The Forgotten One không mất ký ức hoàn toàn.**

Mà ký ức bị chia thành hai lớp:

### Conscious Memory

Những gì nhân vật nghĩ mình nhớ.

### World Memory

Những gì thế giới nhớ về nhân vật.

Hai thứ **không giống nhau**.

Ví dụ:

NPC:

> "Cậu đã cứu làng này."

Nhân vật:

> "Tôi chưa từng tới đây."

NPC khác:

> "Đừng tin hắn. Chính cậu đã thiêu rụi nó."

Và cả hai đều có bằng chứng.

Đây là kiểu mystery mình nghĩ rất phù hợp với DNA.

---

# 8. V01

Mình đề xuất **giữ V01**, nhưng nâng vai trò.

Không chỉ:

> pet đáng yêu.

Không chỉ:

> companion.

Mà V01 là một trong số ít sinh vật **không bị ảnh hưởng hoàn toàn bởi Memory Conflict**.

Nó có thể:

- nhớ người chơi;
- phản ứng với nơi người chơi từng đến;
- nhận ra NPC;
- phản ứng với những thứ mà người chơi không nhớ;
- dẫn người chơi đến những địa điểm quan trọng;
- đôi khi **phản ứng trái với World State hiện tại**.

Ví dụ:

Người chơi bước vào một căn nhà.

NPC:

> "Nhà này bỏ hoang 20 năm rồi."

V01 chạy thẳng lên tầng hai.

Nó đứng trước một căn phòng.

Cửa bị khóa.

Người chơi:

> "Mày biết chỗ này?"

V01 không mở được.

Nhưng nó ngồi chờ.

Đây là **storytelling không cần exposition**.

---

# 9. Creature

Mình không muốn creature chỉ là:

> monster / pet / combat unit.

Đề xuất chia creature theo **mối quan hệ với memory**.

Ví dụ:

### Rememberers

Nhớ được quá khứ.

### Forgetters

Không thể lưu giữ ký ức.

### Echoes

Lặp lại hành động từng xảy ra.

### Distortions

Bị Memory Conflict làm biến dạng.

### Anchors

Có khả năng giữ một trạng thái của thế giới không bị thay đổi.

Nếu hệ thống này hợp DNA, nó có thể trở thành nền tảng cho cả lore lẫn gameplay.

---

# 10. Farming

Không bỏ.

Nhưng **farming không phải core identity**.

Nó là:

> **World Interaction System**

Nó giúp người chơi có cảm giác:

> "Tôi đang sống ở đây."

Và sau đó chính điều này khiến Memory Conflict có sức nặng.

Ví dụ:

Ngày 1:

> Người chơi trồng một cây.

Ngày 5:

> Cây lớn.

Ngày 20:

> NPC nói:

> "Cây đó có từ trước khi cậu đến."

Người chơi:

> "Không."

→ Đây là lúc mechanic farming trở thành **story mechanic**.

---

# 11. Day / Night

Mình đề xuất giữ.

Nhưng không chỉ phục vụ crop.

Một số thứ chỉ tồn tại:

- ban ngày;
- ban đêm;
- trước khi ngủ;
- sau khi ngủ;
- sau một World State change.

Đặc biệt:

> **Sleep = Save + World Tick**

Nhưng đôi khi:

> **Sleep = Memory Transition**

Ví dụ:

Người chơi ngủ.

Ngày hôm sau:

> Một thứ đã thay đổi.

Không có explanation.

---

# 12. Session Structure

DNA hiện tại nói 10–15 phút/session.

Mình đồng ý, nhưng đề xuất:

### Micro-session

10–20 phút:

```
Discover
→ Investigate
→ Act
→ World reacts
```

### Chapter

3–6 micro-sessions.

### Arc

3–5 chapters.

### Main Story

4–6 arcs.

Như vậy game có thể rất dài nhưng từng session vẫn dễ chơi.

---

# 13. Gameplay Loop

Mình đề xuất core loop chính thức:

```
EXPLORE
   ↓
NOTICE
   ↓
QUESTION
   ↓
INTERACT
   ↓
CHANGE SOMETHING
   ↓
WORLD REMEMBERS
   ↓
DISCOVER CONTRADICTION
   ↓
QUESTION AGAIN
```

Đây là loop mình muốn Veyloria sở hữu.

Không phải:

```
Kill → Loot → Upgrade
```

và cũng không phải:

```
Farm → Sell → Upgrade
```

Hai thứ đó có thể tồn tại.

Nhưng **không phải identity**.

---

# 14. Combat

Mình đề xuất **chưa chốt combat là core**.

Nếu có combat:

> Combat phải có liên quan tới World/Memory.

Ví dụ creature không chết theo cách bình thường.

Hoặc:

> Người chơi đánh một Echo.

Sau khi thắng:

> NPC nhớ rằng người chơi chưa từng chiến đấu.

Hoặc:

> Killing một creature làm một khu vực thay đổi.

Nếu combat chỉ để:

> đánh quái → XP → level

thì mình đề xuất hạn chế.

---

# 15. Progression

Không muốn progression chỉ là:

```
Level 1
↓
Level 2
↓
Level 3
```

Mà nên có:

### Character progression

Ability.

### Knowledge progression

Người chơi **hiểu thế giới hơn**.

### Relationship progression

NPC / creature tin tưởng người chơi.

### World progression

Khu vực thay đổi.

### Memory progression

Người chơi ghép được nhiều mảnh sự thật.

Trong đó **Knowledge + Memory** mới là progression đặc trưng của Veyloria.

---

# 16. Quest

Quest nên có hai lớp.

### Surface Quest

Người chơi hiểu rõ phải làm gì.

> "Sửa máng nước."

### Hidden Narrative

Tại sao máng nước lại hỏng?

Ai làm?

Tại sao NPC nhớ khác nhau?

Tại sao V01 quan tâm?

→ Người chơi **không nhất thiết được giao quest này**.

Nó tự hình thành từ tò mò.

Đây rất hợp với nguyên tắc:

> **Gameplay clean — Story open-ended.**

---

# 17. NPC

NPC không nên chỉ có:

```
quest giver
shopkeeper
farmer
blacksmith
```

Mỗi NPC nên có:

```
Current belief
Past memory
Relationship with player
Knowledge
False belief
Secret
```

Hai NPC có thể nói hai phiên bản khác nhau về cùng một sự kiện.

Nhưng:

> **Không được random nonsense.**

Mỗi phiên bản phải có logic.

---

# 18. Story Theme

Mình đề xuất 4 theme chính:

### Memory

Ta là ai nếu không nhớ mình là ai?

### Identity

Ta được định nghĩa bởi ký ức của bản thân hay ký ức của người khác?

### Truth

Nếu mọi người nhớ khác nhau, sự thật nằm ở đâu?

### Consequence

Nếu thế giới nhớ những gì ta làm...

> **Ta có thực sự có thể chạy trốn khỏi những gì mình đã làm không?**

Theme cuối cùng có thể trở thành emotional core.

---

# 19. Một nguyên tắc cực kỳ quan trọng

## Không twist vì twist.

Veyloria rất dễ mắc bệnh:

> "Haha, tất cả đều là ký ức!"

> "Haha, NPC thực ra là..."

> "Haha, thế giới thực ra..."

Mình đề xuất đặt rule:

> **Mọi twist phải làm thay đổi cách người chơi hiểu ít nhất một hành động mình đã từng thực hiện.**

Ví dụ:

Chapter 1:

> Người chơi sửa cây cầu.

Chapter 20:

> Phát hiện cây cầu đó đáng lẽ không được sửa.

→ Người chơi quay lại nhớ:

> "Khoan... vậy tại sao mình lại có quest sửa nó?"

Twist tốt nhất là twist khiến **quá khứ của người chơi thay đổi ý nghĩa**, chứ không chỉ thêm thông tin mới.

---

# 20. Những thứ mình đề xuất KHÔNG canon

Tạm thời chưa chốt:

- 7 nguyên thủy stones.
- 8 quốc gia.
- hệ thống evolution B/A/S/Ultimate.
- nguồn gốc chính xác của Veyloria.
- bản chất thực thể đen.
- nguyên nhân mất memory.
- ending.
- phe phái.
- hệ thống combat.
- tên Greenwake.
- tên Brackenwood.

Tất cả có thể được giữ làm **candidate ideas từ prototype**, nhưng chưa đóng đinh.

---

# 21. DNA V2 cô đọng thành một câu

Nếu phải viết trên đầu Game Design Document, mình đề xuất:

> **Veyloria is a story-driven exploration game about a forgotten person living in a world that remembers differently — where the player's actions alter not only the world, but the memories that define what the world believes to be true.**

Hoặc bản tiếng Việt:

> **Veyloria là một game phiêu lưu khám phá kể về một người đã bị lãng quên trong một thế giới vẫn còn nhớ — nơi hành động của người chơi không chỉ thay đổi thế giới, mà còn thay đổi ký ức định nghĩa thế giới đó.**

---

## Và có một quyết định mình muốn bạn chốt trước khi sang Story Bible

Mình thấy có **3 hướng rất khác nhau** cho Veyloria:

**A — Mystery / Psychological**  
Nặng điều tra, ký ức sai lệch, identity, NPC contradiction. Gameplay nhẹ hơn.

**B — Adventure / Cozy Mystery**  
Giữ farming, pet, village, exploration làm lớp ngoài; bên dưới là mystery về memory. Đây là hướng cân bằng nhất với prototype hiện tại.

**C — Fantasy RPG / Reality Mystery**  
Có combat, creature, nhiều vùng đất, progression lớn; Memory System là hệ thống đặc trưng xuyên suốt.

**Cá nhân mình nghiêng về B → dần mở sang C.**

Tức là **ban đầu Veyloria trông như một game phiêu lưu/farming dễ tiếp cận**, người chơi yêu V01, NPC và thế giới; sau đó từng chút một nhận ra **có thứ gì đó rất sai với thế giới này**. Đến giữa game, mystery trở thành trọng tâm.

Nếu bạn chốt hướng này, bước kế tiếp mình sẽ làm **Story Bible của Veyloria**, trước khi viết một dòng kịch bản dài.
