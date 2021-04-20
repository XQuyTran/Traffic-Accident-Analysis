# Khám phá dữ liệu

- Tại đây chứa các thông tin cơ bản về các trường dữ liệu trong file `../../Data/data_2018_2019.csv`

## Trường dữ liệu

- `Reference Number`: 

- `Grid Ref: Easting`: 

- `Grid Ref: Northing`: 

- `Number of Vehicles`: Số lượng phương tiên liên quan đến vụ tai nạn. Datatype = 'int64'

- `Accident Date`: Ngày xảy ra vụ tai nạn. Datatype = 'object'

- `Time (24hr)`: Thời gian xảy ra vụ tai nạn giao thông. Datatype = 'int64'.
    - Với a là giá trị cột "Time (24hr)". Thời gian cụ thể được tính:
        - Só giờ = (a - (a % 100)) // 100
        - Số phút = a % 100  

- `1st Road Class`: Tiền tố của tên đường. Datatype = 'object' 
    - Ở UK, tên đường được chia thành 2 phần: Tiền tố ứng với loại đường, hậu tố ứng với số đường
    - Phân loại tiền tố trong tập dữ liệu bao gồm
        - 1 - Motorway: Đường chính. Loại đường bao gồm nhiều làn xe, phục vụ cho việc lái xe đường trường với tốc độ cao.
        - 2 - A(M): 
        - 3 - A: Đường chính. Nhằm cung cấp liên kết giao thông quy mô lớn trong hoặc giữa các khu vực. Lưu lượng giao thông thấp hơn đường Motorway.
        - 4 - B: Đường phụ. Kết nối vào các đường loại A. Lưu lượng giao thông thấp hơn đường A.
        - 5 - C: Đường phụ. Kết nối vào các đường loại A và B. Lưu lượng giao thông thấp hơn đường B.
        - 6 - Unclassified: Đường phụ. Phục vụ cho giao thông địa phương. Lưu lượng giao thông thấp nhất trong các loại đường.

- `1st Road Class & No`: Tên đường hoàn chỉnh - chỉ một con đường duy nhất. Bao gồm tiền tố chỉ loại đường và số đường. Datatype = 'object'

- `Road Surface`: Điều kiện mặt đường lúc xảy ra tai nạn. Datatype = 'int64'
    - Được chia thành 5 loại:
        - 1: Khô ráo.
        - 2: Ẩm ướt.
        - 3: Snow.
        - 4: Đóng băng.
        - 5: Ngập nước.

- `Lighting Conditions`: Điều kiện ánh sáng tại thời điểm xảy ra tai nạn. Datatype = 'int64'
    - Được chia thành 5 loại:
        - 1: Buổi sáng, có đèn đường.
        - 2: Buổi sáng, không có đèn đường.
        - 3: Buổi sáng, không biết điều kiện đèn đường.
        - 4: Buổi tối, có đèn đường.
        - 5: Buổi tối, không có đèn đường.
        - 6: Buổi tối, không biết điều kiện đèn đường.

- `Weather Conditions`: 

- `Local Authority`: Mã thành phố nơi xảy ra tai nạn. Datatype = 'object'

- `Type of Vehicle`: Loại của phương tiện trong vụ tai nạn giao thông. Datatype = 'int64'
    - Gồm 20 loại:
        - 1: Xe có bàn đạp(pedal).
        - 2: Xe moto có phân khối <= 50cc.
        - 3: Xe moto có phân khối trong khoảng 50cc -> 125cc.
        - 4: Xe moto có phân khối trong 125cc -> 500cc.
        - 5: Xe moto có phân khối > 500cc.
        - 8: Xe taxi hoặc được cho thuê.
        - 9. Xe ô tô.
        - 10: Bux nhỏ (8 đến 16 chỗ).
        - 11: Xe khách hoặc xe bus (trên 17 chỗ).
        - 14: Các loại xe cơ giới khác.
        - 15: Các loại xe thô sơ khác.
        - 16: Có sử dụng ngựa.
        - 17: Xe nông nghiệp.
        - 18: Xe điện chạy trên đường ray (đường sắt nhẹ- thường được dùng trong đô thị).
        - 19: Phương tiện chở hàng <= 3.5 tấn.
        - 20: Phương tiện chở hàng từ 3.5 tấn -> 7.5 tấn.
        - 21: Phương tiện chở hàng > 7.5 tấn.
        - 22: Xe điện cơ động.
        - 90: Các phương tiện khác. 
        - 97: Xe moto chưa biết phân khối.

- `Casualty Class`: 

- `Casualty Severity`: 

- `Sex of Casualty`: Giới tính của nạn nhân vụ tai nạn giao thông. Datatype = 'int64'.
    - Gồm 2 loại:
        - 1: nam.
        - 2: nữ.

- `Age of Casualty`: 

## Tham khảo

- https://www.eastriding.gov.uk/environment/roads-streets-traffic-and-parking/roads-pavements-and-traffic/classification-of-roads/
