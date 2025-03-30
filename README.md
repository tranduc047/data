📝 Bài tập 4: Phân tích dữ liệu thời tiết
📥 Dữ liệu: Hourly Weather Data

Yêu cầu bài tập
Đọc dữ liệu và kiểm tra thông tin cột thời gian.
Lọc dữ liệu: Chỉ giữ lại dữ liệu từ năm 2020 trở đi.
Trích xuất thông tin thời gian: Thêm cột year, month, day_of_week, hour.
Lấy mẫu lại dữ liệu: Chuyển từ dữ liệu theo giờ thành trung bình nhiệt độ theo ngày.
Nội suy dữ liệu bị thiếu để điền nhiệt độ bị khuyết.
Tính toán xu hướng thời gian: Tính nhiệt độ trung bình theo tháng và vẽ biểu đồ.
Ví dụ kết quả mong đợi
Sau khi resample, dữ liệu có dạng: | Date | Avg_Temp | |------------|---------| | 2020-01-01 | 5.2 | | 2020-01-02 | 4.8 | | 2020-01-03 | 3.1 |

Gợi ý cách làm
Dùng .to_datetime(df["datetime"]) để chuyển đổi cột thời gian.
Lọc dữ liệu bằng điều kiện df["datetime"].dt.year >= 2020.
Sử dụng .resample("D", on="datetime").mean() để lấy nhiệt độ trung bình theo ngày.
Dùng .interpolate() để nội suy nhiệt độ bị thiếu.
Vẽ biểu đồ xu hướng nhiệt độ theo tháng bằng Matplotlib.
