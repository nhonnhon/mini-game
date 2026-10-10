# BON BOSS Hub

Kho game web nhỏ rèn phản xạ, trí nhớ và tư duy số — thân thiện trẻ **6–8 tuổi**, chạy tốt trên điện thoại & iPad.

Mở `index.html` để vào hub chọn game. Không cần build.

## Công nghệ

- HTML + JavaScript inline (mỗi game 1 file)
- [Tailwind CSS](https://tailwindcss.com/) qua CDN
- Highscore / tiến độ lưu `localStorage` (một số game)
- Layout gọn: header mỏng + bàn chơi full màn hình, không scroll

## Danh sách game trên hub

### Dành cho bé 6–8 tuổi

| # | Game | File | Cách chơi | Cấu hình |
| --- | --- | --- | --- | --- |
| 1 | **Tìm Hình Khác** | `find_odd.html` | Tìm ô emoji khác biệt trong lưới | N = **10–20** (mặc định 10) |
| 2 | **Bấm Theo Mẫu** | `sequence_tap.html` | Mẫu hiện sẵn phía trên, bấm đúng thứ tự con vật | Độ dài 2 / 3 / 4 bước |
| 3 | **Xếp Số** | `catch_sort.html` | Trượt các **số to** về đúng thứ tự (ô trống để trượt) | Lưới **2×2** hoặc **3×3** |
| 4 | **Đếm Emoji** | `count_emoji.html` | Đếm số emoji trên màn hình, chọn đáp án đúng | Đếm tối đa 5 / 8 / 12 |

### Phản xạ & trí nhớ nâng cao

| # | Game | File | Cách chơi | Cấu hình |
| --- | --- | --- | --- | --- |
| 5 | **Lưới Schulte (NxN)** | `tim-so.html` | Tìm tuần tự từ 1 → N², càng nhanh càng tốt | N = 3–10; highscore theo từng N×N |
| 6 | **Lật Thẻ Trí Nhớ** | `memory_match.html` | Lật thẻ, ghép cặp emoji trùng nhau | Số cặp 4–18; thời gian 10–180s |

## Chi tiết nhanh từng game

### Tìm Hình Khác (`find_odd.html`)
Lưới đầy emoji gần giống nhau, **1 ô khác**. Bấm đúng → +điểm, sang vòng mới. Lưới lớn thì ô tự thu nhỏ để vừa 1 màn hình.

### Bấm Theo Mẫu (`sequence_tap.html`)
Không cần nhớ mù: chuỗi mẫu **luôn hiện** phía trên (có highlight bước đang làm). Bé bấm 4 nút con vật theo đúng thứ tự. Sai → làm lại từ đầu cùng mẫu.

### Xếp Số (`catch_sort.html`)
Puzzle trượt số kiểu 15-puzzle: chỉ hiện **số lớn**, không dùng emoji. Trượt ô kề chỗ trống đến khi `1 → 2 → 3 …` đúng thứ tự. Đếm số bước.

### Đếm Emoji (`count_emoji.html`)
Hiện một đống emoji giống nhau, chọn số đúng trong 4 đáp án. Điểm + vòng tăng khi trả lời đúng.

### Lưới Schulte (`tim-so.html`)
Lưới số xáo trộn, bấm tuần tự 1, 2, 3… Thời gian bắt đầu khi bấm số 1. Best time lưu theo kích thước lưới. Có nút ← về hub; setup N ở thanh dưới.

### Lật Thẻ Trí Nhớ (`memory_match.html`)
Memory match emoji cổ điển: lật 2 thẻ, khớp thì giữ, sai thì úp. Hết giờ thua; ghép hết trước hết giờ thắng. Header gọn + setup ở footer.

## Archive (không hiện trên hub)

| File | Ghi chú |
| --- | --- |
| `archive_time_attack.html` | Săn số theo thời gian ngắn (bản cũ) |
| `archive_endless_combo.html` | Săn điểm 60 giây (bản cũ) |

## Cấu trúc thư mục

```
tim-so/
├── index.html                  # Hub chọn game
├── find_odd.html               # Tìm hình khác
├── sequence_tap.html           # Bấm theo mẫu
├── catch_sort.html             # Xếp số (2×2 / 3×3)
├── count_emoji.html            # Đếm emoji
├── tim-so.html                 # Lưới Schulte
├── memory_match.html           # Lật thẻ trí nhớ
├── archive_time_attack.html
├── archive_endless_combo.html
└── README.md
```

## Chạy local

Mở trực tiếp file HTML trong trình duyệt, hoặc phục vụ thư mục:

```bash
npx serve .
```

Rồi vào trang chủ (thường `http://localhost:3000`).
