# Mẫu mod cho Vityaz Hero

Bấm **Use this template** để có kho của riêng bạn. Trong đó có hai mod chạy được, không cần mã:

| Thư mục | Là |
|---|---|
| `mods/my_panel` | một bảng số liệu |
| `mods/my_theme` | một giao diện: màu, cỡ chữ, nền |

Giữ thư mục bạn cần, xoá thư mục kia. Chỉ cần game và một chương trình sửa chữ. Hướng dẫn từng bước: [Cẩm nang Nhà sáng tạo](https://vityaz.ink.io.vn/mod/).

## Thử

1. Trong game, mở cửa sổ Tướng, bánh răng, **Mod**.
2. **Nhập thư mục**, chọn `mods/my_panel`.
3. Bấm nút mảnh ghép trên thanh mod để mở bảng.

Với `my_theme`: nhập xong thì mở lại game, rồi chọn nó trong Cài đặt, **Giao diện**.

## Đổi tên

Id dùng chữ thường, số và `_`. Tên mới phải giống nhau ở mọi chỗ:

- `my_panel`: thư mục `mods/my_panel`, thư mục `modules/my_panel`, `id` trong `bundle.json` và `module.json`, mục `modules`.
- `my_theme`: thư mục `mods/my_theme`, file `my_theme.json`, `id` trong `bundle.json` và trong file đó, mục `content`, file `locale/my_theme.csv`.

## Chia sẻ

Ghi tên bạn và một dòng giới thiệu vào `listing.json` của mod: trang [Mod cộng đồng](https://vityaz.ink.io.vn/mod/community/) hiện hai dòng đó.

Nộp mod vào [mods-community](https://github.com/Ink-vityaz/mods-community): chép thư mục mod vào `mods/` ở đó và mở một pull request.

Mẫu làm cho game 0.29.x. Giấy phép: MIT.
