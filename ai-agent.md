# Hướng dẫn cho AI Agent

Tài liệu này mô tả quy trình cập nhật series **Tử Vi Nam Phái** từ Facebook của tác giả Calvin Cường Nguyễn.

## Nguồn và cấu trúc

- Trang tác giả: <https://www.facebook.com/jian.nguyen.1>
- Album tham khảo: <https://www.facebook.com/media/set/?vanity=jian.nguyen.1&set=a.10232636128668385>
- Bài viết thường bắt đầu bằng `TỬ VI NAM PHÁI - BÀI SỐ XX:`.
- Mục lục: `README.md`.
- Nội dung bài số `N`: `N/content.md`.
- Ảnh: thư mục `images`, đặt tên theo thứ tự `BaiN-anh1.jpg`, `BaiN-anh2.jpg`, ...

## Quy tắc làm việc bắt buộc

1. Chỉ được mở thêm tối đa **một tab Chrome** ngoài tab Facebook hiện có.
2. Xử lý tuần tự từng bài, không mở hoặc đọc nhiều bài cùng lúc.
3. Quy trình của mỗi bài phải hoàn tất theo thứ tự:
   - Mở bài viết.
   - Mở rộng toàn bộ nội dung nếu có nút `See more`.
   - Đọc và kiểm tra nội dung.
   - Tải ảnh theo đúng thứ tự.
   - Ghi `N/content.md`.
   - Cập nhật `README.md`.
   - Kiểm tra các liên kết và tệp ảnh.
   - Sau đó mới chuyển sang bài tiếp theo trong cùng tab.
4. Không giữ nội dung của nhiều bài trong bộ nhớ rồi mới ghi hàng loạt.
5. Nếu Facebook chỉ trả nội dung rút gọn, không thấy toàn bài, hoặc không xác định chắc chắn ranh giới bài viết thì không tạo nội dung giả hay chép phần thiếu. Ghi số bài đó vào danh sách cần bổ sung thủ công và chuyển sang bài tiếp theo.

## Cách tạo tệp nội dung

Đầu và cuối mỗi `content.md` đều phải có:

```md
[Mục lục](../README.md)
```

Liên kết đầu tệp nằm trước tiêu đề; liên kết cuối tệp nằm sau đoạn nội dung chính cuối cùng. Sau liên kết đầu tệp là tiêu đề đầy đủ của bài và toàn bộ nội dung chính. Giữ nguyên câu chữ, thứ tự các đoạn và ký hiệu liệt kê của tác giả; chỉ chuẩn hóa Markdown khi cần để dễ đọc.

Không sao chép phần kêu gọi tương tác ở cuối bài, thường bắt đầu bằng một đường phân cách rồi đến `P/S`, ví dụ nội dung đề nghị bình luận, chia sẻ hoặc giải thích “pháp thí”.

Chèn ảnh theo đúng thứ tự bằng đường dẫn tương đối:

```md
![Bài N - ảnh 1](../images/BaiN-anh1.jpg)
```

Khi tải ảnh qua URL `lookaside.fbsbx.com`, phải dùng User-Agent dạng crawler như `facebookexternalhit/1.1`; nếu không, Facebook có thể trả về một trang HTML chuyển hướng nhưng vẫn được lưu với đuôi `.jpg`. Sau khi tải, kiểm tra tệp là JPEG thật (hai byte đầu là `FF D8`) và có kích thước hợp lý. Không chèn tệp HTML giả ảnh vào Markdown.

## Cập nhật mục lục

Thêm một dòng vào `README.md`, sắp xếp tăng dần theo số bài:

```md
- [N: TÊN BÀI VIẾT](N/content.md)
```

Không thêm bài vào mục lục nếu chưa có `N/content.md` hoàn chỉnh.

## Kiểm tra trước khi kết thúc

- Mỗi bài đã ghi có liên kết `[Mục lục](../README.md)` ở cả đầu và cuối tệp.
- Không còn phần `P/S` hoặc lời kêu gọi chia sẻ đã được yêu cầu loại bỏ.
- Mọi ảnh được tham chiếu đều tồn tại và có đúng tên.
- Mọi liên kết trong `README.md` đều trỏ đến tệp tồn tại.
- Tệp dùng UTF-8 và hiển thị đúng tiếng Việt.
- Không ghi đè thay đổi không liên quan của người dùng.
- Không commit hoặc push Git nếu người dùng chưa yêu cầu.
- Báo rõ danh sách bài hoàn thành và danh sách bài cần người dùng tìm thủ công.
