# api_covid-19_vn
Api (nguyên gốc: https://static.pipezero.com/covid/data.json) + Giao diện (có thay đổi nhẹ) tìm thấy tại: https://covid19.gov.vn/ <br>
Các thông số đặt hidden ở giao diện gốc tức là không còn được update => sai<br>
Thông số được cập nhật theo dữ liệu tính từ 16h hôm trước tới 16h hôm sau của mỗi ngày<br>
Chưa thử biểu đồ (dữ liệu từ api có '.overview') <br>
<b>Cấu trúc json:</b><br>
&nbsp;json = {total: {…}, today: {…}, overview: Array(7), locations: Array(63)} <br>
&nbsp;<b>json.total:</b> {internal: {…}, world: {…}} <br>
&nbsp;&nbsp;internal: {death: … treating: …, cases: …, recovered: …} <br>
&nbsp;&nbsp;world: {death: …, treating: …, cases: …, recovered: …} <br>
&nbsp;<b>json.today:</b> {internal: {…}, world: {…}} <br>
&nbsp;&nbsp;internal: {death: …, treating: …, cases: …, recovered: …} <br>
&nbsp;&nbsp;world: {death: …, treating: …, cases: …, recovered: …} <br>
&nbsp;<b>json.overview:</b> (7) [{…}, {…}, {…}, {…}, {…}, {…}, {…}] <br>
&nbsp;&nbsp;0: {date: '20-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&nbsp;&nbsp;1: {date: '21-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&nbsp;&nbsp;2: {date: '22-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&nbsp;&nbsp;3: {date: '23-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&nbsp;&nbsp;4: {date: '24-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&nbsp;&nbsp;5: {date: '25-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&nbsp;&nbsp;6: {date: '26-11', death: …, treating: …, cases: …, recovered: …, treating: …} <br>
&nbsp;<b>json.locations:</b> (63) [{…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}] <br>
&nbsp;&nbsp;0: {name: 'TP. Hồ Chí Minh', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;1: {name: 'Bình Dương', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;2: {name: 'Đồng Nai', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;3: {name: 'Long An', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;4: {name: 'Tiền Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;5: {name: 'Tây Ninh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;6: {name: 'An Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;7: {name: 'Đồng Tháp', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;8: {name: 'Kiên Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;9: {name: 'Bình Thuận', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;10: {name: 'Cần Thơ', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;11: {name: 'Sóc Trăng', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;12: {name: 'Bà Rịa – Vũng Tàu', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;13: {name: 'Khánh Hòa', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;14: {name: 'Bạc Liêu', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;15: {name: 'Hà Nội', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;16: {name: 'Vĩnh Long', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;17: {name: 'Cà Mau', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;18: {name: 'Đắk Lắk', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;19: {name: 'Bắc Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;20: {name: 'Trà Vinh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;21: {name: 'Bến Tre', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;22: {name: 'Đà Nẵng', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;23: {name: 'Bình Phước', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;24: {name: 'Bắc Ninh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;25: {name: 'Nghệ An', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;26: {name: 'Hậu Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;27: {name: 'Hà Giang', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;28: {name: 'Phú Yên', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;29: {name: 'Ninh Thuận', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;30: {name: 'Bình Định', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;31: {name: 'Gia Lai', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;32: {name: 'Thừa Thiên Huế', death: 11, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;33: {name: 'Quảng Nam', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;34: {name: 'Quảng Ngãi', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;35: {name: 'Quảng Bình', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;36: {name: 'Thanh Hóa', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;37: {name: 'Đắk Nông', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;38: {name: 'Lâm Đồng', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;39: {name: 'Phú Thọ', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;40: {name: 'Hải Dương', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;41: {name: 'Hà Nam', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;42: {name: 'Nam Định', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;43: {name: 'Thái Bình', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;44: {name: 'Vĩnh Phúc', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;45: {name: 'Hà Tĩnh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;46: {name: 'Quảng Trị', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;47: {name: 'Hưng Yên', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;48: {name: 'Quảng Ninh', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;49: {name: 'Điện Biên', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;50: {name: 'Tuyên Quang', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;51: {name: 'Lạng Sơn', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;52: {name: 'Kon Tum', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;53: {name: 'Sơn La', death:  …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;54: {name: 'Ninh Bình', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;55: {name: 'Hòa Bình', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;56: {name: 'Hải Phòng', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;57: {name: 'Lào Cai', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;58: {name: 'Thái Nguyên', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;59: {name: 'Cao Bằng', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;60: {name: 'Yên Bái', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;61: {name: 'Lai Châu', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
&nbsp;&nbsp;62: {name: 'Bắc Kạn', death: …, treating: …, cases: …, recovered: …, treating: … } <br>
Demo tại: http://doanminhquang.github.io/api_covid-19_vn/ hoặc xem trực tiếp tại nguồn chính chủ: https://covid19.gov.vn/

