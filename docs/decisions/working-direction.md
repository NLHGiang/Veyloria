# Working Direction — Step 4

> **Trạng thái:** Đã chốt trong quá trình xây dựng Pre-V1  
> **Nguyên tắc:** Tích hợp trực tiếp vào source hiện tại; không tạo tài liệu/nhánh riêng mang tên “DNA V2”.

## 1. Vai trò của hai source

Veyloria hiện được phát triển từ hai nguồn có vai trò khác nhau:

- **Veyloria repository** — source of truth cho DNA, concept, world, design principles và các quyết định đã được chốt.
- **voryki-v1.0 repository** — prototype/demo dùng để kiểm chứng cách triển khai hình ảnh, interaction và gameplay; prototype có thể chưa khớp DNA.

Tên prototype không quyết định tên game. Tên thống nhất của game là **Veyloria**.

## 2. Trạng thái Veyloria

Veyloria vẫn ở trạng thái **Pre-V1 / Working Source**.

Không coi bất kỳ tài liệu hiện tại nào là “Veyloria V1 chính thức”. Các quyết định mới được tích hợp vào bộ source hiện tại khi được chốt.

## 3. Quyết định về “DNA V2”

**Không tạo DNA V2.**

Lý do: source hiện tại chưa được xem là V1 hoàn chỉnh; việc tách sang một “V2” sẽ tạo thêm tầng phiên bản không cần thiết và làm phân tán source of truth.

Thay vào đó:

> **Mỗi quyết định đã chốt được cập nhật trực tiếp vào các tài liệu hiện tại và index của knowledge base.**

## 4. Hướng phát triển

Thứ tự làm việc được giữ như sau:

1. Đọc và xác định DNA hiện tại.
2. Đọc toàn bộ prototype/demo.
3. So sánh DNA với prototype.
4. Chốt các quyết định nền tảng và tích hợp trực tiếp vào source hiện tại.
5. Khóa World + Premise + Themes + Core Fantasy.
6. Xây Story Bible.
7. Viết long-form script.
8. Chuyển hóa sang gameplay.
9. Map Story → Quest → Mechanic → Level → Progression.
10. Sau đó mới quay lại prototype để triển khai code theo DNA đã ổn định.

## 5. Nguyên tắc bảo vệ DNA

Prototype không được tự động trở thành design authority.

Khi prototype và DNA khác nhau:

> **DNA quyết định hướng thiết kế; prototype là nơi kiểm chứng và triển khai.**

Các chi tiết prototype chỉ được đưa ngược vào DNA khi chúng được xem xét và chốt như một quyết định thiết kế.

---

Đây là **working direction**, không phải “DNA V2”.
