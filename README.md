# Rổ Phim Cô Tư TV — Bản phát hành

Repo này **chỉ chứa file cài đặt (APK)** của app **Rổ Phim Cô Tư TV** dành cho Android TV / Google TV.
Mã nguồn nằm ở một repo riêng và không được công khai.

## Tải app

Vào mục **[Releases](../../releases/latest)** rồi tải file `CoTuPhim-TV-universal.apk`.

APK là bản **universal** — chạy được trên mọi Android TV box, TV Google, và cả điện thoại/máy tính bảng Android.

## Cài đặt

**Cách 1 — cập nhật ngay trong app (khuyên dùng)**

App có sẵn tính năng tự cập nhật. Vào **Cài đặt** (biểu tượng bánh răng ở góc phải trên) → **Kiểm tra cập nhật**.
App sẽ tự đối chiếu với bản mới nhất ở đây, tải về và mở trình cài đặt giúp bạn.

**Cách 2 — cài thủ công qua adb**

```bash
adb install -r CoTuPhim-TV-universal.apk
```

**Cách 3 — cài từ USB / trình duyệt file**

Chép file APK vào USB, cắm vào TV rồi mở bằng một trình duyệt file bất kỳ (ví dụ *File Commander*, *X-plore*).
Lần đầu cài, Android sẽ hỏi cấp quyền *"Cài đặt ứng dụng không xác định"* — hãy chấp nhận.

## Lưu ý khi cập nhật

Bản mới luôn được ký bằng cùng một khóa nên **cài đè trực tiếp được**, không mất dữ liệu và không cần gỡ bản cũ.

Riêng trường hợp **tên app đổi**, launcher của Google TV có thể vẫn hiện tên cũ do nó lưu cache riêng.
Khi đó gỡ hẳn rồi cài lại là xong:

```bash
adb uninstall ro.cotuphim.tv
adb install CoTuPhim-TV-universal.apk
```

## Thông tin app

| | |
|---|---|
| Package | `ro.cotuphim.tv` |
| Nền tảng | Android TV / Google TV (leanback), chạy được cả trên Android thường |
| ABI | `arm64-v8a`, `armeabi-v7a`, `x86_64` |
