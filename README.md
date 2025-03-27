## HOW TO MAKE A BOT DISCORD
## BƯỚC 1: Cài đặt `Node.js`
- JavaScript cần có Node.js để chạy ngoài trình duyệt, và bot Discord cũng chạy bằng `Node.js`.
### 1. Kiểm tra xem máy bạn đã có Node.js chưa
- Mở Command Prompt (cmd) hoặc PowerShell (bấm `Windows + R`, nhập cmd, rồi Enter).
- Gõ lệnh sau và nhấn Enter ```node -v```
- Nếu hiện ra số phiên bản (ví dụ: v18.16.0), thì bạn đã có Node.js và có thể bỏ qua Bước 2.
- Nếu báo lỗi "node is not recognized", thì bạn chưa có Node.js và cần cài đặt ở bước tiếp theo.
## BƯỚC 2: Cài đặt Node.js
### 1. Tải `Node.js`
- Truy cập trang web chính thức: `https://nodejs.org/`
- Tải bản LTS (Long Term Support) (ổn định hơn).
- Nhấn vào file tải về và cài đặt như phần mềm bình thường (bấm Next liên tục).
### 2. Kiểm tra lại sau khi cài xong
- Mở lại cmd và gõ ```node -v```
- Nếu hiện phiên bản `Node.js`, nghĩa là đã cài thành công.
### Cài xong `Node.js` thì bạn cũng có sẵn npm (Node Package Manager). Kiểm tra bằng lệnh `npm -v`
### Thêm PATH 
- Bấm `Windows + S`
- Tìm kiếm và mở `edit the system environment variables`
- Chọn tab Advanced, nhấn vào Environment Variables....
- Ở phần System variables, tìm biến Path, nhấn Edit....
- Nhấn New, thêm các đường dẫn sau (tùy vào thư mục cài đặt Node.js):
```
C:\Program Files\nodejs\
C:\Users\<Tên-user>\AppData\Roaming\npm\
```
- (Thay <Tên-user> bằng tên tài khoản Windows của bạn)
## BƯỚC 3: Cài đặt VS Code và mở dự án
### 1. Nếu chưa có VS Code
- Tải về từ `https://code.visualstudio.com/`
- Cài đặt bình thường (Next liên tục).
### 2. Mở VS Code và tạo thư mục bot
- Mở VS Code.
- Tạo một thư mục mới ở Desktop (hoặc nơi bạn muốn), đặt tên "discord-bot".
- Trong VS Code, chọn File → Open Folder… và mở thư mục discord-bot vừa tạo.
## BƯỚC 4: Khởi tạo dự án Node.js
- Trong VS Code, mở Terminal (bấm `Ctrl + J`).
- Gõ lệnh sau để khởi tạo dự án Node.js ```npm init -y```
- Lệnh này sẽ tạo file package.json chứa thông tin của dự án.
## BƯỚC 5: Cài đặt thư viện discord.js
- Trong Terminal, gõ ```npm install discord.js```
- Lệnh này sẽ tải thư viện Discord.js để bot có thể kết nối với Discord.
## BƯỚC 6: Tạo file bot
- Trong VS Code, vào thư mục discord-bot.
- Tạo file mới tên `index.js`.
- Mở file `index.js`, dán code sau vào:
```
const { Client, GatewayIntentBits } = require('discord.js');
const client = new Client({ intents: [GatewayIntentBits.Guilds] });

client.once('ready', () => {
    console.log(`Bot đã online!`);
});

client.login('TOKEN_CỦA_BẠN');
```
### Lưu ý:
- Chỗ `TOKEN_CỦA_BẠN` cần thay bằng token bot Discord của bạn.
- Nếu chưa có token, xem tiếp bước dưới.
## BƯỚC 7: Tạo bot Discord và lấy token
### 1. Vào Discord Developer Portal
- Truy cập: `https://discord.com/developers/applications`
- Nhấn New Application, đặt tên tùy ý.
- Chọn tab Bot, nhấn Add Bot → Yes, do it!
- Kéo xuống, bật "Message Content Intent" (nếu muốn bot đọc tin nhắn).
- Nhấn Reset Token → Copy Token (lưu lại để thay vào code ở trên).
### 2. Thêm bot vào server Discord
- Vào tab OAuth2 → URL Generator.
- Ở phần Scopes, tích chọn bot.
- Ở phần Bot Permissions, chọn quyền cần thiết (ví dụ: Administrator).
- Kéo xuống, copy link, mở trình duyệt, dán link vào để thêm bot vào server.
## BƯỚC 8: Chạy bot
- Quay lại VS Code, mở Terminal.
- Gõ lệnh sau để chạy bot ```node index.js```
- Nếu hiện dòng "Bot đã online!", nghĩa là bot đã chạy thành công.
## BƯỚC 9: Kiểm tra bot trên Discord
- Mở Discord, vào server mà bạn đã thêm bot.
- Kiểm tra xem bot có online không. Nếu có, bot đã chạy thành công.
