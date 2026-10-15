# BÀI LÀM – HACKATHON 01

- **Mã đề:** 03
- **Họ tên: Trần Tuấn Anh** 
- **Lớp: CNTT4** 
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):Windows** 

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
- pwd
- ls
- Move-Item .\lich-tap.txt .\docs\
- Move-Item .\logo-phong-gym.PNG .\media\
- Copy-Item .\media\logo-phong-gym.PNG .\backup\
- rm .\temp_103.tmp
- cd .\logs\
- ls
- cd ..

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
    Directory: D:\Đề 003 - Phòng tập Gym\starter-kit\starter-kit\gym-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/15/2026   8:18 AM                backup
d-----        10/15/2026   8:13 AM                data
d-----        10/15/2026   8:17 AM                docs
d-----        10/15/2026   8:13 AM                logs
d-----        10/15/2026   8:17 AM                media
-a----        10/15/2026   8:06 AM             68 .env
-a----        10/15/2026   8:15 AM           2157 bai_lam.md

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
- Get-Content .\logs\member.log | Select-String "ERROR" > logs/daily_report.txt
- Get-Content .\logs\daily_report.txt
```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2025-11-28 07:26:18 [ERROR] Khong tim thay trang /lich-tap (404)
2025-11-28 07:29:18 [ERROR] Het thoi gian cho (timeout)
```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] Heading 1: tên dự án
- [x] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [x] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [x] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [x] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [x] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
- "# Script: auto_report.ps1
>> # Tac gia: TranTuanAnh
>> # Ngay tao: 10/15/2026" > logs/auto_report.txt
- Write-Host "Dang loc log..." > logs/auto_report.txt
-   "=== BAO CAO LOI ===" > logs/auto_report.txt
- Get-Content logs/member.log | Select-String "ERROR" >> logs/auto_report.txt
- Write-Host "Hoan thanh!" > logs/auto_report.txt

```

### Kết quả hiển thị

```text
(Dán kết quả vào đây – xoá dòng này)

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
(Get-Content logs/member.log | Select-String "ERROR").count
```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
7
```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
New-Item logs/tong_hop.txt
"=== TONG HOP LOG ===" > logs/tong_hop.txt
Get-Content logs/member.log | Select-String "WARNING" > logs/tong_hop.txt
Get-Content logs/member.log | Select-String "ERROR" > logs/tong_hop.txt
```

### Nội dung file logs/tong_hop.txt

```text
(Dán kết quả vào đây – xoá dòng này)

```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/dang_ky_thang_11.xlsx`, không cần ghi vào đây.
