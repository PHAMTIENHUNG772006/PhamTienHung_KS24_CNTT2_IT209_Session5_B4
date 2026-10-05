\# Báo cáo Bài 4: Mô phỏng quy trình Hotfix \& Gitflow



\## 1. Sơ đồ phân nhánh Gitflow đã áp dụng

\- \*\*main\*\*: Nhánh lưu trữ phiên bản production ổn định.

\- \*\*develop\*\*: Nhánh chứa các tính năng đang phát triển cho tương lai.

\- \*\*hotfix/v1.0.1\*\*: Nhánh được tách ra trực tiếp từ `main` để sửa lỗi khẩn cấp (không ảnh hưởng đến tiến độ của `develop`).

\- \*\*Luồng xử lý\*\*: Sau khi sửa lỗi trên `hotfix/v1.0.1`, em đã gộp nhánh này vào `main` (kèm tag v1.0.1 để release) và đồng thời gộp ngược lại vào `develop` để đảm bảo lỗi này không bị lặp lại ở các phiên bản tương lai. Cuối cùng tiến hành xóa nhánh hotfix.



\## 2. Kết quả Log đồ thị các nhánh

\*   aa068f7 (HEAD -> develop) Merge branch 'hotfix/v1.0.1' into develop

|\\

| \* ef7fc42 (tag: v1.0.1, main, hotfix/v1.0.1) fix: va loi lo du lieu nguoi dung nghiem trong

\* | cdecb48  feat : dang code do tinh nang moi

|/

\* 1f85d9d (tag: v1.0.0)  release : phien ban v1.0.0 stable

