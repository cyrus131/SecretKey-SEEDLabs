# Secret-Key-Encryption-SEED-Labs

## Task 1. Phân tích tần suất
- Ở đây ta có một tập tin ciphertext.txt được tải trên website của Lab này. Nội dung của tập tin ciphertext.txt như sau:

    ![ảnh](https://user-images.githubusercontent.com/86979345/130312790-75716ef0-8ef3-4712-bbd5-e529235895a9.png)

- Ta thực hiện phân tích tần suất xuất hiện của các chữ cái trong bản mã trên dựa vào tần suất xuất hiện của cái chữ cái (so sánh tần suất 1,2,3 ký tự để đảm bảo độ chính xác cao) trong Tiếng Anh. 

    ![ảnh](https://user-images.githubusercontent.com/86979345/130312824-c2e2266e-db26-4b1d-ba50-72f42486a527.png)
    
    Tần suất xuất hiện phổ biến của các chữ cái trong Tiếng Anh
    
    
    ![ảnh](https://user-images.githubusercontent.com/86979345/130312840-a2c20c46-1af4-46f8-b867-75cb61c5c9ee.png)
    
    Tần suất xuất hiện của cặp 2 ký tự phổ biến Tiếng Anh
    
    ![ảnh](https://user-images.githubusercontent.com/86979345/130312855-f31b14f4-1015-4c9a-aab3-6b3e8e7e4cee.png)
    
    Tần suất xuất hiện của cặp 3 ký tự phổ biến trong Tiếng Anh
    
- Thông qua bản mã tải về ta phân tích được như sau:

    + Đối với 1 ký tự   
    
      | 1 | 2 | 3 | 4  | 5 |
      | ------------- |:-------------:|---------| ------------- | ------------- |
      |N = 488| Y = 373|V = 348|X = 291|U = 280|
      |Q = 276|M = 264 |H = 235|T = 183|I = 166|
      |P = 156|A = 116 |C = 104|Z = 95 |L = 90 |
      |B = 83 |G = 83  |R = 82 |E = 76 |D = 59 |
      |F = 49 |S = 19  |K = 5  |J = 5  |O = 4  |
      |W = 1  |

    + Đối với cặp 2 ký tự
    
       | 1 | 2 | 3 | 4  | 5 |
       | ------------- |:-------------:|---------| ------------- | ------------- |
       |YT = 53|TN = 44	|MU = 40|NH = 38|VU = 32|HN = 31|
       |NQ = 30|QY = 28	|NV = 25|VY = 25|XH = 25|YN = 25|
       |VH = 24|NP = 23 |XU = 22|VI = 21|UV = 21|NU = 20|
       |GN = 20|YX = 19	|VQ = 18|UP = 18|MY = 18|YM = 18|
       |TM = 16|QX = 15	|AV = 15|QN = 15|UY = 15|ZY = 14|
       |UQ = 14|NC = 14	|PY = 14|IN = 13|NA = 13|XZ = 13|
       |QV = 13|CX = 13	|UR = 13|HM = 12|HY = 12|	…|
    + Đối với cặp 3 ký tự
       | 1 | 2 | 3 | 4  | 5 |
       | ------------- |:-------------:|---------| ------------- | ------------- |
       |YTN = 29|VUP = 10|MUR = 8|PYT = 8|YNH = 7|
       |VYN = 7	|NQY = 7 |NUY = 6|XZY = 6|QXZ = 5|
       |QXZ = 5 |CMU = 5 |YXH = 5|NYT = 5|RTY = 5|
       |RTY = 5	|LVQ = 5 |NHQ = 5|YTV = 5| …|
       
- Ở đây ta viết một chương trình để thực hiện công việc này (hoặc ta có thể sử dụng công cụ online được đề cập trong Lab này) như sau:


    ![ảnh](https://user-images.githubusercontent.com/86979345/130313491-e30c31c6-2704-4804-b12d-41aa9007480e.png)


- Sau khi thực hiện đoạn code ta được kết quả như sau:

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313507-0b23c238-d68f-4719-ba58-0b02f4860512.png)

- Khi có được kết quả thay thế của các cặp từ thì ta sử dụng câu lệnh tr để tiến hành giải mã để thu được bản rõ ban đầu:

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313520-d2307739-37c9-4831-b714-00a1f857d2ab.png)


# Task 2. Mã hoá bằng các hệ mật mã với chế độ khác nhau
- Đầu tiên ta sẽ tiến hành tạo một file plaintext.txt với nội dung như sau:
    
    ![ảnh](https://user-images.githubusercontent.com/86979345/130313557-0102ec8f-3930-46c6-8c46-a7a44a2b2148.png)
    
- Thực hiện mã hoá với các chế độ lần lượt là –aes-128-cbc, -bf-cbc, -aes-128-cfb
   
   ![ảnh](https://user-images.githubusercontent.com/86979345/130313559-4918c006-84cc-4781-b6d0-6e2eb1c3a80a.png)

- Sau khi thực hiện mã hoá ta sẽ được các tập tin mã hoá như sau:
    
    ![ảnh](https://user-images.githubusercontent.com/86979345/130313568-691e3f80-a3c5-4fc3-bdb6-44515d713f48.png)

# Task 3. Chế độ mã hoá ECB với CBC
- Ở đây ta sẽ sử dụng hình ảnh pic_original.bmp được tải từ chính trang web của bài Lab này
  
    ![ảnh](https://user-images.githubusercontent.com/86979345/130313582-27faf949-eac8-4a00-a34e-773be7e357c3.png)
    
- Ta sẽ tiến hành thực hiện mã hoá hình ảnh này với các chế độ ECB và CBC
   
   ![ảnh](https://user-images.githubusercontent.com/86979345/130313592-d2c53f82-878b-4852-b31d-6714ab5320d6.png)

- Sau khi mã hoá ta sẽ được hai tập tin như sau:

   ![ảnh](https://user-images.githubusercontent.com/86979345/130313598-1f7727e6-73e3-4fec-8fcd-b00032164560.png)
   
- Khi mà cố gắng xem tập tin hình ảnh đã mã hoá bằng một phần mềm xem ảnh thì nó sẽ xuất hiện thông báo lỗi “BMP Image has bogus header data” bởi vì 54 byte đầu tiên chứa tiêu đề thông tin (header của hình ảnh) mà khi mã hoá đã bị thay đổi giá trị cho nên ta sẽ không thể xem được ảnh. 

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313610-d6a4dd70-399f-48e7-9bfa-7bff35ba1292.png)


- Mục tiêu yêu cầu 1 của nhiệm vụ này là tiến hành chỉnh sửa giá trị 54 byte đầu tiên của hình ảnh mã hoá này giống với 54 byte đầu tiên của hình ảnh gốc ban đầu. Ở đây chúng ta sẽ sử dụng câu lệnh như sau để thực hiện việc chỉnh sửa:

     + Đối với chế độ ECB:
      
     ![ảnh](https://user-images.githubusercontent.com/86979345/130313628-343ddaa7-1a56-4ce6-a2c6-d6cd61d1ecf3.png)

     + Đối với chế độ CBC:

     ![ảnh](https://user-images.githubusercontent.com/86979345/130313637-6750ed50-6da0-48fd-a3da-da138415e60c.png)

- Hình ảnh của 2 chế độ ECB và CBC sau khi chỉnh sửa sẽ như thế này

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313650-babf394d-cee1-43ac-8be1-c08246934668.png)
    
- Nhận xét:
    + Hình ảnh được mã hoá với chế độ ECB sẽ bị nhiễu chút ít so với hình ảnh gốc và người quan sát có thể ước lượng được bố cục của hình ảnh gốc. ECB là một chế độ tiêu chuẩn, bản rõ/bản mã ban đầu được phân ra thành các khối, mỗi khối sẽ được mã hoá/giải mã cùng với một khoá, các khối là hoàn toàn độc lập với nhau cho nên khi một khối bị hỏng thì nó sẽ không làm ảnh hướng đến các khối khác và hình ảnh vẫn được đảm bảo người quan sát có thể nhìn ra được.
    
    + Hình ảnh được mã hoá với chế độ CBC dường như bị nhiễu hoàn toàn và người quan sát không thể nào có thể ước lượng được bố cục của hình ảnh gốc. CBC ngoài việc mỗi khối sử dụng khoá ra thì nó còn sử dụng vector khởi tạo (IV). IV có cùng kích thước với khối được mã hoá/giải mã và thường là một số ngẫu nhiên. Bởi vì có sử dụng thêm IV sẽ làm tăng tính an toàn cho dữ liệu mã hoá. Mỗi khối sẽ được tiến hành thực hiện phép XOR với IV rồi tiến hành mã hoá/giải mã, đầu ra kết quả của việc giải mã trên sẽ được sử dụng cho khối tiếp theo nó vì vậy khi một khối mã bị hỏng thì nó sẽ ảnh hướng đến các khối mã khác.


# Task 4. Padding

- Trong yêu cầu 1 của nhiệm vụ này ta tiến hành tạo một tập tin văn bản plaintext.txt với kích thước là 6 bytes.

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313713-d477e49a-fadf-46b4-ba18-371c51cfe656.png)

- Thực hiện mã hoá tập tin với các chế độ ECB, CBC, CFB và OFB

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313717-ede4a62b-6ddf-4aa8-aa25-2280cef201b7.png)

- Sau khi thực hiện mã hoá thì ta có thể thấy rằng 

    + Chế độ OFB và CFB sẽ không có đệm vì chế độ OFB và CFB cho phép các khối mã hoá được sử dụng như là hệ mã dòng (Stream Cipher) do đó bản rõ không cần phải là bội số của kích thước khối, các chế độ này nó sẽ không mã hoá trực tiếp bản rõ mà nó chỉ sử dụng bản mã để XOR với bản rõ để lấy bản mã nên nó không cần phải chèn thêm dữ liệu.

    + Chế độ CBC và ECB có thực hiện việc thêm đệm vì các chế độ này bản rõ sẽ được chia thành các khối mã (Block Cipher) với kích thước cố định (ví dự như 64 hay 128 bit), nếu như khối không đủ kích thước thì nó sẽ tiến hành chèn thêm đệm vào để đảm bảo rằng mọi người đều có kích thước như nhau. Sau khi thực hiện giải mã thì phần đệm cũng sẽ được loại bỏ để đảm bảo nội dung y như lúc ban đầu.

- Trong yêu cầu 2 của nhiệm vụ ta thực hiện tạo tập tin f1.txt, f2.txt và f3.txt lần lượt với các kích thước là 5 bytes, 10 bytes và 16 bytes.

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313736-7a71c1f3-f401-48f0-b4f1-e1613c8f4063.png)

- Thực hiện mã hoá AES với chế độ CBC cho cả 3 tập tin trên

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313743-d2bee90d-9275-4778-95be-3a99199ccad8.png)

- Thực hiện giải mã ba tập tin mã hoá ở trên

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313745-6618e3c1-5d99-41de-838d-d535f5611783.png)

- Sử dụng câu lệnh hexdump để xem thông tin về phần đệm (padding) của các tập tin (ở đây bạn cũng có thể sử dụng công cụ khác chẳng hạn như bless, ghex để xem)

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313751-8c440d4c-a9aa-472e-a267-ac67e57bd156.png)
    
    
# Task 5. Lan truyền lỗi - văn bản mã hoá bị hỏng
- Phân tích trước khi thực hiện nhiệm vụ:
    + Chế độ ECB: Các khối trong ECB được mã hoá/giải mã hoàn toàn độc lập với nhau cho nên khi thay đổi 1 bit của byte trong 1 khối bất kỳ thì chỉ có khối duy nhất có byte bị thay đổi sẽ bị hỏng, các khối khác không bị ảnh hưởng.
    + Chế độ CBC: Do 1 bit của byte thứ 55 bị thay đổi nên khối chưa byte có bit bị thay đổi sẽ hỏng, đồng thời trong khối tiếp theo có byte ở vị trí tương ứng ở đây là byte thứ 71 so với byte thứ 55 cũng sẽ bị hỏng Do mỗi khối plaintext được XOR với khối ciphertext trước khi được mã hoá nên mỗi khối ciphertext phụ thuộc vào tất cả plaintext xuất hiện từ đầu đến thời điểm đó.
    + Chế độ CFB: Tương tự như CBC, khi thực hiện thay đổi 1 bit của byte thứ 55 thì ngoài việc byte thứ 55 bị hỏng nó sẽ còn ảnh hưởng đến khối tiếp theo.
    + Chế độ OFB: Do 1 bit của byte thứ 55 bị hỏng nên khi khối mã hoá được XOR với bản mã thì chỉ có 1 bit trong byte thứ 55 của khối đó bị hỏng, các byte khác trong khối cũng như các khối khác cũng không bị ảnh hưởng gì.


- Thực hiện nhiệm vụ và quan sát kết quả: Đầu tiên ta tạo một tập tin văn bản plaintext.txt với kích thước 1000 bytes

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313812-9980c1c1-8bbf-4ef0-8f33-415a5c5faf7e.png)

- Tiến hành mã hoá tập tin trên với các chế độ ECB, CBC, CFB và OFB

    
    ![ảnh](https://user-images.githubusercontent.com/86979345/130313820-31b46a48-9487-4754-9946-7c1a6b7ec5be.png)

- Ta sử dụng công cụ Bless (hoặc Ghex) để xem vị trí byte thứ 55 của tập tin đã bị mã hoá sau đó tiến hành sửa đổi giá trị tại vị trí này. Sau khi đã sửa đổi nội dung tại byte thứ 55 thì ta tiến hành giải mã các tập tin bị mã hoá và quan sát kết quả:

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313829-2a754b25-a840-439a-88ca-ec84f290f61f.png)


    + Quan sát đối với chế độ ECB
    
    ![ảnh](https://user-images.githubusercontent.com/86979345/130313839-e95b1df0-2802-4e23-b8d7-69ca16b42a12.png)

    + Quan sát đối với chế độ CBC

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313844-7fe6993d-c0e6-4ebc-99ca-25ed5461a6bb.png)
    
    ![ảnh](https://user-images.githubusercontent.com/86979345/130313845-9a76eca6-5895-4d1d-bd9c-7f0130056116.png)
    
    + Quan sát đối với chế độ CFB

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313849-6f33411e-f6d8-4015-b8e5-d8d339c9acb0.png)
    
    ![ảnh](https://user-images.githubusercontent.com/86979345/130313852-9aeaeba5-16bd-4104-a640-907d7b017677.png)
    
    + Quan sát đối với chế độ OFB
    
    ![ảnh](https://user-images.githubusercontent.com/86979345/130313858-f9291488-45b2-48e1-93fe-7da553bf3e4e.png)

- Ở đây chúng ta có thể viết một chương trình kiểm tra số byte khác so với bản rõ plaintext ban đầu. Đoạn chương trình như sau:

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313864-01b17511-e0e5-4fa9-948a-f197052e43d3.png)

- Tiến hành chạy chương trình để xem có bao nhiêu byte bị hỏng đối với từng chế độ

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313870-92aa98ee-8bb1-42a7-ab3d-f00c2d88266b.png)

- Nhận xét:
    + Đối với chế độ ECB: Chỉ có các byte từ thứ 49 đến byte thứ 64 (Offset 0x30 đến 0x3F) thuộc khối thứ 4 sẽ bị hỏng, còn các byte và các khối khác không bị ảnh hưởng gì.
    + Đối với chế độ CBC: Các byte từ thứ 49 đến byte thứ 64 (Offset 0x30 đến 0x3F) thuộc khối thứ 4 và byte thứ 71 (Offset 0x46) thuộc khối thứ 5 bị hỏng, còn các byte và các khối khác không bị ảnh hưởng gì.
    + Đối với chế độ CFB: Byte thứ 55 (Offset 0x36) thuộc khối thứ 4 và các byte thứ 65 đến byte thứ 80 (Offset 0x40 đến 0x4F) thuộc khối thứ 5 bị hỏng, còn các byte và các khối khác không bị ảnh hưởng gì.
    + Đối với chế độ OFB: Chỉ có byte thứ 55 (Offset 0x36) thuộc khối thứ 4 mà chúng ta đã chính sửa là bị hỏng, còn các byte và các khối khác không bị ảnh hưởng gì


# Task 6. Initial Vector (IV) và những sai lầm phổ biến

## Task 6.1
- Đầu ta ta thực hiện tạo một tập tin plaintext.txt với nội dung “this is content” và tiến hành mã hoá tập tin theo phương thức AES-128-CBC cho ra 2 tập tin same_iv_1.txt và same_iv_2.txt.
 
    ![ảnh](https://user-images.githubusercontent.com/86979345/130313935-198140d3-a93b-4e5c-922c-3193443d59db.png)

- Quan sát kết quả tập tin sau khi mã hoá có cùng IV thì ta có thể thấy nội dung đã mã hoá của cả hai tập tin là như nhau:

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313940-52b16a84-0bb6-4e18-8825-941570e6b0e9.png)

- Tiếp tục thực hiện mã hoá với trường hợp khác IV

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313945-dd5952a5-b0f5-4e5a-9c5b-8a9d9b5a9b6f.png) 

- Quan sát tập tin sau khi mã hoá với IV khác nhau thì ta có thể thấy nội dung đã mã hoá của hai tập tin là khác nhau

    ![ảnh](https://user-images.githubusercontent.com/86979345/130313956-70b9b3db-dae3-454e-95d8-730bb60dd4ae.png)

- Kết luận
    + Việc sử dụng cùng một IV trên cùng một bản rõ đã dẫn đến kết quả đầu ra giống hệt nhau
    + Việc sử dụng khác IV trên cùng một bản rõ dẫn đến kết quả đầu ra khác nhau.
    + IV cần là phải là duy nhất bởi vì nếu chúng ta sử dụng bản rõ nhiều hơn một lần, việc không có IV duy nhất mỗi lần với cùng một khoá sẽ dẫn đến một bản mã giống hệt nhau, từ đó mà kẻ tấn công có thể thu thập và phân tích ra nội dung bản rõ.

## Task 6.2. Sử dụng cùng một IV

- Đối với chế độ OFB, nếu khoá và IV không thay đổi thì việc tấn công bằng kỹ thuật known-plaintext có khả thi.

- Đầu ra có thể thu được bằng bản rõ XOR với bản mã theo khối. Tương tự, để có được bản rõ, chúng ta có thể XOR bản rõ và bản mã. Khi sử dụng cùng một khoá và IV cho chế độ OFB thì đầu ra giống hết nhau.

     ![ảnh](https://user-images.githubusercontent.com/86979345/130313986-3ec74539-c686-4d27-bc23-3f5ef6edfc0b.png)

- Giả sử rằng chúng ta biết một bản rõ P1 và bản mã OFB của nó là C1. Một bản mã OFB khác C2 có cùng khoá và IV. Nhưng chúng ta chưa biết bản rõ P2 của C2. Bằng cách nhìn vào hai bản mã C1 và C2 thì ta có thể đoán ký tự kết thúc của P2 cũng là một dấu “!”.
     
     
     ![ảnh](https://user-images.githubusercontent.com/86979345/130313991-16687bf7-4106-472d-bf21-f4bd39585c28.png)

- Đầu tiên ta thực lấy luồng kết quả mã hoá đầu ra của bản rõ P1

     + Output_stream = P1 XOR C1
      
- Bản rõ P2 được xác định:
     + P2 = Output_stream XOR C2

- Ta có thể viết ngắn ngọn lại thành:
     + P2 = P1 XOR C1 XOR C2

- Bây giờ ta sẽ viết một chương trình tấn công để tìm bản rõ P2

    ![ảnh](https://user-images.githubusercontent.com/86979345/130314038-ce125dd9-e028-458a-9be0-81f2866441fa.png)

- Kết quả sau khi thực hiện chương trình

    ![ảnh](https://user-images.githubusercontent.com/86979345/130314046-b80ded0d-dd4f-409b-a615-a68736640dc0.png)

- Bản rõ P2 tìm được là “Order: Launch a missible!”

- Với trường hợp chế độ CFB, kẻ tấn công chỉ biết khối đầu tiên của bản rõ mà thôi.


## Task 6.3 Sử dụng IV có thể đoán trước

- Giả sử ban đầu nội dung của bản rõ P1 là “Yes”

- Vì vậy bản mã P2 được xác định như sau:

    + P2 = “Yes” XOR IV XOR IV-NEXT

- Ta viết một chương trình để xác định P2 dựa trên công thức ở trên

    ![ảnh](https://user-images.githubusercontent.com/86979345/130314108-46b3dee0-888b-4186-b3b4-2c788e9e662c.png)

- Thực hiện chạy chương trình trên ta được kết quả P2 là Yes

    ![ảnh](https://user-images.githubusercontent.com/86979345/130314115-79e6ae62-dae4-47b3-ad1b-0e7f1d78209d.png)

- Tiến hành mã hoá P2 để xác định được C2. Vì đây là phương thức AES-128-CBC nên nó cần được chèn thêm đệm trước khi thực hiện mã hoá. Để so sánh với C1 thực tế, chúng ta chỉ cần khối đầu tiên của C2

    ![ảnh](https://user-images.githubusercontent.com/86979345/130314118-236c3207-ab88-4bae-84fd-32e890719b1c.png)

- Ta có thể thấy rằng 16 bytes (128 bit) của C2 giống với C1 mà đề cho nên ta có thể kết luận dự đoán ban đầu mà ta đưa ra là C1 có nội dung là “Yes” là chính xác. Để chắc chắn ta lấy 128 bit đầu của C2 cho nội dung của C1. Sau đó tiến hành mã hoá C1 ra để tìm nội dung của P1.

    ![ảnh](https://user-images.githubusercontent.com/86979345/130314127-166d88e4-e81c-4ce4-a8e5-a1d05b940c3a.png)

- Vậy là kết quả P1 có nội dung là “Yes”


# Task 7. Lập trình bằng thư viện Crypto

- Trong nhiệm vụ này chúng ta sẽ viết một chương trình ngôn ngữ Python sử dụng thư viện Crypto để tìm khoá chính xác trong danh sách tập tin khoá. Chương trình được viết như sau:

    ![ảnh](https://user-images.githubusercontent.com/86979345/130314154-d790a58e-47a8-4d2a-9925-385c26c9057d.png)

- Tiến hành chạy thử và truyền các tham số mà đề cung cấp

    ![ảnh](https://user-images.githubusercontent.com/86979345/130314162-eaf23f28-f7cf-4102-a6d5-863c589305ba.png)

- Vậy là khoá cần tìm là Syracuse
# SecretKey-SEEDLabs
