# BÀI LÀM – THI THỬ HACKATHON 02 (GAMEZONE)

- **Họ tên:Phạm Viết Toàn** 
- **Lớp:CNTT3** 
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):** 

## 4.2. Thao tác CLI

### Các lệnh đã chạy

```shell
#
pwd
ls -Recurse
mv .\cap_nhat.txt .\docs
mv .\logo_gamezone.png .\media 
cp .\media\logo_gamezone.png .\backup\
rm .\temp_207.tmp
cd .\logs\
ls 
cd..
```

### Kết quả liệt kê toàn bộ dự án 

```text
Directory:
    C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\de-on-tap-game\starter-kit\gamezone-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/26/2026   1:37 PM                backup
d-----        10/26/2026   3:27 PM                data
d-----        10/26/2026   1:33 PM                docs
d-----        10/26/2026   2:42 PM                logs
d-----        10/26/2026   1:35 PM                media
-a----        10/26/2026   1:10 PM             70 .env
-a----        10/26/2026   2:37 PM            242 auto_report.ps1
-a----        10/26/2026   1:10 PM           1437 bai_lam.md


    Directory:
    C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\de-on-tap-game\starter-kit\gamezone-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           8542 logo_gamezone.png


    Directory:
    C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\de-on-tap-game\starter-kit\gamezone-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           5814 giao_dich_thang_11.xlsx


    Directory:
    C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\de-on-tap-game\starter-kit\gamezone-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM             61 cap_nhat.txt


    Directory:
    C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\de-on-tap-game\starter-kit\gamezone-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   2:37 PM            720 auto_report.txt
-a----        10/26/2026   1:53 PM            660 daily_report.txt
-a----        10/26/2026   1:10 PM            986 game.log
-a----        10/26/2026   2:42 PM            168 tong_hop.txt


    Directory:
    C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\de-on-tap-game\starter-kit\gamezone-website\media


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           8542 logo_gamezone.png
```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
Get-Content .\logs\game.log | Select-String "ERROR" >> .\logs\daily_report.txt
Get-Content .\logs\daily_report.txt
Get-Content .\logs\daily_report.txt -Head 3

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text

2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game

```

## 4.4. README.md

> Chấm trực tiếp trên `README.md` ở gốc dự án.

- [ ] Heading 1
- [ ] Mô tả in đậm + in nghiêng
- [ ] Bảng `Thư mục | Nội dung` (≥3 dòng)
- [ ] Code block lệnh liệt kê
- [ ] Task list (≥2 việc, ≥1 đã xong)
- [ ] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report

### Lệnh chạy

```shell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\auto_report.ps1
```

### Nội dung file logs/auto_report.txt

```text
Da tao bao cao: HOAN THIEN

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
# 
(Get-Content .\logs\game.log | Select-String "ERROR"). Count


```

### Kết quả đếm

```text
6

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
#
"=== TONG HOP LOG ===" > logs/tong_hop.txt
Get-Content logs/game.log | Select-String "WARNING" >> logs/tong_hop.txt
Get-Content logs/tong_hop.txt

```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG ===

2025-11-05 08:54:15 [WARNING] May chu qua tai CPU 90%

```

## 4.8. Excel

> Chấm trực tiếp trên file `data/giao_dich_thang_11.xlsx`.

