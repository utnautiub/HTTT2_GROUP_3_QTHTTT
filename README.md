# XÂY DỰNG HỆ THỐNG BÁN HÀNG VỚI WORDPRESS, ERPNEXT, LUKLAK VÀ N8N

### Trường Đại Học Thủy Lợi  
**Khoa Công Nghệ Thông Tin**  
Giáo viên hướng dẫn: Thầy Đỗ Oanh Cường  
Nhóm 3 - 63HTTT2  

Sinh viên:  
- Bùi Tuấn Tú – 2151163736  
- Trần Văn Hải – 2151163686  
- Vũ Hà Lâm - 2151163701  

---

## Video DEMO

[Xem video demo](https://drive.google.com/file/d/1btpuxJCvBxePPoZeVR-G8-C1ezdt_VcZ/view?usp=sharing)

---

## Tài liệu

[Word](https://1drv.ms/w/c/bc371bdf3eae6ab0/EZWHBi3gRiBArCaEQqYqlfMBhFUh8BT8GhSIqILtB87Y3Q?e=oqdzyU)
[PowerPoint](https://1drv.ms/p/c/bc371bdf3eae6ab0/ERrRvagF7LJMkfvogehV-qIBuRFhxUwtEQUMtnuzbxhEtg?e=PSJ0jB)

---

## Mục Lục

1. [Giới thiệu đề tài](#giới-thiệu-đề-tài)
    - Bối cảnh đề tài
    - Vấn đề với các hộ kinh doanh
    - Tóm tắt đề tài
2. [Hướng giải quyết](#hướng-giải-quyết)
    - Xây dựng nền tảng bán hàng trực tuyến linh hoạt
    - Kết nối và đồng bộ hóa với hệ thống ERP
    - Quản lý quy trình với Luklak
    - Tự động hóa các quy trình với N8N
    - Tích hợp hệ thống thanh toán và vận chuyển
    - Đảm bảo tính bảo mật và an toàn dữ liệu
3. [Triển khai hệ thống](#triển-khai-hệ-thống)
    - Các công nghệ sử dụng
    - Quy trình và các chức năng
    - Triển khai
4. [Demo hệ thống](#demo-hệ-thống)
5. [Kết luận và hướng phát triển](#kết-luận-và-hướng-phát-triển)
6. [Tài liệu tham khảo](#tài-liệu-tham-khảo)

---

## Giới thiệu đề tài

### Bối cảnh đề tài
Trong thời đại công nghệ phát triển nhanh chóng, các doanh nghiệp bán lẻ đang phải đối mặt với nhu cầu chuyển đổi số mạnh mẽ, hướng tới các nền tảng thương mại điện tử. Đề tài này xây dựng một hệ thống quản lý bán hàng trực tuyến nhằm hỗ trợ Shop bán đồ cắm trại chuyển đổi từ quy trình thủ công sang hệ thống tự động, bao gồm quản lý sản phẩm, kho, đơn hàng và tích hợp các nền tảng.

### Vấn đề với các hộ kinh doanh
1. **Thiếu kết nối giữa các bộ phận**: Không đồng bộ dữ liệu giữa kho hàng, kế toán và bán hàng, dẫn đến sai sót trong quản lý và chậm trễ trong xử lý đơn hàng.
2. **Tốn thời gian cho các quy trình thủ công**: Các tác vụ như cập nhật tồn kho, gửi thông báo đơn hàng, hay tạo báo cáo thường phải thực hiện thủ công, gây lãng phí thời gian và tiềm ẩn rủi ro sai sót.
3. **Thiếu hệ thống báo cáo và phân tích hiệu quả**: Doanh nghiệp không có cái nhìn toàn diện về hiệu suất bán hàng, xu hướng mua sắm, và không thể tối ưu hóa chiến lược kinh doanh.
4. **Vấn đề về bảo mật và hiệu suất**: Sự gia tăng tần suất mua sắm trực tuyến khiến các trang web phải đối mặt với nguy cơ tấn công mạng, đồng thời đòi hỏi hiệu suất cao để đáp ứng nhu cầu khách hàng.

### Tóm tắt đề tài
Đề tài này hướng tới việc xây dựng một hệ thống quản lý bán hàng toàn diện và tích hợp cho shop đồ cắm trại, bao gồm các chức năng:
- Quản lý sản phẩm, kho, và đơn hàng.
- Báo cáo và phân tích dữ liệu.
- Tích hợp tự động hóa với N8N và hệ thống bảo mật Cloudflare.
  
Các nền tảng chính bao gồm WooCommerce, ERPNext, Luklak, và Cloudflare, đảm bảo tính bảo mật và khả năng mở rộng cho hệ thống.

---

## Hướng giải quyết

1. **Xây dựng nền tảng bán hàng trực tuyến linh hoạt**
   - Sử dụng WordPress và WooCommerce để xây dựng hệ thống bán hàng trực tuyến.
   - Quản lý sản phẩm, cập nhật thông tin, và tương tác với khách hàng.

2. **Kết nối và đồng bộ hóa với hệ thống ERP**
   - Tích hợp ERPNext để quản lý các kênh bán hàng, sản phẩm, nhân sự, và tài chính tự động.

3. **Quản lý quy trình với Luklak**
   - Tự động hóa việc tạo đơn hàng, khách hàng và kích hoạt các bước xử lý đơn hàng, giúp giảm thiểu sai sót và đẩy nhanh quy trình xử lý đơn hàng.
   - Luklak cũng hỗ trợ phân tích và báo cáo dữ liệu bán hàng.

4. **Tự động hóa các quy trình với N8N**
   - Sử dụng N8N làm công cụ tự động hóa, kết nối các hệ thống WooCommerce, ERPNext, và các dịch vụ vận chuyển.
   - Các quy trình tự động bao gồm tạo đơn hàng, đồng bộ dữ liệu sản phẩm, gửi email xác nhận, và tạo đơn vận chuyển.

5. **Tích hợp hệ thống thanh toán và vận chuyển**
   - Đa dạng hóa phương thức thanh toán (ngân hàng, mã QR, thanh toán khi nhận hàng).
   - Liên kết với các đơn vị vận chuyển để tự động theo dõi và cập nhật trạng thái đơn hàng cho khách hàng.

6. **Đảm bảo tính bảo mật và an toàn dữ liệu**
   - Sử dụng Cloudflare và Google reCAPTCHA để bảo vệ hệ thống trước các mối đe dọa bảo mật và tấn công mạng, đảm bảo trải nghiệm mua sắm an toàn cho khách hàng.

---

## Triển khai hệ thống

### Các công nghệ sử dụng
- **WordPress & WooCommerce**: Nền tảng chính cho trang thương mại điện tử, tích hợp dễ dàng các plugin và công cụ mở rộng.
- **ERPNext**: Quản lý kho hàng, tài chính, nhân sự và đồng bộ dữ liệu với WooCommerce.
- **Luklak**: Tự động tạo đơn hàng, quản lý khách hàng và phân tích dữ liệu bán hàng.
- **N8N**: Công cụ tự động hóa các luồng công việc, liên kết WooCommerce, ERPNext và hệ thống vận chuyển.
- **Cloudflare**: Dịch vụ CDN và bảo mật, giúp tăng cường hiệu suất và bảo mật trang web.

### Quy trình và các chức năng
1. **Tự động hóa quản lý sản phẩm và tiếp thị**:
   - Sản phẩm mới từ ERP sẽ tự động đăng lên WooCommerce.
   - Tương tác trực tiếp với khách hàng trên mạng xã hội.

2. **Quản lý và xử lý đơn hàng**:
   - Tự động tạo đơn hàng trong Luklak khi có đơn từ WooCommerce.
   - Kết nối và tự động cập nhật thông tin giao hàng từ GHTK (Giao Hàng Tiết Kiệm).

3. **Quản lý khách hàng và chăm sóc khách hàng**:
   - Luklak lưu trữ thông tin khách hàng, bao gồm dữ liệu mua sắm và tương tác trên mạng xã hội.
   - Hỗ trợ đội ngũ chăm sóc khách hàng trong việc phản hồi và xây dựng mối quan hệ.

4. **Quy trình thanh toán và bảo mật**:
   - Tích hợp thanh toán qua các kênh khác nhau và bảo mật bằng Cloudflare và Google reCAPTCHA.

5. **Báo cáo và phân tích hiệu suất kinh doanh**:
   - Hệ thống ERPNext cung cấp các báo cáo doanh thu, số lượng đơn hàng và theo dõi xu hướng mua sắm của khách hàng.

### Triển khai

#### 1. Cài đặt website bán hàng trực tuyến
   - Mua tên miền và hosting tại các dịch vụ như tenten.vn và 123host.vn.
   - Cài đặt WordPress và plugin WooCommerce để tạo trang bán hàng.

#### 2. Cài đặt và cấu hình ERPNext
   - Đăng ký ERPNext trên Frappe Cloud để sử dụng bản thử nghiệm.
   - Đồng bộ dữ liệu với WooCommerce thông qua N8N.

#### 3. Thiết lập N8N
   - Mua VPS tại 123host.vn để cài đặt N8N và tự động hóa quy trình.

#### 4. Thiết lập Luklak
   - Sử dụng Luklak để quản lý các hoạt động bán hàng, đồng bộ dữ liệu và tự động hóa đơn hàng.

#### 5. Bảo mật và tối ưu hóa hiệu suất hệ thống
   - Bảo vệ trang web với Cloudflare và cài đặt chứng chỉ SSL.
   - Cấu hình bảo mật cho WordPress bằng các plugin như Wordfence hoặc Sucuri.

---

## Demo hệ thống

### Website trực tuyến
- Link: [Hành Trình Ngoài Trời](https://trioproject.site)

![Demo Website](/img/webtructuyen.png)
![Demo Website](/img/demowebtructuyen.png)
![Giỏ hàng](/img/demowebtructuyen1.png)
![Thanh toán](/img/demowebtructuyen2.png)

### Hệ thống ERPNext
![Demo ERPNext](/img/erp-item.png)
![Demo ERPNext Detail Product](/img/erp-item1.png)
![Demo ERPNext Employee](/img/erp-employee.png)

### Hệ thống Luklak
![Demo Luklak](/img/luklak.png)
![Demo Luklak](/img/luklak1.png)
![Demo Luklak](/img/luklak2.png)
![Demo Luklak](/img/luklak3.png)

### Tự động hóa với N8N
![Demo N8N](/img/n8n.png)
![Demo N8N](/img/n8n-1.png)
![Demo N8N](/img/n8n-2.png)
![Demo N8N](/img/n8n-3.png)
![Demo N8N](/img/n8n-4.png)
![Demo N8N](/img/n8n-5.png)
![Demo N8N](/img/n8n-6.png)
![Demo N8N](/img/n8n-7.png)
![Demo GHTK](/img/ghtk.png)

---

## Kết luận và hướng phát triển

### Kết luận
- Đã xây dựng thành công website bán hàng với khả năng tự động hóa quy trình từ tạo đơn hàng đến vận chuyển.
- Giúp tối ưu hóa chi phí, quản lý hiệu quả và tăng cường trải nghiệm khách hàng.

### Hướng phát triển
- Tự động hóa các quy trình về nhân sự, kho bãi.
- Tích hợp AI trong việc đăng bài quảng cáo và tự động hóa tiếp thị sản phẩm.
- Mở rộng hệ thống lên các nền tảng thương mại điện tử khác.

---

## Tài liệu tham khảo

- Slide bài giảng môn Quản trị hệ thống thông tin.
- [n8n Docs](https://docs.n8n.io/)
- [API Giao Hàng Tiết Kiệm](https://giaohangtietkiem.vn)

