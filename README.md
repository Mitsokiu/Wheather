#Cấu trúc COOKIECUTTER    
weather_classification/
├── LICENSE
├── Makefile           <- Tệp Makefile với các lệnh như `make data` hoặc `make train`
├── README.md          <- Tài liệu README chính cho các nhà phát triển sử dụng dự án này.
├── data
│   ├── external       <- Dữ liệu từ các nguồn bên thứ ba.
│   ├── interim        <- Dữ liệu trung gian đã được chuyển đổi.
│   ├── processed      <- Các tập dữ liệu cuối cùng, chuẩn cho mô hình.
│   └── raw            <- Dữ liệu gốc, không thể thay đổi.
│
├── docs               <- Một dự án Sphinx mặc định; xem sphinx-doc.org để biết chi tiết.
│
├── models             <- Các mô hình đã huấn luyện và được lưu lại, dự đoán mô hình hoặc tóm tắt mô hình.
│
├── notebooks          <- Các notebook Jupyter. Quy ước đặt tên là số (để sắp xếp),
│                         chữ cái viết tắt của người tạo và một mô tả ngắn được phân cách bằng dấu `-`, ví dụ:
│                         `1.0-jqp-initial-data-exploration`.
│
├── references         <- Từ điển dữ liệu, tài liệu hướng dẫn và tất cả các tài liệu giải thích khác.
│
├── reports            <- Phân tích được tạo ra dưới dạng HTML, PDF, LaTeX, v.v.
│   └── figures        <- Các đồ họa và hình ảnh được tạo ra để sử dụng trong báo cáo.
│
├── requirements.txt   <- Tệp yêu cầu cho việc tái tạo môi trường phân tích, ví dụ:
│                         được tạo ra bằng `pip freeze > requirements.txt`.
│
├── setup.py           <- Làm cho dự án có thể cài đặt bằng pip (pip install -e .) để src có thể được nhập khẩu.
├── src                <- Mã nguồn để sử dụng trong dự án này.
│   ├── __init__.py    <- Biến src thành một mô-đun Python.
│   │
│   ├── data           <- Các script để tải xuống hoặc tạo dữ liệu.
│   │   └── make_dataset.py
│   │
│   ├── features       <- Các script để chuyển đổi dữ liệu thô thành các đặc trưng cho mô hình.
│   │   └── build_features.py
│   │
│   ├── models         <- Các script để huấn luyện mô hình và sau đó sử dụng các mô hình đã huấn luyện để thực hiện
│   │   │                 dự đoán.
│   │   ├── predict_model.py
│   │   └── train_model.py
│   │
│   └── visualization  <- Các script để tạo ra các hình ảnh khám phá và hình ảnh liên quan đến kết quả.
│       └── visualize.py
│
└── tox.ini            <- Tệp tox với các cài đặt để chạy tox; xem tox.readthedocs.io.
----------------------------------------------------------------------------------------------------------------------------
#Bài toán: Phân loại thời tiết dựa trên dữ liệu lịch sử

Nhóm chúng tôi quyết định xây dựng một mô hình phân loại thời tiết nhằm xác định trạng thái thời tiết (như "Sunny", "Rainy", "Cloudy") dựa trên các yếu tố môi trường như nhiệt độ, độ ẩm, tốc độ gió và áp suất khí quyển. Mô hình sẽ sử dụng dữ liệu lịch sử từ nhiều giờ và ngày khác nhau để dự đoán tình trạng thời tiết trong thời gian tới.

2. Động lực thực hiện bài toán
Ý nghĩa thực tiễn: Dự đoán thời tiết chính xác có thể hỗ trợ con người trong việc lên kế hoạch cho các hoạt động hàng ngày, như nông nghiệp, du lịch, và các sự kiện ngoài trời. Điều này có thể giảm thiểu thiệt hại do thời tiết xấu và nâng cao chất lượng cuộc sống.

