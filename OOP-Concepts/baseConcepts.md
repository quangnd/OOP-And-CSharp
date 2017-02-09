# OOP Concepts

## Câu hỏi

1. Lập trình hướng đối tượng (OOP) có những tính chất đặc thù gì? Nêu chi tiết.
2. Viết chương trình minh hoạ cho các tính chất trên.

## Giải quyết

1. OOP có 04 tính chất đặc thù
    * **Tính đóng gói (Encapsulation)**:
    
         Có thể gói dữ liệu (data, ~ biến, trạng thái) và mã chương trình (code, ~ phương thức) thành một cục gọi là lớp (class) để dễ quản lí. Trong cục này thường data rất rối rắm, không tiện cho người không có trách nhiệm truy cập trực tiếp, nên thường ta sẽ che dấu data đi, chỉ để lòi phương thức ra ngoài. Ví dụ hàng xóm sang mượn búa, thay vì bảo hàng xóm cứ tự nhiên vào lục lọi, ta sẽ bảo: "Ấy bác ngồi chơi để tôi bảo cháu lấy cho". Ngôn ngữ Ruby "phát xít" đến nỗi dấu tiệt data, cấm không cho truy cập từ bên ngoài. Ngoài ra, các lớp liên quan đến nhau có thể được gom chung lại thành package (tùy ngôn ngữ mà còn gọi là module, namespace v.v.).

    * **Tính trừu tượng (Abstraction)**
         
         Có câu "program to interfaces, not to concrete implementations". Nghĩa là khi viết chương trình theo phong cách hướng đối tượng, khi thiết kế các đối tượng, ta cần rút tỉa ra những đặc trưng của chúng, rồi trừu tượng hóa thành các interface, và thiết kế xem chúng sẽ tương tác với nhau như thế nào. Nói cách khác, chúng ta định ra các interface và các contract mà chúng cần thỏa mãn.

    * **Tính thừa kế (Inheritance)**
         
         Lớp cha có thể chia sẻ dữ liệu và phương thức cho các lớp con, các lớp con khỏi phải định nghĩa lại những logic chung, giúp chương trình ngắn gọn. Nếu lớp cha là interface, thì lớp con sẽ di truyền những contract trừu tượng từ lớp cha.

    * **Tính đa hình (Polymorphism)**

         Đối tượng có thể thay đổi kiểu (biến hình). (1) Với các ngôn ngữ OOP có kiểu, có thể mượn phát biểu của C++ "con trỏ kiểu lớp cha có thể dùng để trỏ đến đối tượng kiểu lớp con". Như vậy khi khai báo chỉ cần khai báo p có kiểu lớp cha, còn sau đó nó trỏ đến đâu thì kệ cha con nó: nếu cha và con cùng có phương thức m, thì từ p cứ lôi m ra gọi thì chắc chắn gọi được, không cần biết hiện tại p đang trỏ đến cha hay con. Khi lớp B thừa kế từ lớp A, thì đối tượng của lớp B có thể coi là đối tượng của lớp A, vì B chứa nhiều thứ thừa kế từ A. (2) Với ngôn ngữ OOP không có kiểu như Ruby, có thể mượn phát biểu của phương pháp xác định kiểu kiểu con vịt: "nếu p đi như vịt nói như vịt, thì cứ coi nó là vịt". Như vậy nếu lớp C có phương thức m, mà có thể gọi phương thức m từ đối tượng p bất kì nào đó, thì cứ coi p có kiểu là C.

2. Chương trình chứng minh

    * Tạo interface Animal có phương thức say_hello. <- Thể hiện tính trừu tượng, có nghĩa ta định ra contract là rằng dù là con vật gì đi nữa thì nó cũng có phương thức say_hello để chào hỏi gì đấy.
    * Tạo 2 lớp Cat và Dog kế thừa từ Animal. Khi khởi tạo chúng sẽ có tên. Chúng override lại phương thức say_hello để chào hỏi theo cách riêng của chúng. <- Thể hiện tính đóng gói (đóng gói biến tên và phương thức say_hello với nhau) và tính thừa kế (Cat và Dog mang đặc điểm chung là có say_hello từ Animal).
    * Tạo lớp Zoo để quản lí nhiều Animal, có (1) phương thức add, remove để thêm, bớt các Animal (các đối tượng của các lớp thừa kế từ Animal), (2) phương thức say_hello_all để gọi say_hello của tất cả đối tượng nó quản lí. <- Thể hiện tính đa hình, Zoo gọi chỉ gọi một phương thức say_hello, nhưng tùy con vật mà lời chào hỏi sẽ khác nhau.

## References

1. https://kipalog.com/posts/4-tinh-chat-dac-thu-cua-lap-trinh-huong-doi-tuong
2. https://chesterli0130.wordpress.com/2012/10/04/four-major-principles-of-object-oriented-programming-oop/