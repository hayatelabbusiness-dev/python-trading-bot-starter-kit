# 🚀 Python AI Trading Bot Starter Kit (Backtest 10,000 Candles)

> **Kho mã nguồn thực nghiệm đi kèm Video #1 kênh YouTube The Wealthy Coder (Code & Dòng Tiền)**  
> 📺 **Xem video phân tích & demo thực tế:** [The Wealthy Coder on YouTube](https://www.youtube.com/channel/UCqEGEkrMniKI3LPyOE9I85g)  
> 📌 **Kênh vệ tinh:** [TikTok: @labhayate](https://www.tiktok.com/@labhayate)

---

## 🎯 Giới Thiệu
Kho mã nguồn này cung cấp bộ khung (framework) Python hoàn chỉnh để:
1. **Kiểm thử chiến lược tự động (Backtesting)** trên hơn 10.000 cây nến lịch sử của Bitcoin / Crypto.
2. **Bóc tách lỗi Lookahead Bias và Phí sàn:** Hiểu rõ vì sao các đoạn code bot do AI (Claude, ChatGPT) sinh ra mặc định thường bị lỗ nặng trong môi trường thực tế.
3. **Bộ lọc định lượng nâng cao (Quant Filters):** Tích hợp bộ lọc sức mạnh xu hướng ADX và cơ chế quản trị quy mô vị thế theo biến động thực tế ATR, biến một hệ thống thua lỗ thành danh mục có kỳ vọng toán học dương.

---

## ⚡ Hướng Dẫn Cài Đặt & Chạy Trong 3 Bước

### Bước 1: Clone repo và tạo môi trường ảo
```bash
git clone https://github.com/hayatelabbusiness-dev/python-trading-bot-starter-kit.git
cd python-trading-bot-starter-kit

# Tạo môi trường ảo (khuyến nghị Python 3.10+)
python -m venv venv
# Kích hoạt trên Windows:
venv\Scripts\activate
# Kích hoạt trên Linux/macOS:
source venv/bin/activate
```

### Bước 2: Cài đặt các thư viện cần thiết
```bash
pip install -r requirements.txt
```

### Bước 3: Chạy thực nghiệm Backtest
```bash
python main.py
```

---

## 📊 Kết Quả Thực Nghiệm Trên 10.000 Nến 1H

| Chỉ số đo lường | Mô hình AI Naive (Mặc định) | Mô hình Quant Tối Ưu (The Wealthy Coder) |
| :--- | :---: | :---: |
| **Số lượng giao dịch** | 156 lệnh | 153 lệnh |
| **Tỷ lệ thắng (Win Rate)** | 59.0% | 56.2% |
| **Lợi nhuận ròng (Net Return)** | +26.4% *(Chưa tính phí ẩn & sideway)* | **+163.1%** *(Đã tính đủ phí sàn & trượt giá)* |
| **Mức sụt giảm tối đa (Max Drawdown)**| -4.0% | **-2.5%** |
| **Chỉ số Sharpe (Hệ số rủi ro)** | 1.82 | **4.76** |

---

## 📁 Cấu Trúc Thư Mục
```
python-trading-bot-starter-kit/
│
├── main.py                     # Entry point chạy backtest so sánh 2 mô hình
├── requirements.txt            # Danh sách thư viện (numpy, pandas, ccxt...)
├── .env.example                # File mẫu cấu hình API sàn giao dịch
│
├── strategies/
│   ├── ema_rsi_naive.py        # Chiến lược AI cơ bản (EMA 50/200 + RSI)
│   └── quant_momentum_atr.py   # Chiến lược Quant tối ưu (ADX Filter + Trailing Stop)
│
└── utils/
    ├── data_feed.py            # Module tải dữ liệu nến sàn Binance / Bybit
    └── metrics.py              # Hàm tính Winrate, Max Drawdown, Sharpe Ratio
```

---

## ⚠️ Tuyên Bố Miễn Trừ Trách Nhiệm (Disclaimer)
Mã nguồn này được phát triển cho mục đích giáo dục, nghiên cứu khoa học và minh họa kỹ thuật lập trình. Mọi thông tin không cấu thành lời khuyên đầu tư tài chính. Giao dịch tiền mã hóa và phái sinh tiềm ẩn rủi ro thanh lý vốn cao. Hãy luôn tự kiểm chứng dữ liệu trước khi vận hành vốn thật.

---

## 💼 Hợp Tác & Nhận Dự Án Ngoài (Commercial Inquiries)
- Bạn cần xây dựng bot giao dịch thuật toán theo yêu cầu riêng (Python, PineScript, C++)?
- Cần audit code bảo mật hoặc tối ưu hóa hiệu năng hệ thống định lượng?
- 📩 **Liên hệ hợp tác:** `contact.thewealthycoder@gmail.com`
- 💬 **Kênh trao đổi:** Để lại comment dưới các video YouTube mới nhất của chúng tôi.
