- ensemble learning: là phương pháp tổng hợp các model con hợp thành một mô hình học máy lớn và hoàn chỉnh hơn
- fitting: 1 thuật ngữ ám chỉ về sự "hợp lý" khi chọn thuật toán model cho việc trainning, nói đơn giản là:
	+ nếu một thuật toán quá đơn giản so với một xu hướng dữ liệu méo mó (phương trình bậc nhất với xu hướng mật độ dữ liệu uốn éo) thì xu hướng dự đoán quá lệch so với đầu ra mong đợi (underfitting)
	+ nếu một thuật toán quá phức tạp, quá "chi tiết" so với một xu hướng dữ liệu đơn điệu (phương trình bậc n so với xu hướng dữ liệu là 1 đường thẳng tắp), nó sẽ trở nên vô cùng tỉ mẩn và khó nhìn ra được vấn đề toàn cảnh của tập dữ liệu ấy, từ đó không dự đoán chuẩn xu hướng dữ liệu được (overfitting)
	+ 1 thuật toán vừa đủ thì sẽ được gọi là fitting
- cross validacation: 1 phương pháp chia dataset mạnh và tối ưu với các loại hình ML, phương pháp này ưu tiên việc đẩy mọi thứ ngẫu nhiên để kiểm tra ML mỗi 1 round train thay vì từ đầu đến cuối chỉ cố định các tập đã chia từ đầu
