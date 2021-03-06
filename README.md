# int3120_20_homeworks

## Quá trình
### Tuần 1:
- Lesson 1: Tham khảo thông tin cơ bản về Flutter (Giới thiệu, tính năng, điểm mạnh,...)
- Lesson 2: Cài đặt, thiết lập môi trường phát triển
![img.png](imgs/flutter-doctor.png)
- Lesson 3: Hello World
![img.png](imgs/hello-world.png)
- Lesson 4: Tìm hiểu về kiến trúc ứng dụng Flutter
  - 1 ứng dụng Flutter là tập hợp các widget, tất cả đều quy về các widget, các widget có thể gói trong các widget khác để mở rộng chức năng. Các widget này hoạt động ở những layer phía trên và sẽ phụ thuộc vào các layer phía dưới để tương tác với hệ điều hành
  - Có cả những widget đặc biệt để quản lí State (Stateful widget), bắt sự kiện cử chỉ (GestureDetector widget)
- Lesson 5: Tìm hiểu về Dart
  - Ngôn ngữ mã nguồn mở, đa năng, được phát triển bởi Google
  - Hướng đối tượng (hỗ trợ class, interface,...), cú pháp C (C-style)
  - Hỗ trợ các kiểu dữ liệu tường minh (Integer, Double, String, Boolean, List, Map) và cả kiểu dữ liệu động (chưa được định nghĩa tường minh) (dynamic)
  - Hỗ trợ các khối lệnh điều khiển thông dụng (if, if...else, switch) cũng như các vòng lặp thông dụng (for, while, do...while)
- Lesson 6: Widget trong Flutter
  - Widget trong Flutter được chia thành 4 nhóm
    - Platform widgets: Các widget đặc thù theo nền tảng. Được thế kế theo các triết lý khác nhau, Material widgets thiết kế theo Material design guideline và Cupertino widgets được thiết kế theo Human Interface Guidelines
    - Layout widgets: Các widget dùng để bố trí giao diện
    - State maintenance widgets: Các widget quản lý state
    - Platform independent / basic widgets: Các widget cơ bản độc lập với nền tảng sử dụng
  - Ứng dụng sử dụng một số widget cơ bản: 
    - Material widgets: Scaffold, AppBar
    - Platform independent widget: Text, Image, Icon
    - Layout widget: Center, Column, Row, Padding
  ![img.png](imgs/lesson6.png)
- Lesson 7: Layout trong Flutter
  - Chia làm 2 loại chính dựa trên số widget con
    - Single Child Widgets - Chỉ có một widget con
    - Multiple Child Widgets - Có nhiều widget con
  - Ứng dụng sử dụng một số widget như: Scaffold, AppBar, Text, Padding, ListView, ListTile, Container, BoxDecoration, DecorationImage, AssetImage
  ![img.png](imgs/lesson7.png)
- Lesson 8: Gesture trong Flutter
  - Một số cử chỉ phổ biến như: Tap, Double Tap, Drag, Flick, Pinch, Spread, Panning
  - Flutter cung cấp widget GestureDetector hỗ trợ xử lý các sự kiện dễ dàng
  - Ngoài ra, Flutter cũng cung cấp cơ chế xử lý sự kiện ở cấp thấp sử dụng Listener widget
  - Ứng dụng áp dụng GestureDetector để xử lý sự kiện hiện dialog khi bấm vào ảnh
  ![img.png](imgs/lesson8.png)
- Lesson 9: Giới thiệu sơ bộ về quản lý State trong Flutter
  - Có thể chia làm 2 loại dựa trên thời gian tồn tại của state
    - Ephemeral (ngắn hạn): kéo dài trong thời gian ngắn, Flutter hỗ trợ quản lý state loại này thông qua StatefulWidget
    - App state (trạng thái ứng dụng): kéo dài trong toàn bộ app, Flutter hỗ trợ quản lý state loại này thông qua scoped_model
- Lesson 10: StatefulWidget trong Flutter
  - Widget được kế thừa từ StatefulWidget để duy trì trạng thái và quản lý các trạng thái của nó
  - Ứng dụng sử dụng StatefulWidget để làm RatingBox
  ![img.png](imgs/lesson10.png)
- Lesson 11: ScopedModel trong Flutter
  - Flutter có package scoped_model hỗ trợ việc quản lý trạng thái ứng dụng. Package này cung cấp 3 class chính
    - Model: Model đóng gói trạng thái của một ứng dụng. Model có một phương thức duy nhất là notifyListeners, notifyListeners sẽ thực hiện các công việc cần thiết để cập nhật giao diện.
    - ScopedModel: Đây là widget giúp chuyển Data Model từ widget cha xuống các widget con đồng thời rebuild các widget con giữ các model khi các model được cập nhật
    - ScopedModelDescendant: Đây là widget lấy Data model từ lớp cha và build UI khi Data model thay đổi
  - Ứng dụng sử dụng scoped_model để thay cho StatefulWidget
  ![img.png](imgs/lesson11.png)
- Lesson 12: Navigator và Routing
  - Flutter cung cấp cho chúng ta lớp routing cơ bản là MaterialPageRoute cùng với hai phương thức Navigator.push() và Navigator.pop()
    - MaterialPageRoute: Đây là widget dùng để render màn hình mới, có thể đi cùng với một hiệu ứng chuyển cảnh nào đó
    - Navigation.push(): Đây là phương thức dùng để chuyển sang màn hình mới
    - Navigation.pop(): Đây là phương thức dùng để quay lại màn hình trước đó
  - Ứng dụng áp dụng routing để chuyển sang màn hình chi tiết của Item khi bấm vào Item đó
  ![img.png](imgs/lesson12.png)