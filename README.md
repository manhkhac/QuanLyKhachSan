CHƯƠNG 1: TỔNG QUAN VỀ PHẦN MỀM
1.1.	Tên đề tài
-	Phần mềm quản lý khách sạn “SÀI GÒN ODYSSEY HOTEL”.
1.2.	Lý dó chọn đề tài
-	Tại Việt Nam nhà nước đang tạo điều kiện thuận lợi cho việc phát triển ngành dịch vụ, kéo theo đó là ngành du lịch. Vì thế ngành kinh doanh khách sạn cũng đang được chú trọng để thu hút lượng khách du lịch tới Việt Nam, để phát huy thuận lời về vị trí địa lý cũng như là các danh lam thám cảnh tại đất nước chúng ta.
-	Tuy nhiên trong thực tế thì, các khách sạn lớn mới có các phần mềm quản lý. Còn các khách sạn vừa và nhỏ thì hầu như công việc đều đang phải làm một cách thủ công, trong khi đó ở nước ta, các khách sạn lớn lại chưa thật sự nhiều, vì vậy cơ sở vật chất và nền kinh tế cũng đang còn phát triển.
-	Xuất phát từ thực tế đó , nhóm chúng em đã chọn đề tài “Phần Mềm Quản Lý Khách Sạn Sài Gòn ODYSSEY HOTEL”. Đây là một đề tài không còn mới song nó vẫn chưa hêt phổ biến trong quá trình quản lý khách sạn. Vì vậy, nhóm em nhiên cứu đề tài này hy vọng sẽ góp phần giúp công việc quản lý trở nên đơn giản hơn.












CHƯƠNG 2: Phân tích thiết kế database
2.1.	Tổng quan về database của phần mềm
 
Database gồm các bảng sau:
-	 Bảng hóa đơn gồm:
 
 Khóa chính là: HoaDonID
Khóa phụ là:KhachHangID, NhanVienID, PhongID, 


-	Bảng lịch làm việc:
 
 Khóa chính là: LichLamViecID
Khóa phụ là : NhanVienID

-	Bảng khách hàng
 
Khóa chính: KhachHangID

-	Bảng chi tiết hóa đơn
 
Khóa chính: ChiTietHoaDonID
Khóa phụ: DichVuID, HoaDonID

-	Bảng dịch vụ
 
Khóa chính: DichVuID

-	Bảng nhân viên:
 
Khóa chính là: NhanVienID

-	Bảng mật khẩu:
	 
Khóa chính là: username

-	Bảng phòng:
 
Khóa chính là : PhongID
Khóa phụ: LoaiPhongID

-	Bảng loại phòng
 
Khóa chính là: LoaiPhongID

-	Bảng vật tư
 
Khóa chính là: VatTuID

















2.2.	Mô hình Class Diagram:
 
2.2.1.	Mô hình UseCase 



















2.2.2.	Màn hình đăng nhập
 
-	Mô tả: Dùng để đăng nhập tài khoản trước khi vào màn hình chính. 

2.2.3.	Màn hình quản lý phòng:


 
-	Mô tả: Hiển thị toàn bộ số phòng đang có trong khách sạn, bao gồm số phòng, loại phòng và giá phòng trên đó, người dùng không được thay đổi thông tin gì trên màn hình này. Góc trái màn hình có 3 nút là 3 chức năng: Cập nhật vật tư, cập nhật dịch vụ, cập nhật loại phòng.












2.2.4.	Màn hình cập nhật vật tư:

 
-	Mô tả:
 + hiển thị toàn bộ vật tư đang có trong khách sạn như: tivi, tủ lạnh, máy lạnh, bài ủi.....
+ có các nút chức năng như: thêm vật tư, xóa vật tư, cập nhật lại vật tư dựa theo thao tác chọn dòng từ datagridview của người dùng. Mỗi thao tác sẽ được cập nhật lại xuống database. 

2.2.5.	Màn hình cập nhật dịch vụ khách sạn:

	 

   - Mô tả: 
+ Hiển thị toàn bộ dịch vụ đang có trong khách sạn như: nước suối, massage, đi tour, đưa đón taxi đi sân bay, giặt ủi....
+ Có các nút chức năng như: thêm dịch vụ, xóa dịch vụ, cập nhật lại dịch vụ dựa theo thao tác chọn dòng từ datagridview của người dùng. Mỗi thao tác sẽ được cập nhật lại xuống database.










2.2.6.	Màn hình cập nhập loại phòng:
 
-	Mô tả:
+ Người dùng lựa chọn số phòng và cập nhật lại loại phòng theo 3 loại đã được set trong combobox: standard, deluxe, superior.
+ Nút lưu sẽ cập nhật lại loại phòng dựa theo số phòng người dùng đã chọn và lưu và database.
      +  Nút hủy để hủy các lựa chọn từ combobox của khách hàng.







2.2.7.	Màn hình quản lý nhân viên:
 
