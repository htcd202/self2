# Self-Bot Discord Relay

Bot tự động phát hiện từ khóa trong tin nhắn và gửi phản hồi đến kênh đích.

## Tính năng

- Phát hiện từ khóa trong tin nhắn từ kênh nguồn
- Tự động gửi phản hồi đến kênh đích qua Discord API
- Hỗ trợ nhiều từ khóa tùy chỉnh

## Cài đặt

### Cách 1: Sử dụng file .env (Khuyến nghị cho Railway/Deployment)

1. Cài đặt dependencies:
```bash
pip install -r requirements.txt
```

2. Tạo file `.env`:
```bash
cp .env.example .env
```

3. Chỉnh sửa `.env` và điền thông tin của bạn:
```env
USER_TOKEN=your_token_here
CHANNEL_ID_NGUON=123456789012345678
CHANNEL_ID_DICH=987654321098765432
```

4. Chạy bot:
```bash
python main.py
```

### Cách 2: Sử dụng file config.py (Local)

1. Tạo file cấu hình:
```bash
cp config.example.py config.py
```

2. Chỉnh sửa `config.py` và điền thông tin của bạn

3. Chạy bot:
```bash
python main.py
```

## Deploy lên Railway

1. Fork/Clone repository này
2. Tạo project mới trên Railway
3. Connect với GitHub repository
4. Thêm các Environment Variables trong Railway:
   - `USER_TOKEN`: Token của bạn
   - `CHANNEL_ID_NGUON`: ID kênh nguồn
   - `CHANNEL_ID_DICH`: ID kênh đích
5. Railway sẽ tự động detect và deploy

## Cấu hình

Chỉnh sửa `KEYWORD_RESPONSES` trong `main.py` để thêm/sửa từ khóa và phản hồi.

## Lưu ý

- Không commit token lên GitHub
- Sử dụng user token (self-bot), không phải bot token
- Đảm bảo bot có quyền đọc tin nhắn trong kênh nguồn và gửi tin nhắn trong kênh đích

