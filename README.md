#Github

## 1. Cách thức hoạt động của gitub
----
> Github là sự kết hợp giữa git - hệ thống quản lý dự án và phiên bản code và hub - mạng xã hội dành cho lập trình viên.

> - Git là hệ thống giúp mỗi máy tính có thể lưu trữ nhiều phiên bản khác nhau của một mã nguồn được nhân bản (clone) từ một kho chứa mã nguồn (repository), mỗi thay đổi vào mã nguồn trên máy tính sẽ có thể ủy thác (commit) rồi đưa lên máy chủ nơi đặt kho chứa chính. Và một máy tính khác (nếu họ có quyền truy cập) cũng có thể clone lại mã nguồn từ kho chứa hoặc clone lại một tập hợp các thay đổi mới nhất trên máy tính kia.

## 2. Các khái niệm
----
> Add

> - Lưu file thay đổi.

---
> Remove

> -  Để remove một thư mục hay một file nào đó có thể xóa ở máy local.

---
> Commit

> -  Dùng để ghi lại sự thay đổi file hay thư mục vào repository.

---
> Push

> -  Dùng để cập nhật thông tin trên máy local lên server.

---
> Pull

> -  Dùng để gộp những thay đổi mới kéo về từ máy chủ từ xa với nhánh hiện tại trên máy local.

---
> Fetch

> -  Dùng để truy cập vào một repository nào đó và cập nhật dữ liệu repository đó.

---
> Clone

> -  Dùng để sao chép remote repository.

---
> Fork

> -  Dùng để copy của một repository.

---
> Star

> -  Dùng để chỉ những repository được nhiều người quan tâm trên github.

---
> Star

> -  Dùng để nhận thông báo cho các yêu cầu mới hay vấn đề gì xảy ra với repository đó.

----

## 2. Các vấn đề khác

> Setting up git

* Tải và cài đặt git
    * `sudo apt-get install git-core`

* Set tên và email trong git
    * ` git config --global user.name "KaitoRyouga"`
    * `git config --global user.email "kaito1477800@gmail.com"`

---
> Generate and add SSH key

* Mở terminal và gõ câu lệnh
    * `ssh-keygen -t rsa -b 4096 -C "kaito1477800@gmail.com"`
    * `Enter file in which to save the key (/home/kaito/.ssh/id_rsa):` 
        * nhấn enter để cài đặt ở mặc định

    * `Enter passphrase (empty for no passphrase):`
        * Nhập password cho key

    * `Enter same passphrase again:`
        * Nhập lại password

    * `eval “$(ssh-agent -s)”`
        * Kích hoạt ssh-agent

    * `ssh–add ~/.ssh/id_rsa`
        * Add ssh key vào ssh-agent

    * `sudo apt-get install xclip`
        * cài xclip
    * `xclip -sel clip < ~/.ssh/id_rsa.pub`
        * Nội dung của id_rsa.pub sẽ lưu vào clipboard

* Vào github, vào setting, vào SSH and GPG keys, click vào new ssh key và paste

---
> Caching your GitHub password in Git
> - Dùng để cache username và password trong một khoảng thời gian nhất định.

* `git config --global credential.helper cache`
* `git config --global credential.helper 'cache --timeout=3600'`
   * set lại timeout nếu cần
