# 📊 Hướng Dẫn Sử Dụng Extension Ahrefs Data Scraper

## 🎯 Chức Năng Chính
Extension giúp bạn trích xuất dữ liệu từ bảng Ahrefs với các tính năng nâng cao:

### 📊 Dữ liệu cào được:
- **Target** (Tên miền)
- **DR** (Domain Rating)
- **RD** (Referring Domains) 
- **Top 20** (Từ khóa trong top 20)
- **Organic Traffic** (Lượng truy cập tự nhiên)
- **Keywords** (Số từ khóa)

### 🚀 Tùy chọn xuất:
- **📁 File Excel/CSV** - Tải về máy
- **📈 Google Sheets** - Upload trực tiếp với OAuth
- **🎨 Conditional Formatting** - Tô màu tự động theo điều kiện

### 🎯 Tính năng đặc biệt:
- **💰 Phân tích giá Traffic** - So sánh với bảng giá chuẩn
- **💱 Tỉ giá tùy chỉnh** - Quy đổi USD/VND (mặc định: 26.500)
- **📅 Chọn ngày upload** - Linh hoạt thời gian
- **🧹 Làm sạch dữ liệu** - Loại bỏ trùng lặp và domain không hợp lệ

## 🚀 Cài Đặt Extension

### Bước 1: Chuẩn bị
1. Mở Chrome browser
2. Đảm bảo có quyền "Developer mode"

### Bước 2: Load Extension
1. Gõ `chrome://extensions/` vào thanh địa chỉ
2. Bật **"Developer mode"** (góc trên bên phải)
3. Click nút **"Load unpacked"**
4. Chọn thư mục `ahref-extension`
5. Extension sẽ xuất hiện với icon trong thanh công cụ

### Bước 3: Kiểm tra
- Thấy icon "Ahrefs Data Scraper" trong thanh extensions
- Click vào sẽ hiện popup với nút "Scrape Data & Export to Excel"

## 📝 Cách Sử Dụng

### Bước 1: Vào trang Ahrefs
- Truy cập `https://ahrefs.com`
- Hoặc bất kỳ subdomain nào: `app.ahrefs.com`, `site-explorer.ahrefs.com`
- Vào trang có **bảng dữ liệu** (Site Explorer, Keywords Explorer...)

### Bước 2: Cấu hình tùy chọn (nếu cần)
1. **Ngày Upload**: Mặc định hôm nay, có thể chọn ngày khác
2. **Tỉ giá USD/VND**: Mặc định 26.500, có thể điều chỉnh
3. **Column Mapping**: Cấu hình trong tab "Google Sheets" (nếu dùng Sheets)

### Bước 3: Scrape dữ liệu
1. **Click icon extension** trên thanh công cụ
2. **Click "Cào Dữ Liệu"** - extension sẽ phân tích trang
3. Chờ extension xử lý (nút sẽ hiện "Đang cào...")
4. Thông báo thành công hiện ra với số bản ghi tìm thấy

### Bước 4: Chọn hành động
**Tùy chọn 1: Tải file Excel**
- Click **"Tải file Excel"**
- File CSV tự động download với tên: `ahrefs_data_YYYY-MM-DD.csv`

**Tùy chọn 2: Upload Google Sheets**
- Click **"Upload lên Google Sheets"**
- Dữ liệu được upload với conditional formatting tự động

## 🔧 Xử Lý Lỗi

### Lỗi: "Please navigate to an Ahrefs page first"
**Nguyên nhân:** Không ở trang ahrefs.com
**Giải pháp:** Vào trang ahrefs.com trước khi sử dụng

### Lỗi: "Ahrefs table not found on this page" 
**Nguyên nhân:** Trang không có bảng dữ liệu
**Giải pháp:** Vào trang có bảng data (Site Explorer, Keywords...)

### Lỗi: "No data found on this page"
**Nguyên nhân:** Bảng trống hoặc chưa load xong
**Giải pháp:** 
- Chờ trang load hoàn toàn
- Refresh trang và thử lại

### Lỗi: "Error occurred while scraping data"
**Nguyên nhân:** Lỗi extension hoặc trang đã thay đổi
**Giải pháp:**
- Reload extension: `chrome://extensions/` → Reload
- Refresh trang Ahrefs
- Thử lại

## 📋 Format File Xuất Ra

File CSV có cấu trúc:
```
Target,DR,Keywords,Top 20,Organic Traffic,Referring domains
example.com,75,1234,257,12.5K,445
domain.net,82,2156,457,23.8K,678
```

## 💡 Tips Sử Dụng

