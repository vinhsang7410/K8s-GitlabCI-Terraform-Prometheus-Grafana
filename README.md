<h1>1. Tổng quan về Gcloud.</h1>
Google Cloud platform là gì? Đây là từ được viết tắt GCP hay còn gọi Google Cloud Platform. Đây chính là một nền tảng của điện toán đám mây cho phép các cá nhân hay tổ chức  xây dựng và phát triển các các ứng dụng của mình trên hệ thống phần mềm do google tạo ra. Các ứng dụng phổ biến như trình duyệt Chrome, ứng dụng bản đồ Google Map,…
<h3>Các dịch vụ của Google Cloud Platform</h3>
<b>IOT (Internet of Things):</b> cho phép người sử dụng quản lý và tiêu thụ dữ liệu từ những thiết bị IOT một cách thuận lợi.</br>
<b>Cloud Machine Learning Engine (Tìm kiếm đám mây):</b> dùng để phát triển ứng dụng trí tuệ nhân tạo (hay còn gọi là AI)</br>
<b>Google Cloud:</b> Cung cấp các dịch vụ như Hadoop và Apache Spark bao gồm Google Cloud Dataproc để dữ liệu được xử lý dễ dàng hơn và nhanh hơn.</br>
<b>Google Cloud Dataflow:</b> Dịch vụ xử lý dữ liệu cho những công việc phân tích, phục vụ cho các dự án tính toán theo thời gian thực tế, trích xuất, chuyển đổi và tải (ETL).</br>
<b>Google BigQuery:</b> nơi cung cấp tài nguyên khổng lồ của Google , bao gồm những dịch vụ xử lý dữ liệu và phân tích. Google BigQuery có chức năng để truy vấn tương tự công cụ SQL truyền thống được thực hiện đối với bộ dữ liệu nhiều terabyte. Tuy nhiên, trên thực tế việc lưu trữ những dữ liệu vô cùng cần thiết và quan trọng.
Dữ liệu không những dừng lại ở những file có kích thước nhỏ mà còn có thể lên đến terabyte.</br>
<h3>Tại sao nên sử dụng Google Cloud platform?</h3>
Hầu hết các doanh nghiệp khi xây dựng các ứng dụng đều phải chú ý đến tốc độ, khả năng nâng cấp, bảo trì và đặt biệt là tính bảo mật của hệ thống dữ liệu. Để đảm bảo được các vấn đề này doanh nghiệp thường phải tiêu tốn khoản chi phí đầu tư đáng kể vào việc mua phần cứng và nhân sự để xây dựng và quản lý hệ thống.</br>
Đó là chưa kể đến trang thiết bị sau một thời gian sẽ trở nên lỗi thời dẫn đến việc nâng cấp đòi hỏi số tiền lớn và các ứng dụng không còn mang lại trải nghiệm tốt cho khách hàng sử dụng dịch vụ hay hệ thống của doanh nghiệp, những vấn đề này sẽ được giải quyết khi doanh nghiệp chuyển đổi lên nền tảng Google Cloud. </br>
<h1>2. Kubernetes trên gcloud.</h1>
<p>Kubernetes là một nền tảng nguồn mở, khả chuyển, có thể mở rộng để quản lý các ứng dụng được đóng gói và các service, giúp thuận lợi trong việc cấu hình và tự động hóa việc triển khai ứng dụng. Kubernetes là một hệ sinh thái lớn và phát triển nhanh chóng. Các dịch vụ, sự hỗ trợ và công cụ có sẵn rộng rãi.
Tên gọi Kubernetes có nguồn gốc từ tiếng Hy Lạp, có ý nghĩa là người lái tàu hoặc hoa tiêu. Google mở mã nguồn Kubernetes từ năm 2014. Kubernetes xây dựng dựa trên một thập kỷ rưỡi kinh nghiệm mà Google có được với việc vận hành một khối lượng lớn workload trong thực tế, kết hợp với các ý tưởng và thực tiễn tốt nhất từ cộng đồng.</p>
<h3>Chức năng chính của Kubernetes</h3>
<b>Service discovery và cân bằng tải:</b> Kubernetes có thể expose một container sử dụng DNS hoặc địa chỉ IP của riêng nó. Nếu lượng traffic truy cập đến một container cao, Kubernetes có thể cân bằng tải và phân phối lưu lượng mạng (network traffic) để việc triển khai được ổn định.</br>
<b>Điều phối bộ nhớ:</b> Kubernetes cho phép bạn tự động mount một hệ thống lưu trữ mà bạn chọn, như local storages, public cloud providers, v.v.</br>
<b>Tự động rollouts và rollbacks:</b> Bạn có thể mô tả trạng thái mong muốn cho các container được triển khai dùng Kubernetes và nó có thể thay đổi trạng thái thực tế sang trạng thái mong muốn với tần suất được kiểm soát. Ví dụ, bạn có thể tự động hoá Kubernetes để tạo mới các container cho việc triển khai của bạn, xoá các container hiện có và áp dụng tất cả các resource của chúng vào container mới.</br>
<b>Đóng gói tự động:</b> Bạn cung cấp cho Kubernetes một cluster gồm các node mà nó có thể sử dụng để chạy các tác vụ được đóng gói (containerized task). Bạn cho Kubernetes biết mỗi container cần bao nhiêu CPU và bộ nhớ (RAM). Kubernetes có thể điều phối các container đến các node để tận dụng tốt nhất các resource của bạn.</br>
<b>Tự phục hồi:</b> Kubernetes khởi động lại các containers bị lỗi, thay thế các container, xoá các container không phản hồi lại cấu hình health check do người dùng xác định và không cho các client biết đến chúng cho đến khi chúng sẵn sàng hoạt động.</br>
<b>Quản lý cấu hình và bảo mật:</b> Kubernetes cho phép bạn lưu trữ và quản lý các thông tin nhạy cảm như: password, OAuth token và SSH key. Bạn có thể triển khai và cập nhật lại secret và cấu hình ứng dụng mà không cần build lại các container image và không để lộ secret trong cấu hình stack của bạn.</br>
<h1>3. Gitlab là gì và tầm quan trọng của Gitlab-ci</h1>
<p>GitLab là một nền tảng DevOps toàn diện được sử dụng để quản lý mã nguồn và quy trình phát triển phần mềm. Nền tảng này cung cấp một môi trường tích hợp để quản lý mã nguồn, kiểm tra mã, quản lý vấn đề, triển khai tự động và theo dõi quy trình phát triển phần mềm.</p>
<h3>Các phiên bản</h3>
<ul>
<li>Gitlab Community Edition (CE): Phiên bản cộng đồng, mã nguồn mở. Đây là bản mới nhất, được nhà phát triển release từ các nhánh stable và nhánh master.</li>
<li>GitLab Enterprise Edition (EE): Phiên bản sử dụng cho các đối tượng là doanh nghiệp. Công cụ được cung cấp từ kho lưu trữ của gitlab.com. Ngay khi đăng ký, bạn sẽ nhận được hỗ trợ của GitLab BV. Vấn đề liên quan đến cài đặt và sử dụng đều được xử lý nhanh chóng.</li>
<li>Gitlab Continuous Integration (CI): Một giải pháp tích hợp, được thực hiện bởi nhóm phát triển GitLab.</li>
</ul>
<p>Mỗi loại sẽ đem đến những hỗ trợ khác nhau cho người dùng. Nhờ có sự nâng cấp liên tục nên luôn đảm bảo trải nghiệm hoàn hảo nhất.</p>
<h3>Protected Branches</h3>
<p>Tính năng Protected Branches trong GitLab cho phép giới hạn quyền truy cập vào Repository và các Branches, ngăn chặn việc push code từ những đối tượng không được cấp quyền và ngăn chặn hành động xóa Branch. Master Branch là Protected Branch mặc định và user cần được cấp ít nhất một quyền từ Master để bảo mật nhánh.</p>
![image](https://github.com/user-attachments/assets/bb238eb3-89a8-4d85-a6c7-035b90122acf)
<h3>System Layout</h3>
<p>GitLab là một ứng dụng được viết bằng Ruby on Rails. Vì vậy, để hiểu rõ hoạt động của nó, ta cần hiểu phương thức vận hành của ngôn ngữ lập trình này. Ruby on Rails là ngôn ngữ lập trình được sử dụng cho GitLab. Khi cài đặt GitLab-Shell, công cụ sẽ được đặt trong thư mục /home/git/gitlab-shell và người dùng có thể sử dụng kho dữ liệu thông qua SSH.</p>
<h3>Tầng vật lý</h3>
<p>Tầng vật lý bao gồm kho lưu trữ, Nginx, cơ sở dữ liệu và GitLab-Shell. Các thành phần này hoạt động như một cỗ máy trong quá trình khai thác.</p>
