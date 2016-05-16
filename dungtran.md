<a name="top"></a>
# Tìm hiểu về add-ons

###Contents:
- [1.What's add-on?](#concept)
- [2.Developing add-ons](#develop)
  - [2.1 Create a new add-on](#create)
    - [2.1.1 WebExtensions](#extension)
    - [2.1.2 Add-on SDK](#sdk)
- [3.Installation add-on SDK](#install)
- [4.How to use SDK](#use)

===
### 1.What's add-on
<a name="concept"></a>
  Add-ons cho phép người phát triển mở rộng và thay đổi phạm vi thực hiện của functions của Firefox.Nó được viết bằng cách sử dụng công nghệ Web tiêu chuẩn-JS,HTML,CSS - thêm một vài hàm JS APIs.Trong số những thứ khác, add-ons có thể:
<ul> 
   <li>Thay đổi bề ngoài hoặc nội dung của các trang web cụ thể.</li>
   <li>Thay đổi giao diện user firefox</li>
   <li>Thêm tính năng mới cho firefox.</li>
</ul>

<a name="develop"></a>
### 2.Developing add-ons
 Hiện nay có một số toolsets để phát triển firefox add-ons.Nhưng WebExtensions sẽ trở thành tiêu chuẩn vào cuối năm 2017.Phần còn lại được dự kiến để deprecated trên cùng một khoảng thời gian.

 Ở đây bạn sẽ tìm thấy thông tin về những lựa chọn có sẵn để phát triển add-ons, bạn cần đưa ra quyết định cái gì tốt nhất với bạn bây giờ và trong tương lai.

<a name="create"></a>
## 2.1 Create a new add-on
 Nếu bạn sẽ viết 1 add-on mới, chúng tôi khuyên bạn chọn một trong 2 phương thức sau.Cho đến khi WebExtension được hoàn thành.Đây là có ích và không có ích với mỗi phương thức.Đọc hết các lựa chọn để đưa ra quyết định cái nào hiệu quả nhất cho bạn

<a name="extension"></a>
####2.1.1 Web extensions
 Là tương lai của FIrefox add-ons.nếu bạn có thể sử dụng WebExtensions API, nó sẽ là lựa chọn tốt nhất.Bạn có thể phát triển và pulish WEBEXtension ngay luôn,nhưng chúng vẫn đang ở giai đoạn đầu.
Hầu hết WebExtnesion APIs cũng có sẵn trên firefox for android
Firefox đang chuẩn bị phát hành phiên bảo đầy đủ đầu tiên cho firefox 48

<a name="sdk"></a>
####2.1.2 Add-on sdk
 Add-on SDK cung cấp APIs để phát triển firefox add-ons và tool để phát triển, kiểm tra,và đóng gói.
Chúng tôi khuyến khích chỉ sử dụng high-level APIs bởi vì nó sẽ làm dễ dàng hơn để  thay đổi sang webextensions trong tương lai.

<a name="install"></a>
### 3.Installation add-on SDK
B1: ``` sudo apt-get install nodejs nodejs-legacy npm. ```

B2: Kiểm tra đã cài:
```    /usr/bin/env node -v```

B3: Nếu có lỗi 
```  /usr/bin/env: node: No such file or directory ```
    Thì cài 
``` sudo apt-get install nodejs-legacy```

B4: Cài jpm 
``` sudo npm install jpm --global```
    Hoặc
```sh
git clone https://github.com/mozilla-jetpack/jpm.git*
cd jpm
npm install
npm link
```

B5: gõ
``` jpm ```
vào tạo add-ons

<a name="use"></a>
### 4.How to use SDK

B1: 
```sh
    mkdir my-addon
    cd my-addon
    jpm init
```

B2: Điền vào file **package.json**
``` https://developer.mozilla.org/en-US/Add-ons/SDK/Tools/package_json ```

B3: Mở file javascript đã tạo trong package.json

B4: Bắt đầu viết code.

B5: ``` jpm run ```