1. **Đợi trang load xong** trước khi scrape
2. **Có thể scrape nhiều lần** trên cùng trang
3. **File tự động đặt tên** theo ngày tháng
4. **Hỗ trợ tất cả subdomain** của Ahrefs
5. **Dữ liệu mở được bằng Excel** hoặc Google Sheets

## 🔒 Bảo Mật & Quyền

Extension chỉ yêu cầu quyền:
- ✅ `activeTab`: Truy cập tab hiện tại
- ✅ `storage`: Lưu settings
- ✅ `downloads`: Download file CSV
- ✅ `ahrefs.com`: Chỉ hoạt động trên Ahrefs

**Không thu thập dữ liệu cá nhân hay gửi data ra ngoài.**

## 📈 Google Sheets Integration

[//]: # (### Setup Google Sheets &#40;Lần đầu&#41;)

[//]: # (1. **Tạo OAuth Client ID** - Theo hướng dẫn trong [OAUTH-SETUP-GUIDE.md]&#40;OAUTH-SETUP-GUIDE.md&#41;)

[//]: # (2. **Cấu hình Extension**:)

[//]: # (   - Tab "Google Sheets" → Nhập Spreadsheet ID)

[//]: # (   - Cấu hình Column Mapping &#40;DR, RD, Top20, Traffic, Keywords&#41;)

[//]: # (   - Paste OAuth Client ID)

[//]: # (3. **Authorize Account** - Click "Xác Thực Google Account")

[//]: # (4. **Test Connection** - Kiểm tra kết nối)

### Column Mapping (Thứ tự mới)
- **AK**: DR (Domain Rating)
- **AL**: RD (Referring Domains)  
- **AM**: Top 20 (Keywords trong top 20)
- **AN**: Traffic (Organic Traffic)
- **AO**: Keywords (Tổng số keywords)

## 🌈 Conditional Formatting

### Quy tắc tô màu tự động:
1. **DR**: ≥ 10 🟢 | < 10 🔴
2. **RD**: ≥ 50 🟢 | < 50 🔴  
3. **Top 20**: > 1 🟢 | ≤ 1 🔴
4. **Traffic**: Giá ≤ Expected 🟢 | Giá > Expected 🔴

### Bảng giá Traffic (với tỉ giá 26.500):
| Traffic | Giá USD | Giá VND | Kết quả |
|---------|---------|---------|---------|
| < 10k | ≤ $45 | ≤ 1.192.500 | 🟢 |
| 10k-20k | ≤ $65 | ≤ 1.722.500 | 🟢 |
| 20k-50k | ≤ $110 | ≤ 2.915.000 | 🟢 |
| 50k-100k | ≤ $130 | ≤ 3.445.000 | 🟢 |
| 100k-500k | ≤ $180 | ≤ 4.770.000 | 🟢 |

## 🧹 Data Cleaning

Extension có tab "Clean Data" để làm sạch danh sách domain:

### Tính năng:
- ✅ Loại bỏ protocol (http://, https://)
- ✅ Xóa trailing slashes
- ✅ Remove duplicates
- ✅ Lọc domain không hợp lệ
- ✅ Chuẩn hóa format

### Cách sử dụng:
1. Tab "Clean Data"
2. Paste danh sách domain vào ô input
3. Click "Clean & Remove Duplicates"
4. Copy kết quả đã làm sạch

## ⚙️ Tabs Extension

Extension có 3 tabs chính:

### 🎯 Tab "Scrape Data"
- Cào dữ liệu từ Ahrefs
- Cấu hình ngày upload và tỉ giá
- Tải Excel hoặc Upload Google Sheets

### 🧹 Tab "Clean Data"  
- Làm sạch danh sách domain
- Loại bỏ trùng lặp
- Chuẩn hóa format

### ⚙️ Tab "Google Sheets"
- Cấu hình OAuth và Spreadsheet
- Column mapping
- Test connection

## 🔧 Troubleshooting Google Sheets

### "OAuth client not found"
- Kiểm tra Client ID đúng format
- Đảm bảo Extension ID chính xác trong Google Cloud Console

### "Không tìm thấy dữ liệu cho ngày"
- Kiểm tra cột B có ngày được chọn không
- Format ngày: DD/MM/YYYY hoặc YYYY-MM-DD

### "Access denied" 
- Chưa authorize Google account
- Click "Xác Thực Google Account"

## 📞 Hỗ Trợ

Nếu gặp vấn đề:
1. Check console logs (F12)
2. Reload extension
3. Refresh trang Ahrefs
4. Kiểm tra extension có hoạt động trên trang khác không

---
**Version:** 2.0 | **Tương thích:** Chrome Extensions Manifest V3 | **Google Sheets API v4**
