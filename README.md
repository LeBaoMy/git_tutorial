# git_tutorial

### giới thiệu git 
   
Git là một bộ công cụ quản lý phiên bản đặc biệt, được tạo ra bởi Linus Torvalds vào năm 2005 để giải quyết những thách thức quản lý mã nguồn trong dự án phần mềm Linux. Từ đó, Git đã trở thành một công cụ phổ biến trong cộng đồng phát triển phần mềm, không chỉ vì tính linh hoạt và hiệu suất cao mà còn vì cơ chế nhánh linh hoạt và hỗ trợ mạnh mẽ từ cộng đồng.

Điểm đặc biệt của Git là cấu trúc phân tán, cho phép mỗi máy tính có thể lưu trữ một bản sao đầy đủ của toàn bộ dự án. Điều này giúp tăng tính linh hoạt và giảm thiểu sự phụ thuộc vào máy chủ trung tâm. Hơn nữa, cơ chế nhánh của Git cho phép phát triển song song các tính năng mới hoặc sửa lỗi mà không làm ảnh hưởng đến phiên bản chính của dự án.

Với một cộng đồng lớn và sôi động, cùng với các dịch vụ như GitHub, GitLab và Bitbucket, Git đã trở thành một phần không thể thiếu trong quy trình phát triển phần mềm hiện đại. Sự linh hoạt, hiệu suất và sự hỗ trợ mạnh mẽ từ cộng đồng đã làm cho Git trở thành công cụ quản lý phiên bản hàng đầu được ưa chuộng bởi các nhà phát triển trên khắp thế giới.

### Kiến trúc của git

- Workspace (Thư mục làm việc)
Đây là bản sao làm việc của tệp. Trạng thái vật lý của tệp mà bạn có thể xem và sửa đổi. Bạn có thể tự do thêm, sửa, bớt bất cứ điều gì bạn muốn. Git sẽ không theo dõi bất kỳ thay đổi nào bạn đang thực hiện khi tệp nằm trong phần này.

- Staging
 Khi bạn cảm thấy mình đã hoàn thành một phần logic của nhiệm vụ bạn đang thực hiện, bạn có thể thêm trạng thái này của tệp ( với những thay đổi này) vào phần Staging. Điều này sẽ tạo một phiên bản tạm thời (được gọi là chỉ mục dàn dựng) của tệp.

- Local Repository
Bạn có thể di chuyển tất cả các thay đổi theo giai đoạn của tệp này sang kho lưu trữ cục bộ. Điều này thường được thực hiện khi tệp đạt đến trạng thái gắn kết hoàn chỉnh (như hoàn thành một phần logic của một tính năng hoặc một hotfix). Bạn sẽ phải thực hiện những thay đổi này để tạo phiên bản vĩnh viễn của tệp trong kho lưu trữ cục bộ. Phiên bản này sẽ có tất cả thông tin chi tiết (như tên của người thực hiện thay đổi, ngày cam kết, hàm băm mật mã của tệp đóng vai trò là id xác nhận và thông báo cam kết). Lịch sử dàn dựng của tệp này (tất cả các phiên bản tạm thời) sẽ bị xóa khi một cam kết xảy ra.

- Remote Repository
Nếu bạn đang làm việc một mình trong một dự án, bạn có thể đạt được khả năng kiểm soát phiên bản đầy đủ với ba bước đầu tiên. Nhưng nếu bạn đang làm việc trong môi trường cộng tác giữa nhiều người và nhiều nhóm thì bạn sẽ cần phải đồng bộ hóa các thay đổi với kho lưu trữ từ xa để mọi người có quyền truy cập vào các thay đổi mã mới nhất. ( đó là nơi Github xuất hiện ).

### Các thuật ngữ

1. Repository (Kho chứa):
Kho chứa dữ liệu của dự án, bao gồm lịch sử thay đổi, các nhánh, và các tệp tin.

2. Commit (Bản ghi):
Một bản sao của repository tại một thời điểm cụ thể, đại diện cho một tập hợp các thay đổi.

3. Branch (Nhánh):
Một nhánh độc lập của repository, cho phép phát triển song song của mã nguồn.

4. Merge (Hợp nhất):
Quá trình kết hợp các thay đổi từ một nhánh vào nhánh khác.

5. Pull Request (PR):
Yêu cầu hợp nhất các thay đổi từ một nhánh vào nhánh khác, thường được sử dụng trong quá trình làm việc nhóm.

6. Fork:
Tạo một bản sao độc lập của một repository, thường được sử dụng để đóng góp vào dự án mã nguồn mở.

7. Clone:
Sao chép một remote repository vào local repository.

8. Push:
Đẩy các commit từ local repository lên remote repository.

9. Pull:
Lấy các thay đổi từ remote repository và cập nhật vào local repository.

10. Checkout:
Chuyển đổi giữa các nhánh hoặc khôi phục các thay đổi từ một commit cụ thể.

11. Conflict (Xung đột):
Xảy ra khi có sự không phù hợp giữa hai phiên bản của cùng một tệp hoặc dòng mã.

12. Tag:
Một thẻ dán một điểm cụ thể trong lịch sử của repository, thường được sử dụng để đánh dấu các bản phát hành.

13. Staging Area (Khu vực đặt sẵn):
Khu vực tạm thời nơi các thay đổi được chuẩn bị trước khi được commit vào repository.

14. Working Directory (Thư mục làm việc):
Thư mục trên máy tính của bạn mà bạn thực hiện các thay đổi và làm việc với các tệp.

15. SHA (Secure Hash Algorithm):
Mã băm duy nhất được sử dụng để định danh các commit và các đối tượng khác trong Git.

16. HEAD:
Tham chiếu đến commit hiện tại hoặc vị trí hiện tại trong repository.

17. Remote:
Một remote repository được đặt tên, thường là trên một máy chủ từ xa.

18. Gitignore:
Một tệp tin chứa danh sách các tệp và thư mục mà Git sẽ bỏ qua trong quá trình theo dõi thay đổi.

### các lệnh cơ bản trong git
   
- git init:
Khởi tạo một repository Git mới trong thư mục làm việc hiện tại.

- git clone <url_repository>:
Sao chép một remote repository vào local repository.

- git add <file_name>:
Thêm tệp vào staging area để chuẩn bị cho commit.

- git commit -m "Commit message":
Tạo một commit từ các thay đổi đã được thêm vào staging area.

- git status:
Hiển thị trạng thái hiện tại của working directory và staging area.

- git push <remote_name> <branch_name>:
Đẩy các commit từ local repository lên remote repository.

- git pull <remote_name> <branch_name>:
Lấy và hợp nhất các thay đổi từ remote repository vào local repository.

- git branch:
Liệt kê tất cả các nhánh trong repository.

- git checkout <branch_name>:
Chuyển đổi sang một nhánh khác.

- git merge <branch_name>:
Hợp nhất các thay đổi từ một nhánh vào nhánh hiện tại.

- git log:
Hiển thị lịch sử commit của repository.

- git remote -v:
Hiển thị các remote repository được liên kết với repository local.

- git fetch <remote_name>:
Lấy các thay đổi từ remote repository mà không hợp nhất vào local repository.

- git rm <file_name>:
Xóa một tệp từ repository.

- git mv <old_file_name> <new_file_name>:
Di chuyển hoặc đổi tên một tệp trong repository.

- git reset HEAD <file_name>:
Loại bỏ một tệp từ staging area.

- git diff:
Hiển thị các thay đổi giữa working directory và staging area.

- git config:
Cấu hình Git, bao gồm thiết lập tên và email người dùng.

4. DEMO
