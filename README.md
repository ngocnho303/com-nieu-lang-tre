# com-nieu-lang-tre
Phân tích và đề xuất giải pháp phát triển Hệ thống Thông tin Quản lý Chuỗi nhà hàng Cơm Niêu Làng Tre


##  1. TỔNG QUAN VỀ DOANH NGHIỆP VÀ HỆ THỐNG THÔNG TIN

### 1.1. Lịch sử hình thành & Quá trình phát triển
* **Tổng quan**: Cơm Niêu Làng Tre là chuỗi nhà hàng hoạt động trong lĩnh vực ẩm thực truyền thống Việt Nam, nổi bật với các món ăn đậm chất gia đình (cơm niêu, cá kho tộ, thịt kho, canh chua...).
* **2018**: Khởi đầu với 01 cơ sở tại Quận Gò Vấp, TP.HCM, tập trung phục vụ đối tượng khách văn phòng và gia đình.
* **2019 – 2021**: Mở rộng thêm các chi nhánh tại Gò Vấp và Bình Thạnh; bắt đầu chuyển đổi từ mô hình đơn lẻ sang chuỗi quy mô nhỏ.
* **2022 – Nay**: Phát triển lên quy mô 4 chi nhánh. Bắt đầu ứng dụng công nghệ ở mức cơ bản (phần mềm POS Ocha) để hỗ trợ ghi nhận đơn hàng, in hóa đơn và kiểm soát kho sơ khai.

### 1.2. Sứ mệnh – Tầm nhìn – Giá trị cốt lõi
* **Sứ mệnh**: Mang đến bữa ăn đậm nét truyền thống Việt Nam trong không gian ấm cúng, gần gũi như gia đình; đảm bảo an toàn thực phẩm và dịch vụ tận tâm.
* **Tầm nhìn**: Trở thành chuỗi cơm niêu quen thuộc tại TP.HCM và mở rộng ra các khu vực lân cận, từng bước hiện đại hóa quản trị F&B.
* **Giá trị cốt lõi**: Chất lượng – Khách hàng là trung tâm – Hiệu quả vận hành – Trách nhiệm – Tinh thần cải tiến.

### 1.3. Cơ cấu tổ chức
Sơ đồ vận hành linh hoạt theo mô hình phẳng dành cho chuỗi F&B vừa và nhỏ:
* **Chủ doanh nghiệp**: Định hướng chiến lược, kiểm soát tài chính tổng thể.
* **Quản lý chi nhánh**: Điều phối vận hành, phân ca nhân sự, kiểm soát chất lượng dịch vụ tại từng điểm bán.
* **Bộ phận vận hành trực tiếp**: Thu ngân, Bộ phận kho, Nhân viên phục vụ, Nhân viên order, Bộ phận bếp, Nhân viên đóng gói.

---

##  2. TỔNG QUAN HỆ THỐNG THÔNG TIN QUẢN LÝ (MIS) HIỆN TẠI

### 2.1. Khái niệm MIS trong lĩnh vực F&B
Hệ thống Thông tin Quản lý (MIS) là sự kết hợp giữa **Con người – Quy trình – Công nghệ – Dữ liệu** nhằm thu thập, xử lý và cung cấp thông tin kịp thời hỗ trợ ra quyết định kinh doanh.

### 2.2. Các thành phần hệ thống hiện tại
* **Hệ thống POS bán hàng**: Phần mềm Ocha đảm nhận nhận đơn online, quản lý bàn, tạo hóa đơn, theo dõi kho cơ bản và báo cáo doanh thu theo ca.
* **Ứng dụng quản lý từ xa**: Ocha Boss cung cấp báo cáo doanh thu tổng quan cho chủ doanh nghiệp trên thiết bị di động.
* **Kênh trực tuyến**: Website giới thiệu thương hiệu ở dạng tĩnh, chưa hỗ trợ tính năng đặt bàn hay gọi món trực tuyến.

### 2.3. Đánh giá sơ bộ & Sự cần thiết nâng cấp
* **Điểm nghẽn vận hành**: Phụ thuộc 100% vào nhân viên ghi đơn 1:1, gây quá tải nghiêm trọng vào các khung giờ cao điểm.
* **Quản lý tài chính & Kho**: Thiếu định mức nguyên vật liệu (BOM) chuẩn gây sai lệch tồn kho; chưa có phân hệ quản lý công nợ khách đoàn/doanh nghiệp và nhà cung cấp.
* **Dữ liệu phân tán**: Dữ liệu bán hàng, kho, nhân sự bị rời rạc; báo cáo mang tính thô, chưa hỗ trợ phân tích chuyên sâu.
* **Nhu cầu tất yếu**: Nâng cấp MIS là bắt buộc để chuẩn hóa vận hành toàn chuỗi, cắt giảm thất thoát và nâng cao trải nghiệm khách hàng.

---

## 3. THỰC TRẠNG PHÁT TRIỂN HỆ THỐNG THÔNG TIN QUẢN LÝ

| Phân hệ / Kênh | Thực trạng hiện tại | Hạn chế chính |
| :--- | :--- | :--- |
| **Quản lý Nhân sự** | Lập lịch ca, chấm công thủ công hoặc rời rạc. | Thiếu liên kết với dữ liệu bán hàng; khó đánh giá chính xác KPI/năng suất theo ca. |
| **Bán hàng & Vận hành** | Dùng POS Ocha nhập đơn, in bill. | Nghẽn giờ cao điểm, phụ thuộc thiết bị chuyên dụng, chưa tự động hóa gọi món qua QR. |
| **CSKH & Kênh Online** | Website thông tin tĩnh. | Thiếu tính năng đặt bàn/món online, thiếu CRM tích hợp và Chatbot CSKH 24/7. |
| **Hỗ trợ ra Quyết định** | Báo cáo cơ bản trên ứng dụng di động. | Quyết định mở rộng/tối ưu thực đơn chủ yếu dựa vào cảm tính và kinh nghiệm. |

