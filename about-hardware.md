# Nói về phần cứng

Surface Go là dòng tablet chạy hệ điều hành Windows do Microsoft phát triển và bán ra. Nó được nhắm đên các học sinh, sinh viên, những người muốn có một thiêt bị tác vụ gọn nhẹ, có thể xách đi khắp nơi. Vơi giá 399 đô, nó có thể coi như là chiếc Surface rẻ nhất từng được bán ra (không tính các phụ kiện)...

Thôi, không nói vòng vo nữa, nhức đầu lắm he (theo cách nói của bạn Cẩm Ly). Giờ chúng ta sẽ bàn về phần cứng của nó. (Bài này mình viết ra trước khi Surface Go 3 ra mắt, dựa trên thông tin leak ra)

## Cấu hình

Surface Go 3 sẽ có 2 cấu hình, cấu hình thứ nhất được xuất hiện trên phiên bản rẻ hơn là cấu hình sử dụng bộ xử lý [Intel Pentium Gold 6500Y](https://ark.intel.com/content/www/vn/vi/ark/products/213357/intel-pentium-gold-6500y-processor-4m-cache-up-to-3-40-ghz.html) và cấu hình thứ hai được xuât hiện trên phiên bản đắt hơn là cấu hinh sử dụng bộ xử lý [Intel i3-10100Y](https://ark.intel.com/content/www/vn/vi/ark/products/213356/intel-core-i310100y-processor-4m-cache-up-to-3-90-ghz.html). Phiên bản câu hình thấp hơn sẽ có 4/8GB RAM, 64GB eMMC/128GB SSD. Cao hơn thì chỉ có bản 8GB RAM, 128GB SSD. Chưa rõ Microsoft có ra phiên bản 256GB hay không, nhung nếu có thì rất tuyệt (Đặc biệt dành cho ai muốn dual boot Windows và macOS) (Update: Tin xấu là thằng Mic nó đ ra bản 256GB thật, đ hiểu vì răng cứ vong vo chắc bản 64 và 128, đ hiểu nổi thăng Mic, theo cách nói của bạn Cẩm Ly)

### CPU

Cả hai bộ xử lý đều là bộ xử lý đến từ Intel, và chúng đều có một điểm chung là... đều là những con chip thuộc dòng siêu tiết kiệm điện (Y),.. đều yếu hết. Chúng còn có một điêm chung là đều thuộc cùng một kiến trúc là Amber Lake Y (Surface Go 2 cũng dùng con chip thuộc thế hệ này, Go 1 thì là Kaby Lake Y). Về hiệu năng thì yếu, Pentium Gold 6500Y trên phiên bản thâp hơn thì mọi người có thể hình dung nó như là con m3-8100Y (Con chip được dùng trên dòng cao cấp hơn của Surface Go 2). Về bản chất thì hai con chip này giống nhau, chỉ khác ở chỗ nó nơi mức TDP-up của dòng m3-8100Y lên tới 8W, còn Pentium Gold 6500Y chỉ có TDP-up lên tới 7W mà thôi. TDP-down của chúng cũng thế, Pentium Gold thì kém hơn 1W so với m3-8100Y. i3-10100 thì cũng có mức TDP, TDP-up/down ngang Pentium Gold 6500Y (Có lẽ giúp cho chiếc máy tiêt kiệm pin hơn chăng?)

### iGPU

Lại là một điểm chung khác của hai con chip đó, chúng đều có GPU thích hợp là Intel UHD 615 (Surface Go 2 cũng dùng iGPU này, Go 1 thì dùng **HD 615**) (Thằng Microsoft đúng là ác ôn, nâng chip nhưng không nâng cấp iGPU, và dĩ nhiên, đâu phải cái này là đổ lỗi cho Microsoft hoàn toàn được?).

Dưới đây là danh sách các ID Thiết Bị (device-id) của các dòng Intel từng thích hợp lên Surface Go (SG) 1-3:

|      **CPU**    | Pentium Gold 4415Y (SG 1 ) | Pentium Gold 4425Y (SG 2) | Core m3-8100Y (SG 2) | Pentium Gold 6500Y (SG 3) | Core i3-10100Y (SG 3) |
|-----------------|----------------------------|---------------------------|----------------------|---------------------------|-----------------------|
|     **iGPU**    |           HD 615           |          UHD 615          |        UHD 615       |           UHD 615         |         UHD 615       |  
|  **device-id**  |           0x591E           |         0x591E            |        0x591C        |          0x591C           |         0x591C        |
