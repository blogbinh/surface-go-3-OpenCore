# Surface Go 3 - macOS - OpenCore

Câu hình OpenCore để hỗ trợ macOS trên Surface Go 3

OpenCore configuration for support macOS on Surface Go 3

### Thông số của Surface Go 3:*
### Surface Go 3 Specs:*
|                           |  Cấu hình thấp hơn (Lower Specs)     |   Cấu hình cao hơn (Higer Specs)     |
|---------------------------|--------------------------------------|---------------------------------------
|         **CPU**           | Intel® Pentium® Gold 6500Y Dual-core |   Intel® Core™ i3-10100Y Dual-core   |
|         **iGPU**          |     Intel® UHD Graphics 615          |                  <<                  |
|         **RAM**           |           4/8GB LPDDR3               |               8GB LPDDR3             |
|  **Ổ lưu trữ / Storage**  |      64GB eMMC**, 128GB SSD          |               128GB SSD              |
|         **Audio**         |              ALC(298)???             |                  <<                  |

*: Thông số không phải là thông số chính thức và có thể sẽ thay đổi khi ra mắt

*: The Specs is not the offical specs and those can be changed before released

**: <span style="color:red">_**ĐẶC BIỆT LƯU Ý**_</span>: Do macOS không hỗ trợ ổ cứng **eMMC** nên sẽ **không thể cài** macOS trên cấu hình này được. Những người muốn hackintosh trên Surface Go 3 thì hãy tránh xa phiên bản thấp nhất này giúp mình (Lúc mình viết tới đoạn này thì có đứa hỏi mình rằng, ủa người ta đã mua Surface thì làm đ gì mà cài macOS lên, thế là mình ngay lập tức giật lấy con MacBook mà nó đang cầm trên lên, khởi động lại, nhân giữ phím Option trong lúc nó đang khởi động, vào phân vùng Boot Camp, và... à mà thôi chắc không nói mọi người cũng biêt rồi :)))) (Có cái này mình nhăc nhẹ lại là số lượng người cài Windows trên máy Mac nhiêu hơn số lượng người cài macOS trên Surface á:)

**: <span style="color:red">_**SPECIALLY NOTED**_</span>: Because macOS doesn't support **eMMC** so we **can't install** macOS on this configuration. For those who want to hackintosh on Surface Go 3, please avoid this low-end configuration (When I write to here, my friend has ask that, why the heck to install macOS on Surface, I immediately take the MacBook that he is holding, reboot it, hold the Option key on boot, boot into Boot Camp partition, and... no more because you will know what happen next even I don't say anything more :)))) (I want to say this again, that the number of user who install Windows is larger than the number of user who install macOS on Surface:)

EFI được làm bao gồm một số thành phần dựa trên file EFI của [@kingo132](https://github.com/kingo132) và [@badstorm](https://github.com/badstorm) . Rất cảm ơn!

EFI was made with some components base from [@kingo132](https://github.com/kingo132) and [@badstorm](https://github.com/badstorm) EFI file. Thank you so much!
