# Hướng dẫn lấy supabaseUrl và supabaseAnonKey cho test-auth.html

Để sử dụng file `test-auth.html` với Supabase, bạn cần lấy thông tin `supabaseUrl` và `supabaseAnonKey` từ dự án Supabase của bạn.

## Các bước thực hiện

1. **Đăng nhập vào Supabase**

   - Truy cập [https://app.supabase.com/](https://app.supabase.com/) và đăng nhập tài khoản của bạn.

2. **Chọn Project**

   - Chọn project bạn muốn sử dụng.

3. **Lấy supabaseUrl**

   - Sau khi vào project, bạn sẽ thấy URL trên thanh địa chỉ trình duyệt, ví dụ: `https://abcxyz.supabase.co`.
   - Hoặc Ở Project Overview, kéo xuống sẽ thấy phần: Connecting to your new project
   - Sao chép giá trị **Project URL** (ví dụ: `https://abcxyz.supabase.co`).

4. **Lấy supabaseAnonKey**

   - Trong cùng mục **Project Settings**, kéo xuống phần **Project API keys**.
   - Sao chép giá trị **anon public** key.

5. **Gắn vào file test-auth.html**

   - Mở file `test-auth.html`.
   - Tìm đoạn:
     ```js
     const supabaseUrl = "https://.supabase.co";
     const supabaseAnonKey = "..-";
     ```
   - Thay bằng thông tin bạn vừa lấy được:
     ```js
     const supabaseUrl = "https://abcxyz.supabase.co";
     const supabaseAnonKey = "eyJ...";
     ```

6. **Lưu file và sử dụng**
   - Lưu lại file và mở bằng trình duyệt để sử dụng chức năng đăng ký/đăng nhập.

---

**Lưu ý:** Không chia sẻ `supabaseAnonKey` công khai nếu không cần thiết. Đây là key public nhưng vẫn nên bảo mật.