---

##  4. CƠ SỞ PHƯƠNG PHÁP LUẬN & CÁC PHƯƠNG ÁN GIẢI PHÁP

### 4.1. Phương pháp luận phát triển
* **Hướng quy trình (Process-oriented)**: Chuẩn hóa luồng nghiệp vụ *Khách chọn món → QR/POS → Bếp → Phục vụ → Thanh toán* nhằm tối ưu tốc độ và giảm sai sót.
* **Hướng dữ liệu (Data-oriented)**: Xây dựng Cơ sở dữ liệu tập trung (ERD) kết nối Bán hàng – Kho – Nhân sự – CRM – Tài chính.
* **Phương pháp luận hỗn hợp (Hybrid Methodology)**: Kết hợp cả 2 hướng để đảm bảo vừa tối ưu hóa luồng vận hành thực tế, vừa đảm bảo tính toàn vẹn dữ liệu.

---


### 4.2. So sánh các phương án giải pháp

| Phương án | Chi phí | Ưu điểm | Nhược điểm |
| :--- | :--- | :--- | :--- |
| **Phương án 1: Nâng cấp trên Ocha**<br>*(Mua lẻ các module hỗ trợ)* | ~115.000.000 VNĐ | Rủi ro thấp, dễ tiếp cận | Rời rạc, dữ liệu bị phân tán |
| **Phương án 2: Triển khai KiotViet**<br>*(Giải pháp Tích hợp Tối ưu - **CHỌN**)* | ~190.000.000 - 195.000.000 VNĐ | Tập trung dữ liệu, chuẩn BOM kho | Cần thời gian đào tạo |
| **Phương án 3: Xây dựng hệ thống ERP**<br>*(Tùy chỉnh riêng biệt)* | ~410.000.000 VNĐ | Tùy biến tuyệt đối | Chi phí quá cao, rủi ro lớn |

> **LỰA CHỌN TỐI ƯU**: **Phương án 2 (Triển khai KiotViet)** là nền tảng cân bằng nhất giữa chi phí, tiến độ triển khai và khả năng quản trị cho chuỗi F&B quy mô vừa.
---

## 5. KẾ HOẠCH HÀNH ĐỘNG VÀ TRIỂN KHAI HỆ THỐNG KIOTVIET

* **Giai đoạn 1: Chuẩn bị & Ký kết (Tháng 1)**
  * Khảo sát quy trình, chốt hợp đồng bản quyền KiotViet.

* **Giai đoạn 2: Cấu hình Phân hệ (Tháng 2)**
  * **POS Sales**: Quản lý order bàn, phòng, khách đoàn.
  * **DMS Kho**: Thiết lập công thức BOM (Recipe), định mức kho.
  * **CRM**: Lưu trữ dữ liệu khách hàng, phân hạng thành viên.
  * **HRMS**: Phân ca làm việc, chấm công FaceID.

* **Giai đoạn 3: Triển khai Thí điểm & Toàn chuỗi (Tháng 3 - Tháng 5)**
  * Chạy Pilot tại 01 chi nhánh $\rightarrow$ Đánh giá & Tối ưu.
  * Nhân rộng ra toàn bộ 4 chi nhánh.

* **Giai đoạn 4: Đào tạo & Chuẩn hóa TO-BE (Tháng 6)**
  * Ban hành SOP vận hành mới, đào tạo nhân viên.


---

## 6. DỰ TRÙ KINH PHÍ VÀ ĐÁNH GIÁ HIỆU QUẢ (KPIs)

### 6.1. Dự trù kinh phí triển khai KiotViet (Đơn vị: VNĐ)
* **Bản quyền phần mềm KiotViet**: 60.000.000 – 120.000.000
* **Thiết bị phần cứng (Máy POS, Máy in, QR, Máy chấm công FaceID)**: ~80.000.000
* **Chi phí đào tạo & Triển khai**: ~30.000.000
* **Chi phí dự phòng rủi ro (10%)**: ~20.000.000
* **TỔNG CHI PHÍ ƯỚC TÍNH**: **~190.000.000 – 250.000.000 VNĐ**

### 6.2. KPIs đánh giá hiệu quả hệ thống mới

| Chỉ số đo lường (KPI) | Trước khi đổi mới | Sau khi đổi mới  |
| :--- | :--- | :--- |
| **Thời gian trung bình Order** | 5 – 7 phút / bàn | **2 – 3 phút / bàn** |
| **Tỷ lệ sai sót đơn hàng** | 5% – 10% | **< 2%** |
| **Quản lý Tồn kho** | Kiểm kê thủ công | **Tự động trừ kho Realtime theo BOM** |
| **Thời gian lập báo cáo** | Cuối ngày / Thủ công | **Báo cáo Realtime tức thì** |
| **Hiệu suất phục vụ chung** | Mức trung bình | **Tăng 20% – 30%** |

---

## 7. KẾT LUẬN
Việc chuyển đổi sang nền tảng quản trị **KiotViet** kết hợp với phương pháp luận hỗn hợp (Hướng quy trình & Hướng dữ liệu) giúp Cơm Niêu Làng Tre giải quyết triệt để các hạn chế hiện tại. Hệ thống mới không chỉ giúp tối ưu chi phí vận hành, giảm bớt thao tác thủ công mà còn đặt nền móng dữ liệu vững chắc cho chiến lược mở rộng chuỗi nhà hàng bền vững trong tương lai.
