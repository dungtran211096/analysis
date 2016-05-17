<a name="top"></a>
# Tìm hiểu về add-ons

##Contents:
- [1.What's add-on?](#concept)
- [2.Developing add-ons](#develop)
- [3.Installation add-on SDK](#install)

===
### 1.What's add-on
<a name="concept"></a>
    Add-on hay tiện ích mở rộng, là các tiện ích được cài thêm vào ngoài các tiện ích có sẵn trên trình duyệt, nó được tạo ra nhờ các lập trình viên(dev) 
	Ngôn ngữ viết: HTML, CSS, Javascript, và các API(API là viết tắt của Application Programming Interface (giao diện lập trình ứng dụng)
	Một số tính năng:
<ul> 
   Tùy vào mục đích của lập trình viên hay nhu cầu của người dùng mà add-on được tạo ra có chức năng khác nhau như: chặn quảng cáo( Vd: APB(*)), Thông báo, download, thay đổi giao diện trang web( vd: Clip in web-CocCoc)
</ul>

<a name="develop"></a>
### 2.Developing add-ons
 Cách tạo một add-on: Sử dụng WebExtension(**) hoặc Add-on SDK

-Add-on SDK( Software Development Kit – một bộ công cụ phát triển phần mềm) 
Cài đặt SDK và sử dụng các công cụ JPM để phát triển, thử nghiệm, và đóng gói add-on

### 3.Installation add-on SDK
Installation
jpm is distributed with the node package manager npm.
Installing npm
There are two ways to get npm.
•	Download and install Node.js from nodejs.org. Node.js includes npm.
•	Or, if you have a package manager like APT, install npm via that. For example, in an Ubuntu or Debian terminal window, enter sudo apt-get install nodejs nodejs-legacy npm.
To test your installation, run:
/usr/bin/env node -v
If you get an error message saying  /usr/bin/env: node: No such file or directory and you have installed nodejs through a package manager, nodejs may have been installed under a different executable name. To ensure compatibility with jpm, however, it must be present in your PATH under the name node. On Debian and Ubuntu, this can be remedied by ensuring you installed the compatibility package, nodejs-legacy:
sudo apt-get install nodejs-legacy
On other distributions, you may have to create a local symlink to nodejs manually:
sudo ln -s "$(which nodejs)" /usr/local/bin/node
Installing jpm
After you have npm installed and node on your PATH, install jpm just as you would any other npm package.
Installing jpm globally
npm install jpm --global
Depending on your setup, you might need to run this as an administrator: sudo npm install jpm --global
Installing jpm locally
If you do not wish to, or are unable to, install jpm globally, you may instead install it locally:
npm install jpm
To run jpm from a terminal when installed locally, you must add the directory"$HOME/node_modules/.bin/" to your terminal's PATH first. Add the following line to the end of the file $HOME/.profile to add it to your PATH permanently (as the file .profile is executed every time a new terminal is opened):
export PATH="$HOME/node_modules/.bin/:$PATH"
Installing jpm from git
Alternatively, you can also get the latest version of jpm using git:
git clone https://github.com/mozilla-jetpack/jpm.git
cd jpm
npm install
npm link
After installing jpm
After installation, at the command prompt, type:
jpm
You should see a screen summarizing the available jpm commands. Note that unlike cfx, jpm is available in every command prompt you start, as long as you installed it with the --global flag.

