# Predicting-Algae-Blooms
1. Giới thiệu

  Sự xuất hiện dày đặt của tảo ( mật độ tảo tăng nhanh chóng- gọi là "nở hoa"), ảnh tưởng đến môi trường sống của sinh vật dưới nước và chất lượng nguồn nước. Việc theo dõi và thực hiện dự báo sớm về sự nở hoa của tảo là cần thiết để nâng cao chất lượng các dòng sông. Với mục tiêu giải quyết vấn đề dự đoán này, một số mẫu nước được thu thập ở các con sông khác nhau ở Châu Âu vào những thời điểm khác nhau trong một năm. Ngoài ra, kết quả của nghiên cứu này được mong đợi là có thể cung cấp sự hiểu biết tốt hơn về các yếu tố ảnh hưởng đến tần số tảo. Cụ thể, muốn hiểu cách các tần số này liên quan đến các thuộc tính hóa học nhất định của mẫu nước như cũng như các đặc điểm khác của mẫu (như mùa trong năm, loại sông,...).
  
  Thực nghiệm này chỉ phục vụ cho việc hoc tập và nghiên cứu.

2. Phương pháp

Phương pháp: Multiple linear regression, Regression tree và RandomForest

Cách đánh giá:  k-fold cross-validation

Độ đo: NMSE- normalized mean squared error

3. Dữ liệu

  Tập data có trong thư viện R, gồm 3 phần nhỏ:
  
  * Analysis.txt: chứa dữ liệu liên quan đến 200 mẫu nước được thu thập tại các dòng sông khác nhau ở Châu Âu(mỗi quan sát trong bộ dữ liệu có sẵn thực tế là tổng hợp của một số mẫu nước được thu thập từ cùng một con sông trong khoảng thời gian 3 tháng, trong cùng một mùa trong năm), mỗi mẫu nước được mô tả bởi 11 biến:
			
      + 3 cột đầu tiên là biến định danh (nominal): mô tả 4 mùa trong năm, kích thước của sông và tốc độ nước của sông.
      
			+ 8 biến còn lại là giá trị của các thông số hóa học khác nhau được đo trong mẫu nước: Giá trị pH tối đa, Giá trị tối thiểu của O2 (oxy), Giá trị trung bình của Cl(clorua), Giá trị trung bình của NO−3 (nitrat), Giá trị trung bình của amoni, Trung bình của orthophosphat, rung bình của tổng PO4 (phốt phát), Ý nghĩa của chất diệp lục.
      
			+ 7 cột tiếp theo là tần số suất xuất hiện 7 loại tảo có hại.
      
  * Eval.txt (được coi như là test set): Có cấu trúc như tập “Analysis.txt” nhưng bỏ qua 7 cột tần suất của tảo(140 mẫu nước). Mục tiêu chính của nghiên cứu là dự đoán tần số xuất hiện của 7 loại tảo có hại trong 140 mẫu nước này.
    
	* Sols.txt: chứa tần suất tảo của 140 mẫu nước của "Eval.txt", tệp này dùng để kiểm định kết quả tần suất sau khi dự đoán được (sau khi dự đoán xong mới được sử dụng).

4. Tham khảo

[1]Luis Torgo, "Data Mining with R Learning with Case Studies, Second Edition by Torgo, Luís (z-lib.org)"