Sự phát triển công nghệ: Với sự phát triển của trí tuệ nhân tạo và máy học, chúng tôi muốn áp dụng các kỹ thuật mới vào bài toán phân loại thời tiết để cải thiện độ chính xác và khả năng dự đoán.

Nghiên cứu khoa học: Việc phân tích và dự đoán thời tiết có thể đóng góp vào lĩnh vực nghiên cứu khí tượng học, giúp hiểu rõ hơn về các hiện tượng thời tiết và xu hướng biến đổi khí hậu.

3. Khó khăn nếu có
Chất lượng dữ liệu: Dữ liệu thời tiết có thể chứa nhiều giá trị thiếu, sai lệch hoặc không chính xác, điều này có thể ảnh hưởng đến kết quả của mô hình. Cần phải thực hiện các bước tiền xử lý dữ liệu cẩn thận.

Tính phức tạp của thời tiết: Thời tiết là một hiện tượng phức tạp và có thể bị ảnh hưởng bởi nhiều yếu tố khác nhau. Việc tìm ra mối quan hệ chính xác giữa các biến có thể là một thách thức.

Lựa chọn mô hình: Có nhiều mô hình máy học khác nhau có thể được áp dụng. Việc lựa chọn mô hình phù hợp nhất cho bài toán và tối ưu hóa siêu tham số có thể cần nhiều thời gian và công sức.

Đánh giá hiệu suất: Cần có các phương pháp đánh giá chính xác để đảm bảo mô hình hoạt động tốt trên tập kiểm tra và không bị overfitting.
---------------------------------------------------------------------------------------------------------------------------
#Nâng cao Kiến thức Về Machine Learning:

Thực hiện dự án này giúp chúng tôi hiểu rõ hơn về các thuật toán máy học, từ việc lựa chọn mô hình phù hợp cho đến tối ưu hóa và đánh giá hiệu suất. Chúng tôi sẽ có cơ hội thực hành và áp dụng lý thuyết đã học vào một bài toán thực tế.
Phát Triển Kỹ Năng Phân Tích Dữ Liệu:

Dự án này sẽ giúp chúng tôi phát triển kỹ năng phân tích dữ liệu, bao gồm việc làm sạch dữ liệu, khám phá và trực quan hóa dữ liệu, cũng như thực hiện các bước tiền xử lý cần thiết. Điều này rất quan trọng trong bất kỳ dự án khoa học dữ liệu nào.
Nâng cao Kỹ Năng Lập Trình:

Qua việc xây dựng mã nguồn cho dự án, chúng tôi sẽ cải thiện kỹ năng lập trình trong Python và làm quen với các thư viện như Pandas, NumPy, scikit-learn, Matplotlib, và Seaborn. Điều này sẽ giúp chúng tôi tự tin hơn trong việc xử lý và phân tích dữ liệu trong tương lai.
Hiểu Rõ Hơn Về Dữ Liệu Thời Tiết:

Dự án sẽ cho phép chúng tôi tìm hiểu sâu hơn về các yếu tố ảnh hưởng đến thời tiết, cách mà các biến môi trường tương tác với nhau, và làm thế nào để dự đoán thời tiết dựa trên dữ liệu lịch sử. Đây là một kiến thức quý giá cho những ai muốn làm việc trong lĩnh vực khí tượng hoặc môi trường.
Khám Phá Khoa Học Dữ Liệu:

Qua việc thực hiện dự án này, chúng tôi có thể hiểu rõ hơn về quy trình khoa học dữ liệu từ đầu đến cuối, từ việc thu thập dữ liệu, xử lý, xây dựng mô hình, đến việc triển khai và bảo trì mô hình. Điều này sẽ giúp chúng tôi trong các dự án khoa học dữ liệu trong tương lai.
Xây Dựng Kinh Nghiệm Thực Tế:

