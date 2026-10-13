# Báo cáo Bài 3: Gradle Dependency Caching

* Họ tên: Đoàn Trung Nguyên
* Mã sinh viên: B24DTCN435
* Lớp: HN-K24-CNTT4

## 1\. Cấu hình

Bổ sung cache: 'gradle' vào bước actions/setup-java@v5
trong .github/workflows/ci.yml, sử dụng Java 17 Temurin.

## 2\. Kết quả thực nghiệm

|Nội dung|Lần chạy #2|Lần chạy #3|
|-|-|-|
|Trạng thái|Thành công|Thành công|
|Thời gian workflow hiển thị trên Actions|59 giây|42 giây|
|Commit|1bc8b73|30650c2|

* Lần 1: https://github.com/nguyenbabie1/PTIT\_CNTT4\_IT209\_SS11\_bai3.3/actions/runs/38426554735
* Lần 2: https://github.com/nguyenbabie1/PTIT\_CNTT4\_IT209\_SS11\_bai3.3/actions/runs/38426942094

## 3\. Minh chứng cache

* Log setup-java lần 1: \[Điền thông báo chưa tìm thấy cache].
* Log setup-java lần 2: \[Điền thông báo khôi phục cache thành công].

## 4\. Nhận xét

Thời gian workflow lần thứ hai giảm 17 giây, tương đương khoảng
28,8% so với lần thứ nhất.

Gradle Dependency Caching giúp tái sử dụng thư viện đã tải.
Cần đối chiếu log setup-java để xác nhận trạng thái cache của hai lần.
Thời gian workflow còn chịu ảnh hưởng của runner và mạng.

