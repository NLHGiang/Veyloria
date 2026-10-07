# Decision Log — Veyloria

> Quyết định **có phương án bị loại** (lưu "tại sao"). **Một file cho cả dự án** — không chia phase (ADR-035 QĐ-7). ID vẫn `DEC-{PHASE}-NNN` trong từng entry.
> Schema đầy đủ: minipower pack `docs/decision-log.md`.

<!-- Thêm entry mới phía trên (mới nhất trước). -->

### DEC-DIS-001 — Minipower gắn vào repo DNA · [2026-10-07]
- Status: accepted
- Context: Workspace cha chứa ba checkout. Cần một dự án Minipower, không phải hai hồ sơ song song.
- Options: A init ở thư mục cha / B init và cài skill trong repo dna / C cài vào cả hai như hai dự án
- Decision: B — repo dna là dự án Minipower. `../prototype` là bản chơi để đối chiếu. `../minipower` là factory skill.
- Why (loại A vì hồ sơ quản trị sẽ tách khỏi knowledge base; loại C vì hai `memory/profile.json` tranh nhau làm nguồn cấu hình).
- Consequences: khung DOC và `.minipower` nằm trong dna. Thư mục cha không giữ hồ sơ dự án thứ hai.
- Affects: repo dna · prototype chỉ để đọc
- Trace: docs/index.md
- Confidence: cao