Dự án này không chỉ giúp chúng tôi học tập mà còn cung cấp kinh nghiệm thực tế quý báu trong việc làm việc nhóm, lập kế hoạch, giải quyết vấn đề, và quả


----------------------------------------------------------------------------------------------------------------------------
#DATASET 
Formatted Date: Thời gian được định dạng, bao gồm ngày, giờ và múi giờ (UTC +2). Thời gian được ghi lại theo từng giờ.

Summary: Tóm tắt tình trạng thời tiết trong khoảng thời gian đó (ví dụ: "Partly Cloudy", "Mostly Cloudy").

Precip Type: Loại mưa hoặc hiện tượng thời tiết (ví dụ: "rain").

Temperature (C): Nhiệt độ trong độ C tại thời điểm ghi nhận.

Apparent Temperature (C): Nhiệt độ cảm nhận được (cảm giác) trong độ C, có thể khác với nhiệt độ thực tế do ảnh hưởng của độ ẩm và gió.

Humidity: Độ ẩm không khí, được biểu thị dưới dạng thập phân (từ 0 đến 1).

Wind Speed (km/h): Tốc độ gió tính bằng km/h.

Wind Bearing (degrees): Hướng gió tính bằng độ, thường được đo theo chiều kim đồng hồ từ phía Bắc (0°).

Visibility (km): Khoảng cách nhìn thấy được, tính bằng km.

Loud Cover: Độ che phủ của mây (có thể không có thông tin chi tiết trong dữ liệu này, thường là một thang đo từ 0 đến 1).

Pressure (millibars): Áp suất khí quyển tính bằng millibar.

Daily Summary: Tóm tắt tình trạng thời tiết trong suốt cả ngày.
----------------------------------------------------------------------------------------------------------------------------
#TIẾN HÀNH
. Chuẩn bị Dữ liệu
Xử lý Dữ liệu: Kiểm tra dữ liệu để loại bỏ giá trị thiếu, biến đổi kiểu dữ liệu  chuyển đổi thời gian thành định dạng datetime và mã hóa các biến phân loại như Summary và Precip Type.
2. Khám Phá Dữ liệu
Khám Phá Dữ liệu (EDA): Phân tích dữ liệu để tìm hiểu mối quan hệ giữa các biến, như mối quan hệ giữa nhiệt độ, độ ẩm và tình trạng thời tiết.
Trực Quan Hóa: Sử dụng thư viện như Matplotlib hoặc Seaborn để tạo biểu đồ trực quan giúp bạn hiểu dữ liệu tốt hơn.
3. Tiền Xử lý Dữ liệu
Chia Dữ liệu: Chia dữ liệu thành tập huấn luyện và tập kiểm tra (ví dụ: 80% dữ liệu huấn luyện và 20% dữ liệu kiểm tra).
Chuẩn Hóa: Đối với các biến số lượng (như nhiệt độ, độ ẩm), hãy chuẩn hóa dữ liệu để đảm bảo rằng tất cả các biến đều có cùng một thang đo.
4. Xây Dựng Mô Hình
Chọn Mô Hình: Có nhiều mô hình mà bạn có thể sử dụng để phân loại như:
Decision Trees
Random Forest
Support Vector Machines (SVM)
Neural Networks
Huấn Luyện Mô Hình: Sử dụng tập huấn luyện để huấn luyện mô hình của bạn và điều chỉnh các siêu tham số nếu cần.
5. Đánh Giá Mô Hình
Dự Đoán: Sử dụng tập kiểm tra để dự đoán và so sánh với nhãn thực tế.
Đánh Giá Hiệu Suất: Sử dụng các chỉ số như độ chính xác, độ chính xác (precision), độ nhạy (recall) và F1-score để đánh giá mô hình.
6. Triển Khai Mô Hình
Triển Khai: Nếu mô hình đạt hiệu suất tốt, bạn có thể triển khai nó vào ứng dụng thực tế hoặc tạo một API để dự đoán thời tiết.
