# Giới thiệu

[Xem trên YouTube](https://www.youtube.com/watch?v=7wuKDDMb3R4)

Python là một ngôn ngữ nguồn mở, đa nền tảng và thông dịch. Bởi vì nó là ngôn ngữ nguồn mở, nên bạn có thể sử dụng ngôn ngữ này trong bất kỳ phần mềm thương mại nào, và bởi vì nó đa nền tảng nên bạn có thể viết các chương trình chạy trên Mac và nó cũng sẽ chạy chính xác trên các nền tảng khác hỗ trợ Python.

Python ra đời đã hơn 30 năm và đó là lý do mà nó có sẵn rất nhiều các gói hỗ trợ của bên thứ 3. Nó cũng khuyến khích kiểm tra tại http://pypi.python.org trước khi bắt đầu viết gói của riêng bạn, bởi vì có thể đã có một ai đó viết một gói tương tự. Có hàng triệu lập trình viên Python trên đây, và python có thể làm hầu như bất cứ điều gì, Youtube, Quora, Hulu chỉ là vài nền tảng viết bằng Python. Với Python chúng ta có thể viết ứng dụng command-line, linux bootloader, tới các ứng dụng web, ứng dụng frontend và tất cả mọi thứ mà bạ muốn

Python là một ngôn ngữ kiểu động, điều đó nghĩa là bạn không phải định nghĩa kiểu dữ liệu của một đối tượng. Nó là một ngôn ngữ hướng đối tượng hoàn toàn. Bởi vì nó có cú pháp tương tự tiếng Anh, Python tạo ra một ngôn ngữ mẫu tuyệt vời, bất kỳ chương trình gì được phát triển bằng Python có số dòng ít hơn đáng kể so với Java, nhưng bởi vì nó là ngôn ngữ kiểu động nên việc gỡ lỗi (debug) trong chương trình viết bằng Python sẽ hơi khó hoặc chúng ta sẽ phải cẩn thận trong quá trình viết. Lí do cho điều đó là nếu bạn có một chương trình có 100 dòng, và bạn định nghĩa `i=1` tại dòng đầu tiên, nhưng sau đó bạn nhầm lẫn khi khai báo `i = '1'` ở một nơi nào đó giữa các dòng, nó sẽ không phàn nàn `i là một số nguyên và bạn không thể gán một chuỗi cho nó`, nó sẽ chỉ chạy phần còn lại của chương trình với giá trị mới của i.

Cũng vì điều này mà nó làm cho Python trở nên mạnh mẽ với sự hiện diện của các cấu trúc dữ liệu cấp cao như hashmaps, sets và lists.

## Python 2 với Python3

Python3 là sự kế thừa của Python2. Tới 2020 Python2 sẽ trở thành lịch sử. Hướng dẫn này dựa trên Python3 vì nó là hiện tại và tương lai của ngôn ngữ này. Lý do tại sao họ tạo ra python3 là đã có một vài thiếu sót trong ngôn ngữ python mà không được đề cập trong suốt 30 năm và bây giờ, các tác giả của python đã quyết định họ nên giải quyết chúng, trong khi giải quyết các vấn đề đó, nó sẽ phải tương thích ngược với ngôn ngữ và python3 được tạo ra. Nếu bạn viết một chương trình trong Python3, không có gì đảm bảo nó sẽ chạy trong Python2 và ngược lại, nếu bạn muốn chương trình của bạn làm việc trên cả Python2 và Python3 bạn sẽ phải viết nó một cách đặc biệt để chạy cả 2 phiên bản. Nó không thuộc phạm vi của hướng dẫn này, nhưng bạn sẽ tìm được nhiều nguồn tài liệu trên Internet dạy bạn làm cách nào để viết chương trình tương thích với cả hai phiên bản.

## Cài đặt

Nếu bạn dùng Windows, vui lòng truy cập https://python.org và download phiên bản .ext mới nhất của Python3. Với Android, vui lòng download TermUX (https://termux.com/help.html). Nếu bạn dùng Mac (brew install python3), nếu bạn dùng Linux thì tùy thuộc vào bản phân phối của bạn (apt-get install python3 or yum install python3)

Lý thuyết đã đủ, bây giờ bắt đầu với các ví dụ.

Bắt đầu viết một chương trình. Đảm bảo rằng bạn đã cài đặt Python.

## Ví dụ: Liệt kê tất cả các tập tin `*.txt`
Chúng ta sẽ in một danh sách của tất cả các tập tin kết thúc với '.txt'.

#### Lưu ý:

Python không sử dụng dấu chấm phẩi hoặc ngoặc nhọn để điều khiển luồng chương trình, nó sử dụng **thụt đầu dòng**. Bạn bắt buộc phảu sử dụng thụt đầu dòng nếu bạn sử dụng `for`, `while`, `if`.

```python
import os

files = os.listdir()
for file in files:
    if file.endswith(".txt"):
        print(file)
```

Lưu đoạn mã trên vào `file.py`. Tạo 2-3 tập tin .txt. `touch file{1,2,3,4,5}.txt` sẽ tạo các tập tin tên file1.txt, file2.txt till file5.txt, nhưng chỉ làm việc trên Linux hoặc Mac.

Sau khi lưu tập tin `file.py`, thực thi chương trình bằng lệnh `python3 file.py`

###### Lưu ý:
Nếu bạn nhận được một lỗi là không tìm thấy python3, gõ `python --version`, nếu nó là 3 hoặc cao hơn bạn chỉ cần gõ `python file.py`, bởi vì trong trường hợp này, bạn đã cài đặt Python3 và gọi python sẽ là gọi python3.

Nếu mọi thứ đều ổn bạn sẽ thấy các đầu ra như sau:

```
file1.txt
file2.txt
file3.txt
file4.txt
file5.txt
```

Đây là một ngôn ngữ đẹp, cú pháp của nó rất dễ hiểu và đó là lí do tại sao nó hết sức mạnh mẽ.

Nếu bạn muốn liệt kê tất cả các tập tin .txt, bạn có thể sử dụng các công cụ trên hệ thống unix như `ls`, `ls *.txt`. Như ở đây, chúng ta thực hiện một tính năng của lệnh `ls` với ít hơn 5 dòng mã. Đây chính là sức mạnh của Python.

## Sử dụng glob
Có một mô-đun stdlib cho phép chúng ta có những tính năng nâng cao như không cần phải kiểm tra phần mở rộng của tập tin nữa.

```python
>>> import glob
>>> files = glob.glob('*.txt')
>>> files
['file1.txt', 'file2.txt', 'file3.txt', 'file4.txt', 'file5.txt']
 ```

Phương thức `glob` là một biểu thức chính quy trên các thư mục hiện hành.

Khi bạn đã có nhiều kiến thức trong Python, bạn sẽ cảm thấy cần sử dụng nhiều các chức nặng stdlib để giảm sự trùng lặp mã.

Bài tập:

1. Viết một chương trình in ra tất cả các tập tin `*.csv`, tạo các tập tin `.csv` trước và không sử dụng glob.
1. Cài đặt ipython sử dụng easy_install hoặc pip. Lưu ý về version của pip mà bạn sử dụng.

##### Links

|[Next](02-more-about-language.md) | [Previous](README.md) |  [Index](SUMMARY.md)
| ---- | ---- | ---- |
