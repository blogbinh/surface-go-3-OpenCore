# Surface Go 3 - macOS - OpenCore

![IMG_1683](https://user-images.githubusercontent.com/54268369/134372672-d387afc7-a9dc-4fbc-9c8a-cc1dc13f16d0.PNG)
* Đừng care tới con Surface Pro 8, mà hãy chú ý tới phiên bản mini nằm ở bên trái
* Do not care about the Surface Pro 8, let's pay attention to the mini on the left

Câu hình OpenCore để hỗ trợ macOS trên Surface Go 3

OpenCore configuration for support macOS on Surface Go 3

### Thông số của Surface Go 3:*
### Surface Go 3 Specs:*
|                               |  Cấu hình thấp hơn (Lower Specs)     |   Cấu hình cao hơn (Higer Specs)             |
|-------------------------------|--------------------------------------|----------------------------------------------|
|         **CPU**               | Intel® Pentium® Gold 6500Y Dual-core |   Intel® Core™ i3-10100Y Dual-core           |
|         **iGPU**              |     Intel® UHD Graphics 615          |                  <<                          |
|         **RAM**               |           4/8GB LPDDR3               |               8GB LPDDR3                     |
|  **Ổ lưu trữ / Storage**      |      64GB eMMC**, 128GB SSD          |               128GB SSD                      |
|         **Audio**             |              ALC(298)???             |                  <<                          |
| **Wifi + Bluetooth**          |   Intel® Wifi6 AX2??, Bluetooth 5.0  |                  <<                          |
|**Khe đọc thẻ nhớ/Card Reader**| Realtek PCI-E Card Reader, 152D:1237 |                  <<                          |
|**Cam Trước&Sau / Front&Rear Cam**|Intel(R) AVStream Camera 2500, ISP Interface, 8086:591c, 8 MPix/5 MPix|     <<    | 
| **Type Cover & Trackpad**     |Microsoft Type Cover, 045E:096F|                                      <<             |
|**Màn hình / Display**      |10.50 inch 3:2, 1920 x 1280 pixel 220 PPI, Hỗ trợ cảm ứng 10 điểm / 10-Point Capative|<<|
|      **Pin/Battery**          |26.81Wh 7.66v 3500mAh|            <<                                                 |


*: Thông số không phải là thông số chính thức và có thể sẽ thay đổi khi ra mắt

*: The Specs is not the offical specs and those can be changed before released

**: <span style="color:red">_**ĐẶC BIỆT LƯU Ý**_</span>: Do macOS không hỗ trợ ổ cứng **eMMC** nên sẽ **không thể cài** macOS trên cấu hình này được. Những người muốn hackintosh trên Surface Go 3 thì hãy tránh xa phiên bản thấp nhất này giúp mình (Lúc mình viết tới đoạn này thì có đứa hỏi mình rằng, ủa người ta đã mua Surface thì làm đ gì mà cài macOS lên, thế là mình ngay lập tức giật lấy con MacBook mà nó đang cầm trên lên, khởi động lại, nhân giữ phím Option trong lúc nó đang khởi động, vào phân vùng Boot Camp, và... à mà thôi chắc không nói mọi người cũng biêt rồi :)))) (Có cái này mình nhăc nhẹ lại là số lượng người cài Windows trên máy Mac nhiêu hơn số lượng người cài macOS trên Surface á:)

**: <span style="color:red">_**SPECIALLY NOTED**_</span>: Because macOS doesn't support **eMMC** so we **can't install** macOS on this configuration. For those who want to hackintosh on Surface Go 3, please avoid this low-end configuration (When I write to here, my friend has ask that, why the heck to install macOS on Surface, I immediately take the MacBook that he is holding, reboot it, hold the Option key on boot, boot into Boot Camp partition, and... no more because you will know what happen next even I don't say anything more :)))) (I want to say this again, that the number of user who install Windows is larger than the number of user who install macOS on Surface:)

Do Surface Go 1-3 không khác nhau nhiều lắm nên có thể lấy file EFI dùng cho Surface Go cũ hơn (dĩ nhiên có thể sẽ cần mod chút xíu)

Since Surface Go 1-3 aren't so much different so it is possible to use the EFI with older gens of Surface Go (although it required some modification)

### Cách tắt Sercure Boot:
### How to turn off the Sercure Boot:
1. Tắt máy và chờ tầm mười giây / Shut down the machine and wait about 10 seconds
2. Nhấn giữ phím Tăng âm lượng và - cùng một lúc - vừa ấn phím Nguồn và thả nó ra / Press and hold the Volume-up button and - at the same time - press and release the Power button
3. Khi logo của Microsoft xuất hiện, giữ phím Tăng âm lượng cho đến khi xuất hiện màn UEFI / As the Microsoft logo appears on your screen, continue to hold the Volume-up button until the UEFI screen appears
4. Chọn vào phần "Security" / Choose the "Security" page
![IMG_1575](https://user-images.githubusercontent.com/54268369/132239366-172856c6-8739-4ebb-b874-2f20048b151d.jpg)
5. Chọn vào nút "Enabled" ở mục "Secure Boot" và lựa chọn "Disabled" / Click the "Enable" button in "Sercure Boot" configuration and disable it
6. Khi khởi động lại mọi người sẽ thấy có vạch đỏ ở trên màn hình với hình ổ khoá bị mở ra / When reboot, you can see the red stripe on the screen with the "Unlock" icon
 
![IMG_1581-2](https://user-images.githubusercontent.com/54268369/132240600-1910f7c7-688a-4f44-8db8-dcb85f981139.jpg)

Hình ảnh của dòng Surface Pro 6. Do Surface Go 1-3 đều dùng UEFI đến từ bên thứ ba nên giao diện nhìn hơi củ chuối so với Pro 6 và các dòng còn lại:))) / The Surface Pro 6 shown here. Because Surface Go 1-3 use the third-party UEFI so the UI looks weird as the Pro 6 and other Surfaces:)))

P/s: Nhắc mới nhớ, Surface Pro 6 do dùng chip tên mã là Kaby Lake R 

EFI được làm bao gồm một số thành phần (dựa) trên file EFI của [@kingo132](https://github.com/kingo132) và [@badstorm](https://github.com/badstorm) . Rất cảm ơn!

EFI was made with some components (base) from [@kingo132](https://github.com/kingo132) and [@badstorm](https://github.com/badstorm) EFI file. Thank you so much!