-	Mô tả:
+ Hiển thị toàn bộ lịch làm việc của nhân viên đang có trong khách sạn, bao gồm số thứ tự, tên nhân viên, ca trực, ngày làm  trên đó,người dùng không được thay đổi thông tin gì trên màn hình này. Góc trái màn hình có 2 nút là 2 chức năng: Cập nhật thông tin nhân viên, cập nhật lịch làm việc và hiển thị lịch để tiện cho việc quan sát ngày tháng.


2.2.8.	Màn hình cập nhật thông tin nhân viên:
 
- Mô tả:
+ Hiển thị thông tin toàn bộ nhân viên làm việc trong khách sạn bao gồm: số thứ tự và tên nhân viên.
+ Các nút với các chức năng như thêm nhân viên, xóa nhân viên, cập nhật lại thông tin nhân viên, tìm kiếm theo tên nhân viên, hủy tìm kiếm.
+ Người dùng chọn dòng trên datagridview và click vào các nút để thao tác, mỗi dòng người dùng click trên picturebox hiển thị hình theo từng nhân viên, nếu nhân viên không có hình hệ thống sẽ lấy hình mặc định.
2.2.9.	Màn hình cập nhật lịch làm việc:

 

-	Mô tả:
+ Hiển thị toàn bộ lịch làm việc của nhân viên trên datagirdview đông thời có thêm các chức năng: thêm lịch làm việc, xóa lịch làm việc, cập nhật lại lịch làm việc.
+ Người dùng sẽ chọn từ 3 combobox bên tay phải màn hình để thêm lịch làm việc cho nhân viên
+ Nhân viên chưa được thêm vào co sở dữ liệu sẽ không được thêm lịch làm việc.
+ Nút xem lại lịch làm việc được hiển thị trên góc trái trên của màn hình để người dùng có thể xem lại ngày làm việc của nhân viên theo lựa chọn trên datetime picker. 
2.2.10.	Màn hình quản lý khách hàng:

 
-	Mô tả:
+ Hiển thị toàn bộ khách hàng đã check in tại khách sạn khi đã có hóa đơn thanh toán.
+ Bao gồm các nút chức năng như: tìm kiếm khách hàng theo tên khách hàng, lọc ra các khách hàng từ ngày nào đến ngày nào.
+ Người dùng không có quyền xóa hay thêm hay cập nhật gì từ màn hình này, người dùng muốn thêm khách hàng thì chỉ được thêm khi đã có hóa đơn từ màn hình chi tiết hóa đơn.
2.2.11.	Màn hình liên hệ:
 
-	Mô tả:
+ Hiển thị thông tin của nhà sáng lập ra phần mềm, địa chỉ, email. website liên hệ, số điện thoại, năm phát hành.

2.2.12.	Màn hình chi tiết phiếu phòng:
 
-	Mô tả:
+ Hiển thị các thông tin về hóa đơn của khách hàng như: loại phòng, tên booking, số khách, ngày vào,
giá phòng, số đêm, số phòng, tên khách, quốc tịch, ngày đi, thành tiền, tên dịch vụ, giá dịch vụ
số lượng,tên nhân viên, ngày của hóa đơn.
+ Bao gồm các nút với các chức năng như: thêm dịch vụ, xóa dịch vụ, lưu khi có sửa đổi, in, và xem lại hóa đơn theo ngày đến trên datetime picker.
+ Sau khi người dùng nhấn nút lưu thông tin sẽ được lưu vào bảng khách hàng, hóa đơn, chi tiết hóa đơn theo từng table trong cơ sở dữ liệu, đồng thời sẽ chuyển về màn hình chính và hiển thị lên các label của phòng đó thông tin đã được điền vào và trạng thái phòng sẽ thay đổi từ trống sang có khách.
+ Khi người dùng nhấn nút thêm, tên dịch vụ được chọn từ combobox và số lượng được điền từ textbox sẽ được insert xuống datagridview chi tiết dịch vụ bên dưới.
+ Khi người dùng nhấn chọn dòng trên datagridview và nhấn nút xóa, thì dòng dl đó sẽ được xóa đi trên datagridview đó.
+ Tên dịch vụ sẽ được load từ database đổ và combobox.


2.2.13.	Màn hình chính:

 
-	Mô tả: Hiển thị tổng quát toàn bộ các chứng năng của phần mềm bao gồm:
+ Hiển thị 8 phòng hiện có của khách sạn: mỗi phòng hiển các thông tin như tên booking, tên khách, số khách, quốc tịch, ngày đến, ngày đi, tiền phòng, và tính năng thay đổi trạng thái phòng, 1 button chuyển đến trang chi tiết để điền thông tin hóa đơn, 1 nút check out khi khách trả phòng.
+ Bên tay trái màn hình hiển thị lịch tiện cho người sử dụng quan sát ngày tháng năm.
+ Dưới góc trái hiển thị các màu theo trạng thái phòng như: màu đỏ - phòng đang trống, màu xanh - phòng đang có khách, màu vàng - phòng khách sẽ trả, màu xám - phòng đang dọn dẹp.
+ Góc trên của màn hình là thanh menustrip bao gồm các chức năng tương đương link tới các màn hình của chức năng đó: quản lý phòng, quản lý nhân viên, quản lý khách hàng, thống kê và liên hệ.
