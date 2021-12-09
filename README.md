# api_covid-19_vn
Api (nguyên gốc: https://static.pipezero.com/covid/data.json) + Giao diện (có thay đổi nhẹ) tìm thấy tại: https://covid19.gov.vn/ <br><br>
![api](https://github.com/doanminhquang/api_covid-19_vn/blob/main/api.png?raw=true)
<b>Lưu ý:</b><br>
&ensp;Các thông số đặt hidden ở giao diện gốc tức là không còn được update, hoặc update không đủ => sai<br>
&ensp;Thông số của Việt Nam được cập nhật vào khoảng 18:00 - 19:00 theo dữ liệu tính từ 16h hôm trước tới 16h hôm sau của mỗi ngày. Riêng dữ liệu về locations có sự thay đổi theo giời tgian theo từng tỉnh/thành phố<br>
&ensp;Chưa thử biểu đồ (dữ liệu từ api có '.overview') <br>
<b>Cấu trúc json:</b><br>
&ensp;<b>json = {total: {…}, today: {…}, overview: Array(7), locations: Array(63)}</b><br>
&ensp;<b>json.total:</b> {internal: {…}, world: {…}} <br>
&ensp;&ensp;internal: {death: … treating: …, cases: …, recovered: …} <br>
&ensp;&ensp;world: {death: …, treating: …, cases: …, recovered: …} <br>
&ensp;<b>json.today:</b> {internal: {…}, world: {…}} <br>
&ensp;&ensp;internal: {death: …, treating: …, cases: …, recovered: …} <br>
&ensp;&ensp;world: {death: …, treating: …, cases: …, recovered: …} <br>
&ensp;<b>json.overview:</b> (7) [{…}, {…}, {…}, {…}, {…}, {…}, {…}] <br>
&ensp;&ensp;0: {date: 'dd-mm', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&ensp;&ensp;1: {date: 'dd-mm', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&ensp;&ensp;2: {date: 'dd-mm', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&ensp;&ensp;3: {date: 'dd-mm', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&ensp;&ensp;4: {date: 'dd-mm', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&ensp;&ensp;5: {date: 'dd-mm', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&ensp;&ensp;6: {date: 'dd-mm', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&ensp;<b>json.locations:</b> (63) [{…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}] <br>
&ensp;&ensp;0: {name: 'TP. Hồ Chí Minh', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;1: {name: 'Bình Dương', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;2: {name: 'Đồng Nai', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;3: {name: 'Long An', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;4: {name: 'Tiền Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;5: {name: 'Tây Ninh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;6: {name: 'An Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;7: {name: 'Đồng Tháp', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;8: {name: 'Kiên Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;9: {name: 'Bình Thuận', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;10: {name: 'Cần Thơ', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;11: {name: 'Sóc Trăng', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;12: {name: 'Bà Rịa – Vũng Tàu', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;13: {name: 'Khánh Hòa', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;14: {name: 'Bạc Liêu', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;15: {name: 'Hà Nội', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;16: {name: 'Vĩnh Long', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;17: {name: 'Cà Mau', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;18: {name: 'Đắk Lắk', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;19: {name: 'Bắc Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;20: {name: 'Trà Vinh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;21: {name: 'Bến Tre', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;22: {name: 'Đà Nẵng', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;23: {name: 'Bình Phước', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;24: {name: 'Bắc Ninh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;25: {name: 'Nghệ An', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;26: {name: 'Hậu Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;27: {name: 'Hà Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;28: {name: 'Phú Yên', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;29: {name: 'Ninh Thuận', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;30: {name: 'Bình Định', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;31: {name: 'Gia Lai', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;32: {name: 'Thừa Thiên Huế', death: 11, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;33: {name: 'Quảng Nam', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;34: {name: 'Quảng Ngãi', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;35: {name: 'Quảng Bình', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;36: {name: 'Thanh Hóa', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;37: {name: 'Đắk Nông', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;38: {name: 'Lâm Đồng', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;39: {name: 'Phú Thọ', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;40: {name: 'Hải Dương', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;41: {name: 'Hà Nam', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;42: {name: 'Nam Định', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;43: {name: 'Thái Bình', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;44: {name: 'Vĩnh Phúc', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;45: {name: 'Hà Tĩnh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;46: {name: 'Quảng Trị', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;47: {name: 'Hưng Yên', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;48: {name: 'Quảng Ninh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;49: {name: 'Điện Biên', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;50: {name: 'Tuyên Quang', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;51: {name: 'Lạng Sơn', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;52: {name: 'Kon Tum', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;53: {name: 'Sơn La', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;54: {name: 'Ninh Bình', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;55: {name: 'Hòa Bình', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;56: {name: 'Hải Phòng', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;57: {name: 'Lào Cai', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;58: {name: 'Thái Nguyên', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;59: {name: 'Cao Bằng', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;60: {name: 'Yên Bái', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;61: {name: 'Lai Châu', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&ensp;&ensp;62: {name: 'Bắc Kạn', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
Demo tại: http://doanminhquang.github.io/api_covid-19_vn/ hoặc xem trực tiếp tại nguồn chính chủ: https://covid19.gov.vn/

