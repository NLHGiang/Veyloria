# Veyloria

> **Cách chơi rõ — câu chuyện chưa kể hết.**

Veyloria là một thế giới nơi những gì được nhớ, bị quên hoặc bị thay đổi có thể tác động trực tiếp đến thực tại.

Người chơi không cần liên tục được nhắc rằng đây là một game về ký ức. Thay vào đó, họ **trải nghiệm những thay đổi của thế giới trước**, rồi dần ghép nối ý nghĩa của chúng.

---

## Ngôn ngữ

Ba ngăn. Thiết kế, thứ tự đọc và hồ sơ Minipower đều tiếng Việt. ID của hồ sơ Minipower giữ tiếng Anh.

| Ngăn | Ngôn ngữ | Gồm |
|---|---|---|
| Thiết kế | Tiếng Việt | Ý tưởng, cách chơi, bản đồ, nguyên tắc, quyết định, nền câu chuyện, bản gom ý |
| Thứ tự đọc | Tiếng Việt | 04 hướng làm việc đến 09 ánh xạ nội dung, gồm 08.01–08.10 và 09.01–09.10 |
| Hồ sơ Minipower | Tiếng Việt, ID giữ tiếng Anh | `00-governance/` … `06-changes/`, mở từ [mục lục khung](README.md) |

Tên riêng giữ nguyên: **Veyloria**, **V01**, **The Forgotten One**, **The World Remembers**, **The Bridge**, tên nhân vật và tên địa danh. Mã định danh (`DOC-xx`, `QUEST-###`, `TRACE-###`) và khóa trạng thái trong khối mã giữ nguyên.

## Tài liệu thiết kế

Trang này là cửa vào. Đọc từ **ý tưởng → cách chơi → thế giới → từng bản đồ nhỏ**.

### Ý tưởng

Những tài liệu định nghĩa Veyloria là gì, nhân vật là ai và ý tưởng chính của thế giới vận hành ra sao.

- **[Tổng quan](design/concept/overview.md)**  
  Ý tưởng Veyloria, hướng trải nghiệm và câu hỏi trung tâm.

- **[The Forgotten One](design/concept/the-forgotten-one.md)**  
  Nhân vật chính, quá khứ chưa biết, mất ký ức và những cách khác nhau mà thế giới nhớ về nhân vật.

- **[Cơ chế chính](design/concept/core-mechanic.md)**  
  Ký ức nằm phía sau thế giới và làm thế giới đổi.

