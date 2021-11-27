# api_covid-19_vn
Api (nguyên gốc: https://static.pipezero.com/covid/data.json) + Giao diện (có thay đổi nhẹ) tìm thấy tại: https://covid19.gov.vn/ <br>
Các thông số đặt hidden ở giao diện gốc tức là không còn được update => sai<br>
Thông số được cập nhật theo dữ liệu tính từ 16h hôm trước tới 16h hôm sau của mỗi ngày<br>
Chưa thử biểu đồ (dữ liệu từ api có '.overview') <br>
<b>Cấu trúc json:</b><br>
json = {total: {…}, today: {…}, overview: Array(7), locations: Array(63)} <br>
<b>json.total:</b> {internal: {…}, world: {…}} <br>
internal: {death: … treating: …, cases: …, recovered: …} <br>
world: {death: …, treating: …, cases: …, recovered: …} <br>
<b>json.today:</b> {internal: {…}, world: {…}} <br>
internal: {death: …, treating: …, cases: …, recovered: …} <br>
world: {death: …, treating: …, cases: …, recovered: …} <br>
<b>json.overview:</b> (7) [{…}, {…}, {…}, {…}, {…}, {…}, {…}] <br>
0: {date: '20-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
1: {date: '21-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
2: {date: '22-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
3: {date: '23-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
4: {date: '24-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
5: {date: '25-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
6: {date: '26-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
<b>json.locations:</b> (63) [{…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}] <br>
0: {name: 'TP. Hồ Chí Minh', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
1: {name: 'Bình Dương', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
2: {name: 'Đồng Nai', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
3: {name: 'Long An', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
4: {name: 'Tiền Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
5: {name: 'Tây Ninh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
6: {name: 'An Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
7: {name: 'Đồng Tháp', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
8: {name: 'Kiên Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
9: {name: 'Bình Thuận', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
1…: {name: 'Cần Thơ', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
11: {name: 'Sóc Trăng', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
12: {name: 'Bà Rịa – Vũng Tàu', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
13: {name: 'Khánh Hòa', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
14: {name: 'Bạc Liêu', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
15: {name: 'Hà Nội', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
16: {name: 'Vĩnh Long', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
17: {name: 'Cà Mau', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
18: {name: 'Đắk Lắk', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
19: {name: 'Bắc Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
2…: {name: 'Trà Vinh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
21: {name: 'Bến Tre', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
22: {name: 'Đà Nẵng', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
23: {name: 'Bình Phước', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
24: {name: 'Bắc Ninh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
25: {name: 'Nghệ An', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
26: {name: 'Hậu Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
27: {name: 'Hà Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
28: {name: 'Phú Yên', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
29: {name: 'Ninh Thuận', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
3…: {name: 'Bình Định', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
31: {name: 'Gia Lai', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
32: {name: 'Thừa Thiên Huế', death: 11, treating: …, cases: …, recovered: …, treating: … } <br>
33: {name: 'Quảng Nam', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
34: {name: 'Quảng Ngãi', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
35: {name: 'Quảng Bình', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
36: {name: 'Thanh Hóa', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
37: {name: 'Đắk Nông', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
38: {name: 'Lâm Đồng', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
39: {name: 'Phú Thọ', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
4…: {name: 'Hải Dương', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
41: {name: 'Hà Nam', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
42: {name: 'Nam Định', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
43: {name: 'Thái Bình', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
44: {name: 'Vĩnh Phúc', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
45: {name: 'Hà Tĩnh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
46: {name: 'Quảng Trị', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
47: {name: 'Hưng Yên', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
48: {name: 'Quảng Ninh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
49: {name: 'Điện Biên', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
5…: {name: 'Tuyên Quang', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
51: {name: 'Lạng Sơn', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
52: {name: 'Kon Tum', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
53: {name: 'Sơn La', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
54: {name: 'Ninh Bình', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
55: {name: 'Hòa Bình', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
56: {name: 'Hải Phòng', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
57: {name: 'Lào Cai', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
58: {name: 'Thái Nguyên', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
59: {name: 'Cao Bằng', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
6…: {name: 'Yên Bái', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
61: {name: 'Lai Châu', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
62: {name: 'Bắc Kạn', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
Demo tại: http://doanminhquang.github.io/api_covid-19_vn/ hoặc xem trực tiếp tại nguồn chính chủ: https://covid19.gov.vn/