- **[The World Remembers](design/knowledge-brainstorm.md#4-cơ-chế-đặc-trưng--the-world-remembers)**  
  Cơ chế đặc trưng: hành động → thế giới ghi nhớ → ký ức lệch nhau → người chơi muốn biết tiếp.

### Cách chơi

Các nguyên tắc quyết định người chơi sẽ chơi như thế nào.

- **[Một phiên chơi](design/gameplay/session-design.md)**  
  Cấu trúc một phiên 10–15 phút: một vấn đề, một hành động chính, một thay đổi của thế giới.

- **[Pet](design/gameplay/pet.md)**  
  Pet gợi ý tự nhiên, không thành dấu nhiệm vụ.

### Bản đồ

- **[The Bridge](design/maps/bridge.md)**  
  Bản đồ mẫu: một vấn đề, một hành động, một thay đổi của thế giới, và một lớp chuyện chưa giải thích.

### Quyết định

- **[Đề xuất DNA](design/decisions/dna-proposal.md)**  
  Bản để tranh luận. Chưa chốt.

- **[Hướng làm việc](design/decisions/04-working-direction.md)**  
  Quyết định mới được ghi thẳng vào các tài liệu hiện tại.

- **[Bước 5 — Thế giới](design/decisions/05-world-premise-themes-core-fantasy.md)**  
  Thế giới, tiền đề, chủ đề và cảm giác chính khi chơi. Đang làm, chờ chốt.

### Câu chuyện

- **[Nền câu chuyện](design/story/06-story-bible.md)**  
  Phần gốc của câu chuyện: nhân vật, V01, tiến trình, bí ẩn, cảm xúc và phần chưa chốt.

### Nguyên tắc và bản gom ý

- **[Nguyên tắc thiết kế](design/design-principles.md)**  
  Cách chơi rõ, câu chuyện chưa kể hết, mỗi phiên một vấn đề, thế giới phải đáp lại.

- **[Bản gom ý](design/knowledge-brainstorm.md)**  
  Nguồn tham chiếu gom ý. Không rút thành bản tóm tắt.

---

## Cơ chế đặc trưng

### The World Remembers

Điểm đặc trưng của Veyloria không chỉ là ký ức làm đổi thế giới, mà là:

> **Thế giới ghi nhớ những gì người chơi đã làm — nhưng không nhất thiết theo cách người chơi nhớ.**

Cơ chế này có 3 tầng:

**Hành động → Thế giới ghi nhớ → Ký ức lệch nhau**

#### 1. Hành động

Mỗi phiên có một hành động rõ ràng.

> Vấn đề → Hành động → Thế giới đổi → Hết phiên.

#### 2. Thế giới ghi nhớ

Hành động không kết thúc cùng phiên.

NPC, bản đồ, vật thể, pet hoặc khu vực khác có thể phản ứng với hành động đó ở những phiên sau.

#### 3. Ký ức lệch nhau

Thế giới có thể ghi nhớ một phiên bản khác với điều người chơi nhớ.

> **"Ủa? Mình nhớ là mình đã làm khác mà?"**

Đây là lớp tạo ra câu hỏi mới và động lực để người chơi tiếp tục khám phá.

---

## Tóm tắt thiết kế

### Phiên chơi

**10–15 phút mỗi phiên**

Mỗi bản đồ nhỏ tập trung vào:

> **Một vấn đề → Một hành động chính → Một thay đổi của thế giới**

### Cách chơi

Người chơi luôn cần hiểu:

- Mình đang ở đâu?
- Ở đây có vấn đề gì?
- Mình cần làm gì?
- Khi nào phiên hoàn thành?

### Câu chuyện

Không cần giải thích toàn bộ.

Người chơi có thể bắt gặp:

- những vật thể không khớp với hiện tại;
- dấu vết bất thường;
- NPC nhớ khác nhau;
- địa điểm thay đổi trạng thái;
- những chi tiết chỉ có ý nghĩa về sau.

### Pet

Pet là một phần của cách chơi.

> **Không chỉ đi cùng. Nó có thể khiến người chơi nhận ra rằng một nơi đáng để khám phá.**

### Cảm giác khi chơi

> **Người chơi biết mình phải làm gì, nhưng không nhất thiết hiểu ngay mọi thứ mình nhìn thấy.**

### Từ phiên này sang phiên sau

> **Hành động → Thế giới ghi nhớ → Ký ức lệch nhau → Người chơi muốn biết tiếp → Phiên sau**

---

## Kim chỉ nam

> **Mỗi phiên cho người chơi một vấn đề rõ ràng để giải quyết.**  
> **Mỗi phiên để lại một câu hỏi chưa được giải thích hết.**  
> **Mỗi thay đổi của thế giới là một phần của câu chuyện lớn hơn.**

Và:

> **Thế giới ghi nhớ những gì người chơi đã làm — nhưng không nhất thiết theo cách người chơi nhớ.**

Cùng với:

> **Ký ức nằm phía sau cách chơi; người chơi không cần bị nhắc liên tục rằng đây là game về ký ức.**


## Thứ tự đọc

Đọc theo số, từ 04 đến 09. Menu site xếp chúng trong mục **Thứ tự đọc**.

- **[04 — Hướng làm việc](design/decisions/04-working-direction.md)**
- **[05 — Thế giới](design/decisions/05-world-premise-themes-core-fantasy.md)**
- **[06 — Nền câu chuyện](design/story/06-story-bible.md)**
- **[07 — Kịch bản](design/story/07-screenplay.md)**
- **[08 — Thích nghi cách chơi](design/gameplay/08-gameplay-adaptation.md)**  
  Các mục 08.01–08.10 nằm cùng thư mục.
- **[09 — Ánh xạ nội dung](design/gameplay/09-story-to-gameplay-content-mapping.md)**  
  Các mục 09.01–09.10 nằm cùng thư mục. Chưa có 09.03.
