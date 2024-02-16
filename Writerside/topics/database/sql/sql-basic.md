# SQL cơ bản

Phần này giúp bạn bắt đầu với MySQL. Ta sẽ cài đặt MySQL Database Server, tải xuống cơ sở dữ liệu mẫu và tải tài liệu
vào MySQL Server để thực hành.

Sử dụng MySQL Workbench để thực hành truy vấn dữ liệu.

## Cài đặt MySQL Databases Server

Ta cài đặt MariaDB hoặc MySQL.
Có thể tham khảo tài liệu dưới đây:

1. [MariaDB Server](maria-db.md))
2. [MySQL Server](my-sql.md)

## Tải MySQL sample database

Ta sẽ tải Database sample từ [link](http://www.mysqltutorial.org/wp-content/uploads/2018/03/mysqlsampledatabase.zip).

File tải về sẽ là file nén ZIP nên ta sẽ phải giải nén sau đó import vào server.

Tải về database sample

```
[root@localhost ~]# wget http://www.mysqltutorial.org/wp-content/uploads/2018/03/mysqlsampledatabase.zip
```

Giải nén và import:

```
[root@localhost ~]# unzip mysqlsampledatabase.zip
Archive:  mysqlsampledatabase.zip
  inflating: mysqlsampledatabase.sql

[root@localhost ~]# mysql -u root -p
Enter password:
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 8
Server version: 10.4.11-MariaDB MariaDB Server

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> source /root/mysqlsampledatabase.sql
```

Kiểm tra database:

```
MariaDB [classicmodels]> show tables;
+-------------------------+
| Tables_in_classicmodels |
+-------------------------+
| customers               |
| employees               |
| offices                 |
| orderdetails            |
| orders                  |
| payments                |
| productlines            |
| products                |
+-------------------------+
8 rows in set (0.000 sec)
```

## Lược đồ cơ bản về Database Sample

Tên Database: `classicmodels`

Mô hình:

<img src = "https://i.imgur.com/mNOro37.png">

- `customers`: lưu trữ dữ liệu của khách hàng.
- `products`: lưu trữ một danh sách các mô hình quy mô xe.
- `productLines`: lưu trữ danh sách các danh mục dòng sản phẩm.
- `orders`: cửa hàng đặt hàng bán bởi khách hàng.
- `orderdetails`: lưu trữ các chi tiết đơn hàng cho mỗi đơn hàng.
- `payments`: lưu trữ các khoản thanh toán được thực hiện bởi khách hàng dựa trên tài khoản của họ.
- `employees`: lưu trữ tất cả thông tin của nhân viên cũng như cấu trúc tổ chức như ai báo cáo cho ai.
- `offices`: lưu trữ dữ liệu văn phòng bán hàng.

Bạn có thể tải về sơ đồ ER của database tại [đây](
http://www.mysqltutorial.org/wp-content/uploads/2018/04/MySQL-Sample-Database-Diagram-PDF-A4.pdf).

------------------------------------------------------------------------

## Kiểu dữ liệu

MySQL sử dụng nhiều kiểu dữ liệu khác nhau được chia thành ba loại –

- Số
- Ngày và giờ
- Các loại chuỗi.

### Kiểu dữ liệu số
MySQL sử dụng tất cả các kiểu dữ liệu số theo chuẩn ANSI SQL. Danh sách sau đây là các kiểu dữ liệu số phổ biến:

`INT`: Một số nguyên có kích thước bình thường có thể được sử dụng trong phạm vi số âm và số dương. Nếu được sử dụng khoảng âm, phạm vi cho phép là từ -2147483648 đến 2147483647. Nếu không phạm vi cho phép là từ 0 đến 4294967295. Bạn có thể chỉ định chiều rộng tối đa là 11 chữ số.

`TINYINT`: Một số nguyên rất nhỏ có thể được sử dụng trong phạm vi số âm và số dương. Nếu bao gồm số âm, phạm vi cho phép là từ -128 đến 127. Nếu không, phạm vi cho phép là từ 0 đến 255. Bạn có thể chỉ định chiều rộng tối đa 4 chữ số.

`SMALLINT`: Một số nguyên nhỏ có thể sử dụng trong phạm vi số âm và số dương. Nếu bao gồm số âm, phạm vi cho phép là từ -32768 đến 32767. Nếu không phạm vi cho phép là từ 0 đến 65535. Bạn có thể chỉ định chiều rộng tối đa 5 chữ số.

`MEDIUMINT`: Một số nguyên có kích thước trung bình có thể được sử dụng trong phạm vi số âm và số dương. Nếu bao gồm số âm, phạm vi cho phép là từ -8388608 đến 8388607. Nếu không, phạm vi cho phép là từ 0 đến 16777215. Bạn có thể chỉ định chiều rộng tối đa 9 chữ số.

`BIGINT`: Một số nguyên lớn có thể sử dụng trong phạm vi số âm và số dương. Nếu bao gồm số âm, phạm vi cho phép là từ -9223372036854775808 đến 9223372036854775807. Nếu không, phạm vi cho phép là từ 0 đến 18446744073709551615. Bạn có thể chỉ định chiều rộng tối đa 20 chữ số.

`FLOAT` (M, D): Một số dấu phẩy động được sử dụng để ngăn cách phần nguyên và phần hữu tỷ. Độ chính xác của số thập phân có thể lên tới 24 vị trí cho một FLOAT.

`DOUBLE` (M, D): Một số dấu chấm động được sử dụng để ngăn cách phần nguyên và phần hữu tỷ. Bạn có thể xác định độ dài hiển thị (M) và số thập phân (D). Độ chính xác thập phân có thể tới 53 vị trí cho một DOUBLE. REAL là một từ đồng nghĩa với DOUBLE.

`DECIMAL` (M, D): Một số dấu phẩy động được sử dụng để ngăn cách phần nguyên và phần hữu tỷ. Trong các số thập phân được giải nén, mỗi số thập phân tương ứng với một byte. Xác định độ dài hiển thị (M) và số thập phân (D) là bắt buộc. NUMERIC là một từ đồng nghĩa với DECIMAL.

### Kiểu dữ liệu ngày và giờ

`DATE`: Ngày theo định dạng YYYY-MM-DD, trong khoảng từ 1000-01-01 đến 9999-12-31. Ví dụ, ngày 30 tháng 12 năm 2018 sẽ được lưu trữ như 2018-12-30.
`
DATETIME`: Kết hợp ngày và giờ theo định dạng HH: MM: SS HHYYY-MM-DD, trong khoảng từ 1000-01-01 00:00:00 và 9999-12-31 23:59:59. Ví dụ: 5:30 chiều ngày 30 tháng 12 năm 2018 sẽ được lưu trữ là 2018-12-30 17:30:00.

`TIMESTAMP`: Mốc thời gian lúc nửa đêm. Kiểu này giống như định dạng DATETIME trước đó chỉ không có dấu gạch nối giữa các số; ví dụ: 3:30 chiều ngày 30 tháng 12 năm 2018 sẽ được lưu giữ là 20181230153000 (YYYYMMDDHHMMSS).

`TIME`: Lưu trữ thời gian theo định dạng HH: MM: SS.
YEAR (M): Lưu trữ một năm ở định dạng 2 chữ số hoặc 4 chữ số. Nếu độ dài được xác định là 2 (ví dụ NĂM (2)), NĂM có thể nằm trong khoảng từ 1970 đến 2069 (70 đến 69). Nếu độ dài được chỉ định là 4, thì YEAR có thể là 1901 đến 2155. Độ dài mặc định là 4.

### Kiểu dữ liệu String

`CHAR` (M): Một chuỗi có độ dài cố định trong khoảng từ 1 đến 255 ký tự (ví dụ CHAR (5)), được ghi thêm bên phải bằng dấu cách với độ dài được chỉ định khi lưu trữ. Việc xác định độ dài là không bắt buộc, nhưng mặc định là 1.

`VARCHAR` (M): Một chuỗi có độ dài từ 1 đến 255 ký tự. Ví dụ, VARCHAR (25). Bạn phải xác định độ dài khi tạo trường VARCHAR.

`BLOB` hoặc `TEXT`: Trường có độ dài tối đa 65535 ký tự. BLOB là “Đối tượng lớn nhị phân” và được sử dụng để lưu trữ lượng lớn dữ liệu nhị phân, chẳng hạn như hình ảnh hoặc các loại tệp khác. Các trường được định nghĩa là TEXT cũng chứa một lượng lớn dữ liệu. Sự khác biệt giữa hai loại và trên là dữ liệu được lưu trữ phân biệt chữ hoa chữ thường trên các BLOB và không phân biệt chữ hoa chữ thường trong các trường TEXT. Bạn không chỉ định độ dài cho BLOB hoặc TEXT.

`TINYBLOB` hoặc `TINYTEXT`: Cột BLOB hoặc TEXT có độ dài tối đa 255 ký tự. Bạn không chỉ định độ dài cho TINYBLOB hoặc TINYTEXT.

`MEDIUMBLOB` hoặc `MEDIUMTEXT`: Cột BLOB hoặc TEXT có độ dài tối đa 16777215 ký tự. Bạn không được chỉ định độ dài cho MEDIUMBLOB hoặc MEDIUMTEXT.

`LONGBLOB` hoặc `LONGTEXT`: Cột BLOB hoặc TEXT có chiều dài tối đa là 4294967295 ký tự. Bạn không được chỉ định độ dài cho LONGBLOB hoặc LONGTEXT.

`ENUM`: dùng để chỉ định một hằng số. Khi xác định một ENUM, bạn tạo một danh sách các mục mà từ đó giá trị phải được chọn (hoặc nó có thể là NULL).

------------------------------------------------------------------------

## Querying Data

### Chức năng

`SELECT` : được sử dụng để truy vấn dữ liệu từ một hoặc nhiều bảng.

### Cú pháp cơ bản

```sql
SELECT select_list
FROM table_name;
```

### Thứ tự đánh giá của SQL

<img src = "https://i.imgur.com/sIqesKh.png">

Tức là SQL sẽ xét `FROM` trước rồi đến `SELECT`

### Ví dụ

Ta sẽ sử dụng bảng `employees` để ví dụ về sử dụng `SELECT`:

<img src = "https://i.imgur.com/KWTyRMo.png">

<img src = "https://i.imgur.com/RjeusXU.png">

#### 1. Lấy dữ liệu từ 1 cột:

Lấy dữ liệu từ cột `email`

```sql
SELECT email
FROM employees;
```

**Kết quả**

<img src = "https://i.imgur.com/ylhGyyH.png">

#### 2. Lấy dữ liệu từ nhiều cột

Lấy dữ liệu từ 3 cột `lastname`, `firstname`, `jobtitle`

```sql
SELECT 
    lastname, 
    firstname, 
    jobtitle
FROM
    employees;
```

**Kết quả**

<img src = "https://i.imgur.com/c5TAbO6.png">

#### 3. Lấy tất cả dữ liệu của bảng:

```sql
SELECT *
FROM employees;
```

**Kết quả**

<img src = "https://i.imgur.com/RjeusXU.png">

#### **Chú ý**

Sử dụng `SELECT *` không nên được sử dụng bừa bãi vì một số lý do sau:

- Nó trả về dữ liệu từ tất cả các cột mà có thể ta không dùng đến.
- Khi chỉ định rõ tên cột sẽ dễ dàng quản lý hơn.
- Khi một bảng có sự thay đổi thì tập kết quả trả về sẽ thay đổi và có thể dẫn đến những lỗi xử lý.
- Có thể bị tiết lộ những thông tin nhạy cảm cho người dùng trái phép.

------------------------------------------------------------------------

## Sorting Data

### Chức năng

Dùng để sắp xếp các dữ liệu được trả về từ truy vấn `SELECT`.

### Cú pháp

```sql
SELECT 
   select_list
FROM 
   table_name
ORDER BY 
   column1 [ASC|DESC], 
   column2 [ASC|DESC],
   ...;
```

Trong đó:

- `ASC`: (ascending) là sắp xếp tăng dần
- `DESC`: (descending) là sắp xếp giảm dần

### Thứ tự đánh giá của SQL

<img src ="https://i.imgur.com/NPKtwpT.png">

`ORDER BY` luôn được đánh giá sau `FROM` và `SELECT`.

### Ví dụ

Sử dụng bảng `customers`

<img src = "https://i.imgur.com/3KHeatZ.png">

#### 1. Sắp xếp dữ liệu theo 1 cột

Sắp xếp `customers` theo giá trị tăng dần từ cột `contactLastName`

```sql
SELECT
    contactLastname,
    contactFirstname
FROM
    customers
ORDER BY
    contactLastname;
```

Kết quả:

<img src = "https://i.imgur.com/d4D4dxt.png">

#### 2. Sắp xếp dữ liệu theo nhiều cột

Sắp xếp các `customers` theo giảm dần của `contactLastname` và tăng dần của `contactFirstname`. Ta sử dụng `DESC`
và `ASC`:

```sql
SELECT
    contactLastname,
    contactFirstname
FROM
    customers
ORDER BY
    contactLastname DESC,
    contactFirstname ASC;
```

Kết quả:

<img src = "https://i.imgur.com/i8ND5EU.png">

#### 3. Sắp xếp kết quả của một phép tính

Sử dụng bảng `orderdetails`

<img src = "https://i.imgur.com/XvbPT6O.png">

Sắp xếp dựa trên phép tính `quantityOrdered` * `priceEach`

```sql
SELECT 
    orderNumber, 
    orderlinenumber, 
    quantityOrdered * priceEach
FROM
    orderdetails
ORDER BY 
   quantityOrdered * priceEach DESC;
```

Kết quả:

<img src = "https://i.imgur.com/Y6ZUp18.png">

Để kết quả truy vấn dễ đọc hơn, ta có thể gán cột `quantityOrdered * priceEach` bằng tên khác ngắn hơn, sử dụng `AS`:

```sql
SELECT 
    orderNumber,
    orderLineNumber,
    quantityOrdered * priceEach AS subtotal
FROM
    orderdetails
ORDER BY subtotal DESC;
```

Kết quả:

<img src ="https://i.imgur.com/nYHB4me.png">

#### 4. Sắp xếp tùy chỉnh

Sử dụng `FIELD()`.

Ta sử dụng bảng `order`:

<img src = "https://i.imgur.com/KGBzomu.png">

Bạn muốn sắp xếp đơn hàng theo thứ tự trạng thái như sau:

- In Process
- On Hold
- Canceled
- Resolved
- Disputed
- Shipped

```sql
SELECT 
    orderNumber, 
    status
FROM
    orders
ORDER BY 
    FIELD(status,
        'In Process',
        'On Hold',
        'Cancelled',
        'Resolved',
        'Disputed',
        'Shipped');
```

Kết quả:

<img src ="https://i.imgur.com/AKYreHi.png">

------------------------------------------------------------------------

## `WHERE`

### Chức năng

`WHERE` : Dùng để lọc kết quả truy vấn(SELECT), cập nhật(UPDATE), xóa (DELETE)

### Cú pháp cơ bản

```sql
SELECT 
    select_list
FROM
    table_name
WHERE
    search_condition;
```

- `search_condition` là sự kết hợp của một hoặc nhiều biến vị ngữ bằng cách sử dụng toán tử
  logic `AND`, `OR`, `NOT`,`=`.
- Trong MySQL một biểu thức boolean có các giá trị `TRUE`, `FALSE` hoặc `UNKNOWN`.

### Thứ tự đánh giá SQL

<img src = "https://i.imgur.com/7bSN5JH.png">

### Cách sử dụng

Ta sẽ sử dụng bảng `employees` để thực hiện

<img src = "https://i.imgur.com/KWTyRMo.png">

#### 1. Sử dụng `WHERE` với toán tử `=`:

Lọc các nhân viên có `jobtitle` là "*Sales Rep*"

```sql
SELECT 
    lastname, 
    firstname, 
    jobtitle
FROM
    employees
WHERE
    jobtitle = 'Sales Rep';
```

Kết quả:

<img src = "https://i.imgur.com/4sNW9JU.png">

#### 2. Sử dụng `WHERE` với toán tử `AND`:

Lọc các nhân viên có `jobtitle` là "*Sales Rep*" và `officeCode` = 2;

```sql
SELECT 
    lastname, 
    firstname, 
    jobtitle,
    officeCode
FROM
    employees
WHERE
    jobtitle = 'Sales Rep' AND 
    officeCode = 2;
```

Kết quả:

<img src = "https://i.imgur.com/mlrPOXn.png">

#### 3. Sử dụng `WHERE` với toán tử `OR`:

Lọc các nhân viên có `jobtitle` là "*Sales Rep*" hoặc `officeCode` = 1;

```sql
SELECT 
    lastName, 
    firstName, 
    jobTitle, 
    officeCode
FROM
    employees
WHERE
    jobtitle = 'Sales Rep' OR 
    officeCode = 1;
```

Kết quả:

<img src = "https://i.imgur.com/HLZTo9K.png">

#### 4. Sử dụng `WHERE` với toán tử `BETWEEN`:

`expression BETWEEN low AND high`

Lọc các nhân viên có `officeCode` trong khoảng từ 1 đến 3:

```sql
select 
	firstName,
	lastName,
	officeCode
from
	employees
where
	officeCode between 1 and 3;
```

Kết quả:

<img src = "https://i.imgur.com/2qaVtsx.png">

#### 5. Sử dụng `WHERE` với toán tử `LIKE`:

Truy vấn các nhân viên có tên kết thúc là '`son`':

```sql
SELECT 
    firstName, 
    lastName
FROM
    employees
WHERE
    lastName LIKE '%son';
```

Kết quả:

<img src = "https://i.imgur.com/b9PsZWA.png">

#### 6. Sử dụng `WHERE` với toán tử `IN`:

`value IN (value1, value2,...)`

Lọc ra những nhân viên có `officeCode` có giá trị là 1 và 3.

```sql
SELECT 
    firstName, 
    lastName, 
    officeCode
FROM
    employees
WHERE
    officeCode IN (1 , 3);
```

Kết quả:

<img src = "https://i.imgur.com/DU0YwSD.png">

#### 7. Sử dụng `WHERE` với `IS NULL`

`value IS NULL`

Lọc những nhân viên mà cột `reportTo` có giá trị `NULL`:

```sql
SELECT 
	lastName,
    firstName,
    reportsTo
FROM 
	employees
WHERE
	reportsTo IS NULL;
```

Kết quả:

<img src = "https://i.imgur.com/x58yLaq.png">

#### 8. Sử dụng `WHERE` với toán tử so sánh

| Toán tử    | Ý nghĩa                                                            |
|------------|--------------------------------------------------------------------|
| =          | Bằng. Có thể sử dụng với hầu hết các loại dữ liệu                  |
| <> hoặc != | Không bằng                                                         |
| <          | Nhỏ hơn. Thường sử dụng với các loại dữ liệu số và ngày, thời gian |
| >          | Lớn hơn                                                            |
| <=         | Nhở hơn hoặc bằng                                                  |
| >=         | Lớn hơn hoặc bằng                                                  |

Ta sẽ lọc các nhân viên mà `jobtitle` không phải "*Sales Rep*":

```sql
SELECT
    lastname,
    firstname,
    jobTitle
FROM
    employees
WHERE
    jobTitle <> 'Sales Rep';
```

Kết quả:

<img src = "https://i.imgur.com/HqgEH4i.png">

------------------------------------------------------------------------

## `SELECT  DISTINCT`

### Chức năng

`DISTINCT`  dùng để loại bỏ các hàng trùng lặp trong tập kết quả truy vấn.

### Cú pháp cơ bản

```sql
SELECT DISTINCT
    select_list
FROM
    table_name;
```

### Cách sử dụng

Ta sẽ sử dụng bảng `employees` để thử truy vấn.

<img src = "https://i.imgur.com/KWTyRMo.png">

Trước tiên, ta sẽ thử truy vấn không có `DISTINCT`:

```sql
SELECT 
    lastname
FROM
    employees
ORDER BY 
    lastname;
```

Kết quả:

<img src = "https://i.imgur.com/CWpiRkQ.png">

-> Có những tên trùng nhau

Bây giờ ta sẽ thêm `DISTINCT`:

```sql
SELECT DISTINCT
    lastname
FROM
    employees
ORDER BY 
    lastname;
```

Kết quả:

<img src = "https://i.imgur.com/WOZfiS2.png">

-> Mỗi tên chỉ xuất hiện một lần. Không có trùng lặp.

### Chú ý:

- Các toán tử `AND`, `OR`, `NOT`, `BETWEEN`, ... đều sử dụng như bình thường.
- Các giá `NULL` thì coi như cùng một giá trị.

------------------------------------------------------------------------

## `IN`

### Chức năng

`IN` dùng để xác định xem một giá trị được chỉ định có khớp với giá trị nào trong danh sách truy vấn hoặc truy vấn con(
subquery) hay không.

### Cú pháp cơ bản

```sql
SELECT 
    column1,column2,...
FROM
    table_name
WHERE 
    (expr|column_1) IN ('value1','value2',...);
```

### Cách sử dụng

#### 1. Sử dụng `IN` kiếm tra giá trị trong danh sách truy vấn:

Ta sẽ sử dụng bảng `employees` để thực hiện

<img src = "https://i.imgur.com/KWTyRMo.png">

Lọc ra những nhân viên có `officeCode` có giá trị là 1 và 3.

```sql
SELECT 
    firstName, 
    lastName, 
    officeCode
FROM
    employees
WHERE
    officeCode IN (1 , 3);
```

Kết quả:

<img src = "https://i.imgur.com/DU0YwSD.png">

#### 2. Sử dụng `IN` trong subquery:

Toán tử `IN` thường được sử dụng với toán tử con. Thay vì cung cấp danh sách các giá trị bằng chữ, truy vấn con nhận
danh sách các giá trị từ một hay nhiều bảng và sử dụng chúng làm giá trị đầu vào của toán tưt `IN`.

Ta sẽ lấy 2 bảng `orders` và `orderDetails`

<img src = "https://i.imgur.com/WC2fGAf.png">

Ta sẽ tìm các đơn hàng có tổng giá trị lớn hơn 60000.

```sql
SELECT 
	orderNumber,
    customerNumber,
    status,
    shippedDate
FROM
	orders
WHERE orderNumber IN 
(
	SELECT 
		orderNumber
	FROM
		orderdetails
	GROUP BY
		orderNumber
	HAVING 
        SUM(quantityOrdered * priceEach) > 60000
)
```

Kết quả:

<img src = "https://i.imgur.com/XCY86Ao.png">

Truy vấn trên có thể được chia thành 2 truy vấn riêng biệt:

**Truy vấn 1:** Truy vấn 1 trả về danh sách các số thứ tự có giá trị lớn hơn 60000 bằng cách sử dụng `GROUP BY`
và `HAVING`

```sql
SELECT 
    orderNumber
FROM
    orderdetails
GROUP BY orderNumber
HAVING SUM(quantityOrdered * priceEach) > 60000;
```

<img src = "https://i.imgur.com/PLrpHPQ.png">

**Truy vấn 2:** Truy vấn 2 lấy dữ liệu từ đơn hàng

```sql
SELECT 
    orderNumber, 
    customerNumber, 
    status, 
    shippedDate
FROM
    orders
WHERE
    orderNumber IN (10165,10287,10310);
```

------------------------------------------------------------------------

## `LIKE`

### Chức năng

LIKE dùng để truy vấn dữ liệu dựa trên một mô hình cụ thể.

### Cú pháp cơ bản

Toán tử `LIKE` là toán tử logic kiểm tra xem một chuỗi có chứa một mẫu đã chỉ định hay không.

Đây là cú pháp của toán tử `LIKE`:

```sql
expression LIKE pattern ESCAPE escape_character
```

MySQL cung cấp 2 ký tự đại diện để xây dựng mẫu:

- `%` : phù hợp với bất kỳ chuỗi và ký tự
  Ví dụ: s% -> sun, six, salt, ...
- `_` : phù hợp với bất kỳ kí tự đơn
  Ví dụ: s_n -> sin, sun, son, ...

Nếu dữ liệu bạn cần có chứa "`%`" hay "`_`" thì bạn cần dùng "`\`" để chỉ định kí tự thoát. Nếu bạn không chỉ định rõ
ràng ký tự thoát, ký tự dấu gạch chéo ngược "`\`" là ký tự thoát mặc định.

Ví dụ:

```sql
SELECT 
    productCode, 
    productName
FROM
    products
WHERE
    productCode LIKE '%\_20%';
```

<img src ="https://i.imgur.com/DhBZqr3.png">

Hoặc bạn có thể chỉ định một ký tự thoát khác, ví dụ: `$` bằng cách sử dụng mệnh đề `ESCAPE`:

```sql
SELECT 
    productCode, 
    productName
FROM
    products
WHERE
    productCode LIKE '%$_20%' ESCAPE '$';
```

<img src = "https://i.imgur.com/zX0Jczd.png">

------------------------------------------------------------------------

## `LIMIT`

### Chức năng

Dùng để hạn chế số lượng kết quả trả về bởi một truy vấn.

### Cú pháp cơ bản

```sql
SELECT 
    select_list
FROM
    table_name
LIMIT [offset,] row_count;
```

- `offset` : phần bù của hàng đầu tiên trả về. offset của cột đầu tiên là 0.
- `row_count` : số lượng hàng tối đa trả về

Hình ảnh minh họa:

<img src = "https://i.imgur.com/D7GGCSv.png">

Khi bạn sử dụng mệnh đề LIMIT với một đối số, MySQL sẽ sử dụng đối số này để xác định số lượng hàng tối đa để trả về từ
hàng đầu tiên của tập kết quả.

### Thứ tự đánh giá của SQL

<img src = "https://i.imgur.com/Y9pY3lU.png">

### Cách sử dụng

Ta sử dụng bảng `customers` để thực hiện.

<img src = "https://i.imgur.com/O0o4sZq.png">

1. Lấy một số lượng nhất định có giá trị cao nhất hoặc thấp nhất
   Lấy ra 5 khách hàng có mức tín dụng cao nhất

```sql
SELECT 
    customerNumber, 
    customerName, 
    creditLimit
FROM
    customers
ORDER BY creditLimit DESC
LIMIT 5;
```

Kết quả:

<img src = "https://i.imgur.com/wm4XomD.png">

2. Phân trang
   Khi bạn hiển thị dữ liệu trên các ứng dụng, bạn thường muốn chia các hàng thành các trang, trong đó mỗi trang chứa
   một số hàng nhất định như 5, 10 hoặc 20.

Để tính số lượng trang, bạn lấy tổng số hàng chia cho số lượng hàng trên mỗi trang. Để tìm nạp các hàng của một trang cụ
thể, bạn có thể sử dụng mệnh đề LIMIT.

`COUNT(*)` để lấy tổng số hàng từ bảng `customers`:

```sql
SELECT COUNT(*) FROM customers;
```

<img src = "https://i.imgur.com/UDR0cck.png">

Giả sử mỗi trang có 10 hàng, để hiển thị 122 khách hàng, bạn có 13 trang. Trang thứ 13 cuối cùng chỉ chứa hai hàng.

Truy vấn này sử dụng mệnh đề LIMIT để lấy các hàng của trang 1 chứa 10 khách hàng đầu tiên được sắp xếp theo tên khách
hàng:

```sql
SELECT 
    customerNumber, 
    customerName
FROM
    customers
ORDER BY customerName    
LIMIT 10;
```

<img src = "https://i.imgur.com/PfHXAuF.png">

Truy vấn này sử dụng mệnh đề LIMIT để lấy các hàng của trang thứ hai bao gồm hàng 11 - 20:

```sql
SELECT 
    customerNumber, 
    customerName
FROM
    customers
ORDER BY customerName    
LIMIT 10, 10;
```

<img src = "https://i.imgur.com/pmIivFj.png">

3. Lấy giá trị cao nhất, thấp nhất thứ n:

```sql
SELECT select_list
FROM table_name
ORDER BY sort_expression
LIMIT n-1, 1;
```

Ví dụ: Lấy giá trị cao thứ 3 tín dụng:

```sql
SELECT 
    customerName, 
    creditLimit
FROM
    customers
ORDER BY 
    creditLimit DESC    
LIMIT 2,1;
```

<img src = "https://i.imgur.com/SETbfof.png">

Kiểm tra lại danh sách đầy đủ:

```sql
SELECT 
    customerName, 
    creditLimit
FROM
    customers
ORDER BY 
    creditLimit DESC;
```

<img src = "https://i.imgur.com/LxKVWU8.png">

------------------------------------------------------------------------

## Table & Column Aliases

### Chức năng

MySQL Aliases dùng để cải thiện đọc của các truy vấn bằng cách đặt bí danh.

### Đặt bí danh cho các cột

Đôi khi các tên của cột thực tế dài và khó hiểu, vì vậy đặt bí danh cho cột là một ý tưởng hợp lí.

#### Cú pháp

```sql
SELECT 
   [column_1 | expression] AS descriptive_name
FROM table_name;
```

Nếu bí danh có dấu khoảng trắng thì ta sử dụng thêm dấu

```sql
`descriptive name`
```

#### Ví dụ

Sử dụng bảng `employese`

<img src = "https://i.imgur.com/CjSGH6D.png">

Truy vấn sau đây chọn tên và họ của nhân viên. Nó sử dụng hàm `CONCAT_WS ()` để ghép tên và họ thành tên đầy đủ.

```sql
SELECT 
    CONCAT_WS(', ', lastName, firstname)
FROM
    employees;
```

<img src = "https://i.imgur.com/oAuCcDu.png">


Bảng kết quả tên cột nhìn dài và khó hiểu. Nên ta sẽ đặt bí danh cho nó:

```sql
SELECT
   CONCAT_WS(', ', lastName, firstname) AS `Full name`
FROM
   employees;
```

<img src = "https://i.imgur.com/LGRY2H1.png">

Trong MySQL, bạn có thể sử dụng bí danh cột trong `ORDER BY`, `GROUP BY` và `HAVING` để chỉ cột.

### Đặt bí danh cho bảng

Cũng giống như cột, bạn có thể đặt bí danh cho bảng.

#### Cú pháp

```sql
table_name AS table_alias
```

Các bí danh cho bảng thường được sử dụng trong câu lệnh có chứa `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`.

#### Ví dụ

Đặt `employese` bí danh bảng là e.

```
SELECT * FROM employees e;
```

Sử dụng bảng `employese`. Truy vấn danh sách nhân viên sắp xếp theo `firstName`:

<img src = "https://i.imgur.com/CjSGH6D.png">

```sql
SELECT 
    e.firstName, 
    e.lastName
FROM
    employees e
ORDER BY e.firstName;
```

<img src = "https://i.imgur.com/vfBHx4S.png">

------------------------------------------------------------------------

## JOIN

Một cơ sở dữ liệu quan hệ bao gồm nhiều bảng liên quan liên kết với nhau bằng các cột chung được gọi là khóa
ngoài (`foreign key`). Vì vậy, dữ liệu từ 1 bảng không đầy đủ theo góc độ kinh doanh.

Để có thể có được dữ liệu đầy đủ ta cần `JOIN` các bảng lại với nhau để có được dữ liệu cần thiết.

Ví dụ: Ta có 2 bảng dữ liệu `orders` và `orderdetails` liên kết với nhau bằng cột `orderNumber`.
<img src ="https://i.imgur.com/egkouFP.png">

Để có thông tin đơn hàng hoàn chỉnh, ta cần truy vấn dữ liệu từ cả 2 bảng `orders` và `orderdetails`.
Chính vì vậy nên chúng ta cần `JOIN`.

MySQL hỗ trợ các kiểu JOIN sau:

- Inner join
- Left join
- Right join
- Cross join

------------------------------------------------------------------------

## `INNER JOIN`

Trong bài viết này, ta sẽ tìm hiểu cách sử dụng mệnh đề `INNER JOIN` để lấy dữ liệu từ nhiều bảng dựa trên các điều
kiện.

### Chức năng

`INNER JOIN` khớp từng hàng trong 1 bảng với mỗi hàng trong bảng khác và cho phép bạn truy vấn các hàng có chứa các cột
chung từ 2 bảng.

### Cú pháp cơ bản

```sql
SELECT
    select_list
FROM t1
INNER JOIN t2 ON join_condition1
INNER JOIN t3 ON join_condition2
...;
```

Trong đó:

- Bảng chính là `t1`
- Bảng chỉ định sẽ được nối với bảng chính: `t2`, `t3`, ...
- Điều kiện nối xác định quy tắc khớp các hàng của bảng chính với các bảng chỉ định.

Sơ đồ Venn minh họa cách hoạt động của `INNER JOIN`:

<img src = "https://i.imgur.com/2tLh5xM.png">

### Ví dụ về cách sử dụng

#### 1. Sử dụng `INNER JOIN` cơ bản

Ta sử dụng 2 bảng `products` và `productlines`:

<img src ="https://i.imgur.com/5NK3aOy.png">

Theo sơ đồ, ta thấy bảng `products` có cột `productLine` tham chiếu giá trị của cột `productLine` của
bảng `productlines`. Cột `productLine` trong bảng `products` được gọi là khóa ngoại.

**Yêu cầu**:

- Lấy `productCode` và `productName` từ bảng `products`
- Lấy `textDescription` của dòng sản phẩm từ bảng `productlines`

Để làm điều này, ta sẽ lấy dữ liệu cả 2 bảng bằng cách khớp các hàng dựa trên các giá trị trong cột `productline` bẳng
mệnh đề `INNER JOIN`:

```sql
SELECT 
    productCode, 
    productName, 
    textDescription
FROM
    products t1
INNER JOIN productlines t2 
    ON t1.productline = t2.productline;
```

Kết quả:

<img src = "https://i.imgur.com/a9FIgfM.png">

Vì các cột được nối của 2 bảng có cùng tên `productline` nên ta có thể sử dụng `USING` như sau:

```sql
SELECT 
    productCode, 
    productName, 
    textDescription
FROM
    products
INNER JOIN productlines USING (productline);
```

#### 2. Sử dụng `INNER JOIN` với `GROUP BY`

Ta sử dụng 2 bảng `orders` và `orderdetails`

<img src = "https://i.imgur.com/egkouFP.png">

Truy vấn trả về số thứ tự, trạng thái đơn hàng và tổng doanh số từ 2 bảng `orders` và `orderdetails`:

```sql
SELECT 
    t1.orderNumber,
    t1.status,
    SUM(quantityOrdered * priceEach) total
FROM
    orders t1
INNER JOIN orderdetails t2 
    ON t1.orderNumber = t2.orderNumber
GROUP BY orderNumber;
```

Kết quả:

<img src = "https://i.imgur.com/IEnyxb3.png">

Tương tự, ta có thể sử dụng với `USING`:

```sql
SELECT 
    orderNumber,
    status,
    SUM(quantityOrdered * priceEach) total
FROM
    orders
INNER JOIN orderdetails USING (orderNumber)
GROUP BY orderNumber;
```

#### 3. Sử dụng `INNER JOIN` 3 bảng

Ta sẽ dùng 3 bảng `products`, `orders`, `orderdetails`. Truy vấn ra danh sách đặt hàng kèm tên với giá sản phẩm,...

<img src = "https://i.imgur.com/LVkuQRz.png">

```sql
SELECT 
    orderNumber,
    orderDate,
    orderLineNumber,
    productName,
    quantityOrdered,
    priceEach
FROM
    orders
INNER JOIN
    orderdetails USING (orderNumber)
INNER JOIN
    products USING (productCode)
ORDER BY 
    orderNumber, 
    orderLineNumber;
```

Kết quả:

<img src = "https://i.imgur.com/BHRyHd5.png">

#### 4. Sử dụng `INNER JOIN` với các toán tử khác

Ta sẽ truy vấn để tìm giá sản phẩm có mã `S10_1949` có giá thấp hơn giá đề xuất của nhà sản xuất (`msrp`).

```sql
SELECT 
    orderNumber, 
    productName, 
    msrp, 
    priceEach
FROM
    products p
INNER JOIN orderdetails o 
   ON p.productcode = o.productcode
      AND p.msrp > o.priceEach
WHERE
    p.productcode = 'S10_1949';
```

Kết quả:

<img src = "https://i.imgur.com/FvETN1R.png">

------------------------------------------------------------------------

## `LEFT JOIN`

Trong bài viết này, ta sẽ tìm hiểu cách sử dụng mệnh đề `LEFT JOIN` để lấy dữ liệu từ nhiều bảng dựa trên các điều kiện.

### Cú pháp cơ bản

```sql
SELECT 
    select_list
FROM
    t1
LEFT JOIN t2 ON 
    join_condition;
```

- `t1` là bảng bên trái
- `t2` là bảng bên phải

### Cách hoạt động

`LEFT JOIN` sẽ lấy dữ liệu từ bảng bên trái (`t1`). Nó sẽ khớp với từng hàng từ bảng bên trái (`t1`) với mỗi hàng của
bảng bên phải (`t2`) dựa trên điều kiện `join_condition`.

Nếu các hàng từ 2 bảng thỏa mãn điều kiện, thì sẽ tạo thành 1 hàng mới gồm các cột của 2 bảng này.

Trong trường hợp hàng từ bảng bên trái (`t1`) không khớp với bất kì hàng nào trong bảng bên phải(`t2`). `LEFT JOIN` vẫn
kết hợp các cột từ các hàng từ 2 bảng thành 1 hàng mới. Tuy nhiên, nó sẽ để giá trị `NULL` cho tất cả các cột của hàng
bên phải.

Nói cách khác, `LEFT JOIN` trả về tất cả các hàng từ bảng bên trái(`t1`) bất kể bảng bên phải(`t2`) có 1 hàng nào phù
hợp hay không. Nếu không có kết quả khớp, các cột của hàng từ bảng bên phải(`t2`) sẽ có giá trị `NULL`.

Sơ đồ Venn minh họa cách hoạt động của `LEFT JOIN`
<img src = "https://i.imgur.com/vDWk5m6.png">

### Ví dụ về cách sử dụng

#### 1. `LEFT JOIN` với 2 bảng

Ta sử dụng 2 bảng `customers` và `orders`

<img src= "https://i.imgur.com/8dneoPw.png">

Theo sơ đồ thì mỗi `customers` có thể có nhiều `orders`, còn mỗi `orders` chỉ từ 1 `customers`.

Truy vấn lấy ra tất cả các khách hàng và đơn hàng của họ.

```sql
SELECT 
    customers.customerNumber, 
    customerName, 
    orderNumber, 
    status
FROM
    customers
LEFT JOIN orders ON 
    orders.customerNumber = customers.customerNumber;
```

Ta có thể sử dụng cách đặt bí danh bảng:

```sql
SELECT
    c.customerNumber,
    customerName,
    orderNumber,
    status
FROM
    customers c
LEFT JOIN orders o 
    ON c.customerNumber = o.customerNumber;
```

Kết quả:

<img src = "https://i.imgur.com/DD5Igl0.png">

Do 2 cột `customerNumber` của 2 bảng giống nhau nên ta có thể sử dụng `USING` như sau:

```sql
SELECT
    customerNumber,
    customerName,
    orderNumber,
    status
FROM
    customers
LEFT JOIN orders USING (customerNumber);
```

#### 2. `LEFT JOIN` với `IS NULL`

Tìm những khách hàng không có đơn hàng.

```sql
SELECT 
    c.customerNumber, 
    c.customerName, 
    o.orderNumber, 
    o.status
FROM
    customers c
LEFT JOIN orders o 
    ON c.customerNumber = o.customerNumber
WHERE
    orderNumber IS NULL;
```

Kết quả:

<img src = "https://i.imgur.com/xZFx6ce.png">

#### 3. `LEFT JOIN` với 3 bảng

Sử dụng 3 bảng `employees`, `customers`, và `payments`:
<img src  ="https://i.imgur.com/IPLbBPC.png">

Truy vấn ra danh sách tất cả các nhân viên và các khách hàng mà họ phụ trách.

```sql
SELECT 
    e.lastName, 
    e.firstName, 
    c.customerName, 
    p.checkNumber, 
    p.amount
FROM
    employees e
LEFT JOIN customers c ON 
    e.employeeNumber = c.salesRepEmployeeNumber
LEFT JOIN payments p ON 
    p.customerNumber = c.customerNumber
ORDER BY 
    customerName, 
    checkNumber;
```

Kết quả:

<img src = "https://i.imgur.com/wgUJknP.png">

- `LEFT JOIN` thứ nhất trả về tất cả các nhân viên và khách hàng của họ quản lí hoặc trả về giá trị `NULL` nếu không
  quản lí khách hàng nào.
- `LEFT JOIN` thứ hai trả về tất cả các khoản thanh toán của mỗi khách hàng được đại diện bởi nhân viên nào đó hoặc trả
  về `NULL` nếu khách hàng không có khoản thanh toán nào.

#### 4. `LEFT JOIN` với 2 mệnh đề `WHERE` và `ON`

**Sử dụng mệnh đề `WHERE`:**

Truy vấn dữ liệu trong bảng `orders` và `orderDetails` trả về đơn hàng chi tiết đơn hàng của số đơn hàng '*10123*'

```sql
SELECT 
    o.orderNumber, 
    o.customerNumber, 
    od.productCode
FROM
    orders o
LEFT JOIN orderdetails od
    USING (orderNumber)
WHERE
    orderNumber = 10123;
```

<img src = "https://i.imgur.com/hLXdFfz.png">


**Nếu ta sử dụng mệnh đề `ON`:**

```sql
SELECT 
    o.orderNumber, 
    o.customerNumber, 
    od.productCode
FROM
    orders o
LEFT JOIN orderdetails od 
    ON o.orderNumber = od.orderNumber AND 
       o.orderNumber = 10123;
```

<img src = "https://i.imgur.com/86nDPsJ.png">

Ở đây sẽ trả về tất cả đơn hàng nhưng chỉ có đơn hàng có `orderNumber` = 10123 là có chi tiết đơn hàng.

------------------------------------------------------------------------

## `RIGHT JOIN`

Giống với `LEFT JOIN`, ngoại trừ việc đảo ngược các bảng được sử dụng.

### Cú pháp cơ bản

```sql
SELECT 
    select_last
FROM t1
RIGHT JOIN t2 ON 
    join_condition;
```

Trong đó:

- `t1` là bảng bên trái
- `t2` là bảng bên phải

### Cách hoạt động

`RIGHT JOIN` sẽ bắt đầu chọn dữ liệu từ bảng bên phải (`t2`). Nó sẽ khớp từng hàng từ bảng bên phải với mỗi hàng từ bảng
bên trái. Nếu thỏa mãn điều kiện thì nó sẽ kết hợp các cột thành 1 hàng mới.

Nếu 1 hàng từ bảng bên phải không có 1 hàng phù hợp từ bảng bên trái, nó sẽ kết hợp các cột của các hàng từ bảng bên
phải với các giá trị NULL thành 1 hàng mới.

Nói cách khác, `RIGHT JOIN` trả về tất cả các hàng từ bảng bên phải bất kể bảng bên trái có hàng phù hợp hay không.

### Ví dụ về cách sử dụng

Chúng ta sẽ sử dụng 2 bảng `employees` và `customers`
<img src = "https://i.imgur.com/qdWqvM4.png">

Cột `salesRepEmployeeNumber` trong bảng `customers` liên kết với cột `employeeNumber` của bảng `employees`.

Một `employees` có thể phụ trách 0 hay nhiều `customers`. Mỗi `customers` được chăm sóc bởi 0 hoặc 1 `employees`.

Nếu giá trị trong cột `salesRepEmployeeNumber` là NULL, điều đó có nghĩa là khách hàng không có bất kỳ đại diện bán hàng
nào.

#### 1. `RIGHT JOIN` đơn giản

Truy vấn ra mã nhân viên và mã khách hàng tương ứng.

```sql
SELECT 
    employeeNumber, 
    customerNumber
FROM
    customers
RIGHT JOIN employees 
    ON salesRepEmployeeNumber = employeeNumber
ORDER BY 
    employeeNumber;
```

<img src = "https://i.imgur.com/3w51072.png">

#### 2. `RIGHT JOIN` với `IS NULL`

Truy vấn ra các nhân viên không phụ trách bất kí khách hàng nào.

```sql
SELECT 
    employeeNumber, 
    customerNumber
FROM
    customers
RIGHT JOIN employees ON 
    salesRepEmployeeNumber = employeeNumber
WHERE customerNumber IS NULL
ORDER BY employeeNumber;
```

<img src = "https://i.imgur.com/Xv6FwI6.png">

------------------------------------------------------------------------

## `CROSS JOIN`

### Cú pháp cơ bản

```sql
SELECT * FROM t1
CROSS JOIN t2;
```

### Cách hoạt động

`CROSS JOIN` sẽ kết hợp tất cả các hàng từ 2 bảng lại, trong đó, mỗi hàng là sự kết hợp của trong bảng đầu tiên với hàng
trong bảng thứ 2. Nếu mỗi bảng có `n` và `m` hàng tương ứng, tập kết quả sẽ có `n x m` hàng.

`CROSS JOIN` không sử dụng mệnh đề `ON` và `USING`.

Trong trường hợp bảng t1 và t2 có quan hệ với nhau, `CROSS JOIN` làm việc giống như là `INNER JOIN`.

```sql
SELECT * FROM t1
CROSS JOIN t2
WHERE t1.id = t2.id;
```

### Ví dụ về cách sử dụng

Chuẩn bị 1 số bảng để tìm hiểu cách `CROSS JOIN` hoạt động.

Cài đặt 1 số bảng để test:
Tạo 1 database mới `salesdb`:

```sql
CREATE DATABASE IF NOT EXISTS salesdb;
```

Tạo 1 vài bảng sau:

```sql
CREATE TABLE products (
    id INT PRIMARY KEY AUTO_INCREMENT,
    product_name VARCHAR(100),
    price DECIMAL(13,2 )
);
 
CREATE TABLE stores (
    id INT PRIMARY KEY AUTO_INCREMENT,
    store_name VARCHAR(100)
);
 
CREATE TABLE sales (
    product_id INT,
    store_id INT,
    quantity DECIMAL(13 , 2 ) NOT NULL,
    sales_date DATE NOT NULL,
    PRIMARY KEY (product_id , store_id),
    FOREIGN KEY (product_id)
        REFERENCES products (id)
        ON DELETE CASCADE ON UPDATE CASCADE,
    FOREIGN KEY (store_id)
        REFERENCES stores (id)
        ON DELETE CASCADE ON UPDATE CASCADE
);
```

3 bảng như sau:

- products(id, product_name, price) : thông tin về sản phẩm
- stores(id, store_name) : thông tin các cửa hàng bán sản phẩm
- sales(product_id, store_id, quantity, sales_date) : các sản phẩm được bán trong một cửa hàng cụ thể theo số lượng và
  ngày.

Nhập 1 vài dữ liệu cho các bảng:

```sql
INSERT INTO products(product_name, price)
VALUES('iPhone', 699),
      ('iPad',599),
      ('Macbook Pro',1299);
 
INSERT INTO stores(store_name)
VALUES('North'),
      ('South');
 
INSERT INTO sales(store_id,product_id,quantity,sales_date)
VALUES(1,1,20,'2017-01-02'),
      (1,2,15,'2017-01-05'),
      (1,3,25,'2017-01-05'),
      (2,1,30,'2017-01-02'),
      (2,2,35,'2017-01-05');
```

Bảng stores:

<img src = "https://i.imgur.com/71Mcl3t.png">

Bảng products:

<img src = "https://i.imgur.com/o5PA6T3.png">

`CROSS JOIN` 2 bảng stores và products:

```sql
SELECT 
    store_name,
    product_name
FROM
    stores CROSS JOIN products;
```

<img src = "https://i.imgur.com/fgjdfJC.png">

------------------------------------------------------------------------

## `Self Join`

### Cơ bản về Self Join

MySQL Self Join sẽ thêm 1 bảng vào chính nó sử dụng `INNER JOIN` và `LEFT JOIN`.

Self Join được sử dụng để truy vấn dữ liệu phân cấp hoặc để so sánh một hàng với các hàng khác trong cùng 1 bảng.

**Lưu ý:** Để thực hiện Self Join, bạn phải sử dụng bí danh bảng để quá trình thực hiện không bị lỗi do lặp lại tên bảng
2 lần trong 1 truy vấn.

### Ví dụ về cách sử dụng

Sử dụng bảng `employees`:

<img src = "https://i.imgur.com/KWTyRMo.png">

Bảng này lưu trữ không chỉ dữ liệu nhân viên mà còn có id của người quản lí nhân viên đó, được xác định bởi
cột `reportsTo`.

#### 1. Self Join sử dụng `INNER JOIN`

```sql
SELECT 
    CONCAT(m.lastName, ', ', m.firstName) AS Manager,
    CONCAT(e.lastName, ', ', e.firstName) AS 'Direct report'
FROM
    employees e
INNER JOIN employees m ON 
    m.employeeNumber = e.reportsTo
ORDER BY 
    Manager;
```

<img src = "https://i.imgur.com/3TYVvlE.png">

Đầu ra kết quả chỉ cho ra những nhân viên có người quản lí.

#### 2. Self Join sử dụng `LEFT JOIN`

Để ra được cả nhân viên không có quản lí. Ta sử dụng `LEFT JOIN`

```sql
SELECT 
    IFNULL(CONCAT(m.lastname, ', ', m.firstname),
            'Top Manager') AS 'Manager',
    CONCAT(e.lastname, ', ', e.firstname) AS 'Direct report'
FROM
    employees e
LEFT JOIN employees m ON 
    m.employeeNumber = e.reportsto
ORDER BY 
    manager DESC;
```

<img src = "https://i.imgur.com/bPPoWTy.png">

3. Self Join dùng để so sánh các hàng với nhau

Hiển thị danh sách khách hàng định vị trong cùng thành phố bằng cách self join bảng `customers` với chính nó.

```sql
SELECT 
    c1.city, 
    c1.customerName, 
    c2.customerName
FROM
    customers c1
INNER JOIN customers c2 ON 
    c1.city = c2.city
    AND c1.customername > c2.customerName
ORDER BY 
    c1.city;
```

<img src = "https://i.imgur.com/njtw7LM.png">

------------------------------------------------------------------------

## `GROUP BY`

Trong bài này, ta sẽ học cách sử dụng `GROUP BY` để nhóm các hàng thành các nhóm con dựa trên các giá trị của cột hay
biểu thức.

### Chức năng

`GROUP BY` nhóm một tập hợp các hàng với nhau theo các giá trị của cột hoặc biểu thức. `GROUP BY` trả về một hàng cho
mỗi nhóm. Nói cách khác, nó làm giảm số lượng hàng trong tập kết quả

### Cú pháp

```sql
SELECT 
    c1, c2,..., cn, aggregate_function(ci)
FROM
    table
WHERE
    where_conditions
GROUP BY c1 , c2,...,cn;
```

Mệnh đề `GROUP BY` phải xuất hiện sau mệnh đề `FROM` và `WHERE`. Theo sau các từ khóa `GROUP BY` là danh sách các cột
hoặc biểu thức được phân tách bằng dấu phẩy mà bạn muốn sử dụng làm tiêu chí cho các hàng nhóm.

### Thứ tự đánh giá của SQL

<img src="https://i.imgur.com/e9DNEE0.png">

### Ví dụ

#### 1. `GROUP BY` đơn giản

Ta sử dụng bảng `orders`

<img src="https://i.imgur.com/o4i0zSz.png">

Ta muốn nhóm các giá trị của trạng thái đơn hàng (`status`) thành các nhóm con.

```sql
SELECT status
FROM 
    orders
GROUP BY status;
```

**Kết quả:**

<img src="https://i.imgur.com/kexDk87.png">

Ta thấy `GROUP BY` trả về các trạng thái có trong bảng. Nó làm việc giống `DISTINCT` trong câu truy vấn sau:

```sql
SELECT DISTINCT
    status
FROM
    orders;
```

#### 2. `GROUP BY` với các hàm tổng hợp

Các hàm tổng hợp cho phép bạn thực hiện tính toán một tập hợp các hàng và trả về một giá trị duy nhất.

`GROUP BY` thường được sử dụng với hàm tổng hợp để tính toán và trả về giá trị duy nhất cho các nhóm con.

Ví dụ, ta muốn lấy số lượng đơn hàng ở mỗi trạng thái, ta sử dụng `COUTN` với `GROUP BY`  như sau:

```sql
SELECT 
    status, COUNT(*)
FROM
    orders
GROUP BY status;
```

**Kết quả:**

<img src="https://i.imgur.com/oxy6tfS.png">

Ví dụ khác, ta xem 2 bảng `orders` và `orderdetails`

<img src="https://i.imgur.com/866AS8W.png">

Bây giờ ta muốn tính toán tổng tiền của mỗi trạng thái đơn hàng. Ta làm như sau:

```sql
SELECT 
    status, 
    SUM(quantityOrdered * priceEach) AS amount
FROM
    orders
INNER JOIN orderdetails
    USING (orderNumber)
GROUP BY 
    status;
```

**Kết quả:**

<img src="https://i.imgur.com/pQGUqh2.png">

#### 3. `GROUP BY` với giá trị biểu thức

Ngoài các cột, bạn có thể nhóm các hàng theo biểu thức. Các truy vấn sau đây có được tổng doanh số cho mỗi năm.

```sql
SELECT 
    YEAR(orderDate) AS year,
    SUM(quantityOrdered * priceEach) AS total
FROM
    orders
INNER JOIN orderdetails 
    USING (orderNumber)
WHERE
    status = 'Shipped'
GROUP BY 
    YEAR(orderDate);
```

**Kết quả:**

<img src="https://i.imgur.com/CZaHQRX.png">

`YEAR(orderDate)` dùng để trích xuất dữ liệu năm từ `orderDate` để truy vấn dữ liệu theo năm.

------------------------------------------------------------------------

## `HAVING`

### Chức năng

Mệnh đề MySQL `HAVING` để chỉ định điều kiện lọc cho các nhóm hàng hoặc tổng hợp.

### Cú pháp

```sql
SELECT 
    select_list
FROM 
    table_name
WHERE 
    search_condition
GROUP BY 
    group_by_expression
HAVING 
    group_condition;
```

**Lưu ý:** mệnh đề `HAVING` áp dụng điều kiện lọc cho từng nhóm hàng, trong khi mệnh đề `WHERE` áp dụng điều kiện lọc
cho từng hàng riêng lẻ.

### Thứ tự đánh giá trong SQL

<img src="https://i.imgur.com/lu0SVwx.png">

### Ví dụ

Sử dụng bảng `orderdetails`

<img src="https://i.imgur.com/OOiUc7H.png">

- Sử dụng `GROUP BY` để lấy số thứ tự, số lượng mặt hàng được bán cho mỗi đơn hàng và tổng doanh số cho mỗi sản phẩm từ
  bảng `orderdetails`

    ```sql
    SELECT 
        ordernumber,
        SUM(quantityOrdered) AS itemsCount,
        SUM(priceeach*quantityOrdered) AS total
    FROM
        orderdetails
    GROUP BY ordernumber;
    ```

<img src="https://i.imgur.com/PfUQqAe.png">

- Bây giờ ta có thể tìm các đơn hàng có tổng doanh số lớn hơn 1000 bằng cách sử dụng `HAVING`
    ```sql
    SELECT 
        ordernumber,
        SUM(quantityOrdered) AS itemsCount,
        SUM(priceeach*quantityOrdered) AS total
    FROM
        orderdetails
    GROUP BY 
        ordernumber
    HAVING 
        total > 1000;
    ```

**Kết quả:**

<img src="https://i.imgur.com/o70dGfj.png">

- Bạn có thể xây dựng một điều kiện phức tạp trong mệnh đề `HAVING` bằng các toán tử logic như `OR` và `AND`

  Tìm các đơn hàng có tổng số tiền lớn hơn 1000 và chứa hơn 600 mặt hàng
    ```sql
    SELECT 
        ordernumber,
        SUM(quantityOrdered) AS itemsCount,
        SUM(priceeach*quantityOrdered) AS total
    FROM
        orderdetails
    GROUP BY ordernumber
    HAVING 
        total > 1000 AND 
        itemsCount > 600;
    ```

**Kết quả**

<img src="https://i.imgur.com/3ungjgA.png">

- Giả sử bạn muốn tìm tất cả các đơn đặt hàng ở trạng thái giao hàng và có tổng số tiền lớn hơn 1500, bạn có thể `JOIN`
  bảng `orderdetails` với bảng `orders` bằng cách sử dụng mệnh đề `INNER JOIN` và áp dụng một điều kiện trên
  cột `status` và `total` như trong truy vấn sau
    ```sql
    SELECT 
        a.ordernumber, 
        status, 
        SUM(priceeach*quantityOrdered) total
    FROM
        orderdetails a
    INNER JOIN orders b 
        ON b.ordernumber = a.ordernumber
    GROUP BY  
        ordernumber, 
        status
    HAVING 
        status = 'Shipped' AND 
        total > 1500;
    ```

**Kết quả:**

<img src="https://i.imgur.com/jFme8ki.png">

------------------------------------------------------------------------

## `ROLLUP`

Cách sử dụng mệnh đề MySQL `ROLLUP` để tạo tổng phụ và tổng lớn.

### Tạo bảng mẫu

- Đoạn truy vấn dưới đây tạo ra bảng mới tên là `sales`, nó lưu trữ các giá trị đơn hàng được tóm tắt theo dòng sản phẩm
  và năm. Dữ liệu đến từ các bảng `products`, `orders` và `orderDetails` trong database mẫu
    ```sql
    CREATE TABLE sales
    SELECT
        productLine,
        YEAR(orderDate) orderYear,
        SUM(quantityOrdered * priceEach) orderValue
    FROM
        orderdetails
            INNER JOIN
        orders USING (orderNumber)
            INNER JOIN
        products USING (productCode)
    GROUP BY
        productLine ,
        YEAR(orderDate);
    ```

- Thử truy vấn kết quả bảng `sales` sau khi tạo
    ```sql
    SELECT * FROM sales;
    ```

    <img src="https://i.imgur.com/2my9CiL.png">

### Tổng quan về `ROLLUP`

Groupong set là tập hợp các cột mà bạn muốn nhóm.

- Query dưới đây tạo ra 1 Grouping set được biểu thị bởi `productline`
    ```sql
    SELECT 
        productline, 
        SUM(orderValue) totalOrderValue
    FROM
        sales
    GROUP BY 
        productline;
    ```

    <img src="https://i.imgur.com/fMIXqod.png">

- Query dưới đây tạo 1 Grouping set trống được kí hiệu là `()`
    ```sql
    SELECT 
        SUM(orderValue) totalOrderValue
    FROM
        sales;
    ```

    <img src="https://i.imgur.com/HD4pwdO.png">

- Nếu muốn tạo 2 hay nhiều Grouping set trong cùng 1 câu truy vấn, bạn có thể sử dụng toán tử `UNION ALL` như sau:
    ```sql
    SELECT 
        productline, 
        SUM(orderValue) totalOrderValue
    FROM
        sales
    GROUP BY 
        productline 
    UNION ALL
    SELECT 
        NULL, 
        SUM(orderValue) totalOrderValue
    FROM
        sales;
    ```

    <img src="https://i.imgur.com/zFVZTD3.png">

- `UNION ALL` yêu cầu các câu truy vấn phải có cùng số cột, ta thêm cột `NULL` để thỏa mãn yêu cầu này.

Những truy vấn này có thể tạo ra tổng giá trị đơn hàng theo dòng sản phẩm và cả tổng lớn. Tuy nhiên, nó có 1 số vấn đề
sau:

1. Các câu truy vấn khá dài
2. Hiệu năng truy vấn có thể không tốt vì phải thực hiện bên trong 2 truy vấn riêng biệt và kết hợp các tập kết quả
   thành một.

Chính vì vậy, ta sẽ sử dụng `ROLLUP`.

#### Cú pháp

- `ROLLUP` là phần mở rộng của mệnh đề `GROUP BY` với cú pháp sau:
    ```sql
    SELECT 
        select_list
    FROM
        table_name
    GROUP BY 
        c1, c2, c3, WITH ROLLUP;
    ```

- `ROLLUP` tạo ra nhiều Grouping set dựa trên các cột hoặc biểu thức được chỉ định trong mệnh đề `GROUP BY`

#### Ví dụ với bảng ta vừa tạo ở trên

- Xem truy vấn sau:
    ```sql
    SELECT 
        productLine, 
        SUM(orderValue) totalOrderValue
    FROM
        sales
    GROUP BY 
        productline WITH ROLLUP;
    ```

    <img src="https://i.imgur.com/taGwuFU.png">

- `ROLLUP` tạo ra các tổng phụ và kèm với tổng chính giá trị các đơn hàng.

- Nếu bạn có nhiều hơn 1 cột được chỉ định trong mệnh đề `GROUP BY`, mệnh đề `ROLLUP` giả định một hệ thống phân cấp
  giữa các cột đầu vào.

#### Ví dụ về phân cấp trong `ROLLUP`

- Ví dụ
    ```sql
    GROUP BY c1, c2, c3 WITH ROLLUP
    ```

- `ROLLUP` sẽ giả định có phân cấp sau
    ```sql
    c1 > c2 > c3
    ```

- Và nó sẽ tạo ra các nhóm sau
    ```sql
    (c1, c2, c3)
    (c1, c2)
    (c1)
    ()
    ```

- **Xem query dưới đây đối với database mẫu**
    ```sql
    SELECT 
        productLine, 
        orderYear,
        SUM(orderValue) totalOrderValue
    FROM
        sales
    GROUP BY 
        productline, 
        orderYear 
    WITH ROLLUP;
    ```

    <img src="https://i.imgur.com/rgxppDv.png">

- Ta thấy `ROLLUP` sẽ tạo các tổng khi thay đổi dòng sản phẩm và tổng chính khi đã hết các dòng sản phẩm.

- Hệ thống phân cấp trong trường hợp này là
    ```sql
    productLine > orderYear
    ```
  
------------------------------------------------------------------------

## `SUBQUERY`

Trong bài này, ta sẽ tìm hiểu cách sử dụng subquery để viết các truy vấn phức tạp và giải thích khái niệm ý tưởng subquery.

Subquery là 1 truy vấn được lồng trong 1 truy vấn khác, chẳng hạn như `SELECT`, `INSERT`, `UPDATE`, `DELETE`. Ngoài ra, một subquery có thể được lồng bên trong một subquery khác.

#### Ví dụ
Ví dụ dưới đây trả về các nhân viên làm việc tại các văn phòng ở USA:
```sql
SELECT 
    lastName, firstName
FROM
    employees
WHERE
    officeCode IN (SELECT 
            officeCode
        FROM
            offices
        WHERE
            country = 'USA');
```

<img src="https://i.imgur.com/lkhpa5x.png">

Trong ví dụ, ta thấy:
- subquery trả về tất cả các mã văn phòng của các văn phòng tại USA.
- Truy vấn ngoài chọn họ và tên của nhân viên làm việc trong văn phòng có mã văn phòng nằm trong tập kết quả được trả về từ subquery

<img src="https://i.imgur.com/qqxLgOU.png">

Khi truy vấn được thực thi, truy vấn con chạy trước và trả về tập kết quả. Sau đó, tập kết quả này được sử dụng làm đầu vào cho truy vấn bên ngoài.

### 1. Subquery trong mệnh đề `WHERE`
Ta sử dụng bảng `payments`:

<img src="https://i.imgur.com/BTtkVLy.png">

#### 1.1. Subquery với các toán tử so sánh
- Ví dụ: Truy vấn sau trả về kết quả khách hàng có khoản thanh toán tối đa
    ```sql
    SELECT 
        customerNumber, 
        checkNumber,
        amount
    FROM
        payments
    WHERE
        amount = (SELECT MAX(amount) FROM payments);
    ```

    <img src="https://i.imgur.com/zKRxTkQ.png">

#### 1.2. Subquery với các toán tử `IN` `NOT IN`
Nếu truy vấn con trả về nhiều hơn một giá trị, bạn có thể sử dụng các toán tử khác như toán tử `IN` hoặc `NOT IN` trong mệnh đề `WHERE`.

Xem bảng `customers` và `orders` sau:

<img src="https://i.imgur.com/isZyQX7.png">

Ví dụ dưới đây, ta sử dụng subquery `NOT IN` để tìm những khách hàng chưa đặt hàng như sau:
```sql
SELECT customerName
FROM 
    customers
WHERE
    customerNumber NOT IN (SELECT DISTINCT
                                customerNumber
                            FROM
                                orders);
```

<img src="https://i.imgur.com/Fjht6YE.png">

### 2. Subquery trong mệnh đề FROM
- Khi sử dụng subquery với mệnh đề FROM, kết quả trả về được sử dụng như là 1 bảng tạm thời. Bảng này được gọi là bảng dẫn xuất hoặc subquery cụ thể.

- Truy vấn dưới đây tìm số lượng mặt hàng tối đa, tối thiểu và trung bình trong các đơn đặt hàng
    ```sql
    SELECT 
        MAX(items),
        MIN(items),
        FLOOR(AVG(items))
    FROM 
        (SELECT
            orderNumber, COUNT(orderNumber) AS items
        FROM
            orderdetails
        GROUP BY 
            orderNumber
        ) AS lineitems;
    ```

    <img src="https://i.imgur.com/AA9uJaL.png">

  `FLOOR()` được sử dụng để xóa các số thập phân sau dấu phẩy.

------------------------------------------------------------------------

## `DERIVED TABLE`

**Derived Table** : Bảng dẫn xuất

Trong bài này, ta sẽ tìm hiểu bảng dẫn xuất trong MySQL và cách sử dụng nó để đơn giản hóa các truy vấn phức tạp.

### 1. Giới thiệu về Derived Table
Derived Table là bảng ảo được trả về từ câu lệnh `SELECT`. Một bảng dẫn xuất tương tự 1 bảng tạm thời, nhưng sử dụng bảng dẫn xuất trong câu lệnh `SELECT` đơn giản hơn nhiều so với bảng tạm thời vì nó không yêu cầu các bước tạo bảng tạm thời.

Thuật ngữ bảng dẫn xuất và truy vấn con thường được sử dụng thay thế cho nhau. Khi một truy vấn con độc lập được sử dụng trong mệnh đề `FROM` của câu lệnh `SELECT`. Nó được gọi là bảng dẫn xuất.

Hình dưới đây minh họa một truy vấn sử dụng bảng dẫn xuất:

<img src="https://i.imgur.com/5HRpeVX.png">

**Lưu ý:** truy vấn con độc lập là truy vấn con có thể thực thi độc lập với câu lệnh chứa nó

Không giống với subquery, bảng dẫn xuất phải có bí danh (alias) để bạn có thể tham chiếu tên của nó sau này trong truy vấn.

Ví dụ sử dụng bảng dẫn xuất:
```sql
SELECT 
    column_list
FROM
    (SELECT 
        column_list
    FROM
        table_1) derived_table_name;
WHERE derived_table_name.c1 > 0;
```

### 2. Ví dụ
Truy vấn sau đây nhận được 5 sản phẩm hàng đầu theo doanh thu bán hàng trong năm 2003 từ các bảng `orders` và bảng `orderdetails` trong cơ sở dữ liệu mẫu:

<img src="https://i.imgur.com/qLO4bhY.png">

```sql
SELECT 
    productCode, 
    ROUND(SUM(quantityOrdered * priceEach)) sales
FROM
    orderdetails
        INNER JOIN
    orders USING (orderNumber)
WHERE
    YEAR(shippedDate) = 2003
GROUP BY productCode
ORDER BY sales DESC
LIMIT 5;
```

<img src="https://i.imgur.com/f9RKbp4.png">

Bạn có thể sử dụng kết quả của truy vấn này dưới dạng bảng dẫn xuất và nối nó với bảng `products` như sau:

<img src="https://i.imgur.com/yoiNqNN.png">

```sql
SELECT 
    productName, sales
FROM
    (SELECT 
        productCode, 
        ROUND(SUM(quantityOrdered * priceEach)) sales
    FROM
        orderdetails
    INNER JOIN orders USING (orderNumber)
    WHERE
        YEAR(shippedDate) = 2003
    GROUP BY productCode
    ORDER BY sales DESC
    LIMIT 5) top5products2003
INNER JOIN
    products USING (productCode);
```

<img src="https://i.imgur.com/HrLGXDx.png">

Trong ví dụ:

1. Truy vấn con được thực thi để tạo tập kết quả hoặc bảng dẫn xuất
2. Sau đó, truy vấn bên ngoài được thực thi đã join với bảng dẫn xuất `top5products2003` với bảng `products` sử dụng cột `productCode`

------------------------------------------------------------------------

## `EXISTS`

Trong bài này, ta sẽ học cách sử dụng toán tử `EXISTS` và khi nào nên sử dụng nó để cải thiện hiệu năng của các truy vấn.

### 1. Giới thiệu về `EXISTS`
`EXISTS` là toán tử Boolean trả về đúng hoặc sai. `EXISTS` thường được sử dụng để kiểm tra sự tồn tại của các hàng được trả về từ subquery

#### Cấu trúc câu truy vấn
```sql
SELECT 
    select_list
FROM
    a_table
WHERE
    [NOT] EXISTS(subquery);
```

Nếu subquery trả về ít nhất một hàng, toán tử `EXISTS` trả về **True**, ngược lại nó trả về **False**

Ngoài ra, toán tử `EXISTS` chấm dứt quá trình xử lí ngay lập tức khi tìm thấy 1 hàng khớp, nó giúp cải thiện hiệu suất của truy vấn.

Toán tử `NOT` phủ định toán tử `EXISTS`. Nói cách khác, `NOT EXISTS` trả về **True** nếu truy vấn con không trả về hàng nào, ngược lại nó trả về **False**.

### 2. Ví dụ
#### 2.1. Ví dụ về `SELECT EXISTS`
Xem mối quan hệ 2 bảng `customers` và `orders`

<img src="https://i.imgur.com/MTGbMci.png">

Sử dụng toán tử `EXISTS` để tìm khách hàng có ít nhất một đơn hàng:
```sql
SELECT 
    customerNumber, 
    customerName
FROM
    customers
WHERE
    EXISTS(SELECT 
                1
            FROM
                orders
            WHERE
                orders.customernumber 
                = customers.customernumber);
```

<img src="https://i.imgur.com/NBNru1B.png">

Trong ví dụ này, đối với mỗi hàng trong bảng `customers`, truy vấn sẽ kiểm tra số khách hàng trong bảng `orders`. Nếu `customerNumber` xuất hiện trong bảng `customers` tồn tại trong bảng `order`, truy subquery trả về hàng khớp đầu tiên. Do đó, toán tử `EXISTS` trả về **True** và dừng kiểm tra bảng `orders`. Mặt khác, subquery không trả về hàng nào và toán tử `EXISTS` trả về **False**

Ví dụ sau sử dụng toán tử `NOT EXISTS` để tìm các khách hàng không có bất kì đơn hàng nào:
```sql
SELECT 
    customerNumber, 
    customerName
FROM
    customers
WHERE
    NOT EXISTS( 
            SELECT 
                1
            FROM
                orders
            WHERE
                orders.customernumber = customers.customernumber
    );
```

<img src="https://i.imgur.com/JmS7B6R.png">

#### 2.2. Ví dụ về `UPDATE EXISTS`
Giả sử bạn phải cập nhật các tiện ích mở rộng trên điện thoại của các nhân viên làm việc tại văn phòng San Francisco.

- Truy vấn dưới đây tìm ra những nhân viên làm việc tại văn phòng San Francisco:
    ```sql
    SELECT 
        employeenumber, 
        firstname, 
        lastname, 
        extension
    FROM
        employees
    WHERE
        EXISTS( 
            SELECT 
                1
            FROM
                offices
            WHERE
                city = 'San Francisco' AND 
                offices.officeCode = employees.officeCode
        );
    ```

<img src="https://i.imgur.com/NsyoM50.png">

- Truy vấn sau, thêm số `1` vào phần mở rộng điện thoại của nhân viên làm việc tại văn phòng ở San Francisco
    ```sql
    UPDATE employees 
    SET 
        extension = CONCAT(extension, '1')
    WHERE
        EXISTS( 
            SELECT 
                1
            FROM
                offices
            WHERE
                city = 'San Francisco'
                AND offices.officeCode = employees.officeCode
        );
    ```

  **Cách hoạt động:**
    - Đầu tiên, toán tử `EXISTS` trong mệnh đề `WHERE` chỉ nhận các nhân viên làm việc tại văn phòng San Francisco
    - Sau đó, hàm `CONCAT()` nối phần mở rộng điện thoại với `1`

### 2.3. Ví dụ về `INSERT EXISTS`
Giả sử bạn muốn lưu trữ những khách hàng không có đơn đặt hàng trong một bảng riêng biệt. Để làm điều này, bạn sử dụng các bước sau:

1. Đầu tiên, tạo một bảng mới để lưu trữ khách hàng bằng cách sao chép cấu trúc từ bảng khách hàng:
    ```sql
    CREATE TABLE customers_archive 
    LIKE customers;
    ```

2. Thêm khách hàng không có bất kì đơn hàng nào vào bảng `customers_archive` bằng cách sử dụng `INSERT`
    ```sql
    INSERT INTO customers_archive
    SELECT * 
    FROM customers
    WHERE NOT EXISTS( 
        SELECT 1
        FROM
            orders
        WHERE
            orders.customernumber = customers.customernumber
    );
    ```

3. Query data từ bảng `customers_archive` để kiểm tra lại:
    ```sql
    SELECT * FROM customers_archive;
    ```

    <img src="https://i.imgur.com/M1yJxo8.png">

#### 2.4. Ví dụ về `DELETE EXISTS`
Một việc cuối cùng trong việc lưu trữ dữ liệu khách hàng là xóa các khách hàng tồn tại trong bảng `customers_archive` từ bảng `customers`.

Để làm việc đó, ta sử dụng toán tử `EXISTS` trong mệnh đề `WHERE` của câu lệnh `DELETE` như sau:
```sql
DELETE FROM customers
WHERE EXISTS( 
    SELECT 
        1
    FROM
        customers_archive a
    
    WHERE
        a.customernumber = customers.customerNumber);
```

------------------------------------------------------------------------

## UNION

Nếu bạn cần viết hai câu truy vấn `SELECT` khác nhau nhưng bạn muốn nó trả về một danh sách kết quả duy nhất thì bạn phải sử dụng toán tử `UNION`. Toán tử này cũng ít khi sử dụng nhưng cũng nên tìm hiểu vì biết đâu sau này cần.

Toán tử UNION cho phép bạn nối kết quả của hai hoặc nhiều câu truy vấn lại với nhau để trở thành một danh sách kết quả duy nhất. Cú pháp của MySQL `UNION` như sau:

```sql
SELECT column_list
UNION [DISTINCT | ALL]
SELECT column_list
UNION [DISTINCT | ALL]
SELECT column_list
...
```

Tuy nhiên khi sử dụng `UNION` trong MySQL chúng ta cần phải tuân thủ những nguyên tắc sau đây:

- Số lượng colums trong tất cả các lệnh `SELECT` phải bằng nhau
- Mỗi column tương ứng vị trí phải có cùng kiểu dữ liệu và độ dài

Theo mặc định thì UNION sẽ loại bỏ các kết quả trùng lặp của các câu SELECT nên nó tạo cho chúng ta hai lựa chọn sau:

- Nếu chọn `UNION DISTINCT`thì nó sẽ loại bỏ kết quả trùng.
- Nếu chọn `UNION ALL` thì nó giữ lại kết quả trùng.
- Nếu bạn không chọn gì thì mặc định nó sẽ lấy `UNION DISTINCT`

Ví dụ:

![Imgur](https://i.imgur.com/PRF3kvd.png)

Giả sử bạn muốn kết hợp tên và họ nhân viên thành một set với UNION, làm như sau:

```sql
SELECT 
    firstName, 
    lastName
FROM
    employees 
UNION 
SELECT 
    contactFirstName, 
    contactLastName
FROM
    customers;
```

![Imgur](https://i.imgur.com/Z22dbq1.png)

Sử dụng alias cột với ví dụ như trên
```sql
SELECT 
    CONCAT(firstName,' ',lastName) fullname
FROM
    employees 
UNION SELECT 
    CONCAT(contactFirstName,' ',contactLastName)
FROM
    customers;
``` 
![Imgur](https://i.imgur.com/zIoNPew.png)

Ví dụ sử dụng kết hợp với`ORDER BY`
```sql
SELECT 
    concat(firstName,' ',lastName) fullname
FROM
    employees 
UNION SELECT 
    concat(contactFirstName,' ',contactLastName)
FROM
    customers
ORDER BY fullname;
```

![Imgur](https://i.imgur.com/PEMau7p.png)

Thêm một cột:

```sql
SELECT 
    CONCAT(firstName, ' ', lastName) fullname, 
    'Employee' as contactType
FROM
    employees 
UNION SELECT 
    CONCAT(contactFirstName, ' ', contactLastName),
    'Customer' as contactType
FROM
    customers
ORDER BY 
    fullname
```

![Imgur](https://i.imgur.com/vuyZ9iX.png)

------------------------------------------------------------------------

## INSERT

Cú pháp:
```sql
INSERT INTO table(c1,c2,...)
VALUES 
   (v11,v12,...),
   (v21,v22,...),
    ...
   (vnn,vn2,...);
```

Trong đó:

- Đầu tiên, chỉ định tên bảng và danh sách các cột được phân tách bằng dấu phẩy bên trong dấu ngoặc đơn sau mệnh đề `INSERT INTO`.
- Sau đó, đặt danh sách các giá trị được phân tách bằng dấu phẩy của các cột tương ứng bên trong dấu ngoặc đơn theo từ khóa `VALUES` .

Lưu ý trước ddoss phải tạo bảng

Ví dụ tạo bảng mới tên tasks

```sql
CREATE TABLE IF NOT EXISTS tasks (
    task_id INT AUTO_INCREMENT,
    title VARCHAR(255) NOT NULL,
    start_date DATE,
    due_date DATE,
    priority TINYINT NOT NULL DEFAULT 3,
    description TEXT,
    PRIMARY KEY (task_id)
);
```

Ví dụ đơn giản:
```sql
    INSERT INTO tasks(title,priority)
    VALUES('Learn MySQL INSERT Statement',1);
```

    SELECT * FROM tasks;

![Imgur](https://i.imgur.com/zMDlgIB.png)

Ví dụ chèn ngày tháng năm

Định dạng `'YYYY-MM-DD'`
```sql
INSERT INTO tasks(title, start_date, due_date)
VALUES('Insert date into table','2018-01-09','2018-09-15');
```

    SELECT * FROM tasks;

![Imgur](https://i.imgur.com/zVkQyol.png)

### INSERT INTO SELECT

Cú pháp minh họa:
```sql
INSERT INTO table_name(column_list)
SELECT 
   select_list 
FROM 
   another_table
WHERE
   condition;
```

Ví dụ tạo bảng suppliers
```sql
CREATE TABLE suppliers (
    supplierNumber INT AUTO_INCREMENT,
    supplierName VARCHAR(50) NOT NULL,
    phone VARCHAR(50),
    addressLine1 VARCHAR(50),
    addressLine2 VARCHAR(50),
    city VARCHAR(50),
    state VARCHAR(50),
    postalCode VARCHAR(50),
    country VARCHAR(50),
    customerNumber INT,
    PRIMARY KEY (supplierNumber)
);
```

Giả sử các khách hàng ở CA trở thành người cung cấp

```sql
SELECT 
    customerNumber,
    customerName,
    phone,
    addressLine1,
    addressLine2,
    city,
    state,
    postalCode,
    country
FROM
    customers
WHERE
    country = 'USA' AND 
    state = 'CA';
```

![Imgur](https://i.imgur.com/bf8QyUR.png)

Thêm các khách hàng tử california đến bảng suppliers

```sql
INSERT INTO suppliers (
    supplierName, 
    phone, 
    addressLine1,
    addressLine2,
    city,
    state,
    postalCode,
    country,
    customerNumber
)
SELECT 
    customerName,
    phone,
    addressLine1,
    addressLine2,
    city,
    state ,
    postalCode,
    country,
    customerNumber
FROM 
    customers
WHERE 
    country = 'USA' AND 
    state = 'CA';
```

    SELECT * FROM suppliers;

![Imgur](https://i.imgur.com/f5dgFe4.png)

------------------------------------------------------------------------

## INSERT INTO

Thêm nội dung vào table

Cú pháp:

    INSERT INTO table_name (column1, column2, column3, ...)
    VALUES (value1, value2, value3, ...);

Nếu thêm vào tất cả các trường trong bảng thì dùng cú pháp

    INSERT INTO table_name
    VALUES (value1, value2, value3, ...);

Ví dụ:

Bảng Customers

![Imgur](https://i.imgur.com/V3AvKqw.png)

Thêm 1 khách hàng vào bảng

    INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
    VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');

Kết quả:

![Imgur](https://i.imgur.com/BsSyqUa.png)

Chỉ thêm 1 vài thông tin

    INSERT INTO Customers (CustomerName, City, Country)
    VALUES ('Cardinal', 'Stavanger', 'Norway');

Kết quả:

![Imgur](https://i.imgur.com/vRG0BAb.png)

------------------------------------------------------------------------

## UPDATE

Câu lệnh UPDATE dùng để sửa đổi dữ liệu hiện có trong một bảng.

Cú pháp:
```sql
UPDATE [LOW_PRIORITY] [IGNORE] table_name 
SET 
    column_name1 = expr1,
    column_name2 = expr2,
    ...
[WHERE
    condition];
```

Lưu ý rằng mệnh đề `WHERE` rất quan trọng mà bạn không nên quên. Đôi khi, bạn có thể muốn cập nhật chỉ một hàng; Tuy nhiên, bạn có thể quên mệnh đề `WHERE` và vô tình cập nhật tất cả các hàng của bảng.

MySQL hỗ trợ hai cách sửa đổi trong câu lệnh UPDATE:

- LOW_PRIORITY sẽ thực hiện câu lệnh UPDATE khi không có kết nối đọc dữ liệu từ bảng.
- IGNORE cho phép câu lệnh UPDATE tiếp tục cập nhật các hàng ngay cả khi xảy ra lỗi. Các hàng gây ra lỗi như xung đột khó a trùng lặp không được cập nhật.

Ví dụ:

Dùng bảng employees

![Imgur](https://i.imgur.com/Oh3AzmG.png)

Tìm email của Mary
```sql
SELECT 
    firstname, 
    lastname, 
    email
FROM
    employees
WHERE
    employeeNumber = 1056;
```

update địa chỉ email của Mary thành: patterson@classicmodelcars.com
```sql
UPDATE employees 
SET 
    email = 'mary.patterson@classicmodelcars.com'
WHERE
    employeeNumber = 1056;
```
Kiểm tra lại kết quả sau khi update

![Imgur](https://i.imgur.com/nEaKD1k.png)

------------------------------------------------------------------------

## DELETE

Cú pháp:
```sql
DELETE FROM table_name
WHERE condition;
```
Ví dụ:

![Imgur](https://i.imgur.com/Oh3AzmG.png)

Xóa nhân viên có officeNumber là 4

```sql
DELETE FROM employees 
WHERE
    officeCode = 4;
```

Xóa tất cả nhân viên:
```sql
    DELETE FROM employees;
```
Ví dụ sử dụng LIMIT

Ví dụ xóa 10 dòng đầu tiên trong bảng customers được sắp xếp theo cột customerName

```sql
DELETE FROM customers
ORDER BY customerName
LIMIT 10;
```

------------------------------------------------------------------------

## REPLACE

Cách sử dụng câu lệnh `REPLACE` của MySQL để chèn hoặc cập nhật dữ liệu.

Để xác định xem hàng mới đã tồn tại trong bảng, MySQL sử dụng chỉ số `PRIMARY KEY` hoặc `UNIQUE KEY`. Nếu bảng không có một trong các chỉ mục này, `REPLACE` hoạt động giống như một câu lệnh `INSERT`.

Cú pháp:
```sql
REPLACE [INTO] table_name(column_list)
VALUES(value_list);
```
Tạo một Table
```sql
CREATE TABLE cities (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    population INT NOT NULL
);
```
Thêm dữ liệu vào bảng
```sql
INSERT INTO cities(name,population)
VALUES('New York',8008278),
      ('Los Angeles',3694825),
      ('San Diego',1223405);
```
Xem lại

    SELECT * FROM cities;

![Imgur](https://i.imgur.com/xHbmJ4u.png)

Bây giờ cập nhật số dân của Los Angeles city thành 3696820.
```sql
    REPLACE INTO cities(id,population)
    VALUES(2,3696820);
```
Sau đó Query Table cities ra ta có như sau:

    SELECT * FROM cities;

![Imgur](https://i.imgur.com/pL8MuDj.png)

Giá trị trong cột name là NULL . Câu lệnh REPLACE hoạt động như sau:

- Đầu tiên, câu lệnh REPLACE đã cố gắng chèn một hàng mới vào các thành phố trong bảng. Việc chèn không thành công vì id 2 đã tồn tại trong bảng thành phố.
- Sau đó, câu lệnh REPLACE đã xóa hàng với id 2 và chèn một hàng mới có cùng id 2 và dân số 3696820. Vì không có giá trị nào được chỉ định cho cột tên, nên nó được đặt thành NULL.

Update 1 hàng

Cú pháp câu lệnh REPLACE:
```sql
REPLACE INTO table
SET column1 = value1,
    column2 = value2;
```

Câu lệnh này giống như câu lệnh UPDATE ngoại trừ từ khóa REPLACE. Ngoài ra, nó không có mệnh đề WHERE.

Ví dụ này sử dụng câu lệnh REPLACE để cập nhật dân số của thành phố Phoenix lên 1768980:
```sql
REPLACE INTO cities
SET id = 4,
    name = 'Phoenix',
    population = 1768980;
```

![Imgur](https://i.imgur.com/6S1PvJQ.png)

REPLACE sử dụng câu lệnh SELECT

Cú pháp:
```sql
REPLACE INTO table_1(column_list)
SELECT column_list
FROM table_2
WHERE where_condition;
```

Câu lệnh sau sử dụng câu lệnh `REPLACE INTO` để sao chép một hàng trong cùng một bảng:
```sql
REPLACE INTO 
    cities(name,population)
SELECT 
    name,
    population 
FROM 
   cities 
WHERE id = 1;
```

Kết quả:

    SELECT * FROM cities; 

![Imgur](https://i.imgur.com/C8ikzeP.png)

------------------------------------------------------------------------

## CONSTRAINT SQL

Constraint là những quy tắc được áp dụng trên các cột dữ liệu, trên bảng. Được sử dụng để kiểm tra tính hợp lệ của dữ liệu vào, đảm bảo tính chính xác, tính toàn vẹn của dữ liệu.

- NOT NULL: Sử dụng để đảm bảo dữ liệu của cột không được nhận giá trị NULL
  DEFAULT	Gán giá trị mặc định trong trường hợp dữ liệu của cột không được nhập vào hay không được xác định.
- UNIQUE: Sử dụng để đảm bảo dữ liệu của cột là duy nhất, không trùng lặp giá trị trên cùng 1 cột.
- PRIMARY KEY (Khóa chính):	Dùng để thiết lập khóa chính trên bảng, xác định giá trị trên tập các cột làm khóa chính phải là duy nhất, không được trùng lặp. Việc khai báo ràng buộc khóa chính yêu cầu các cột phải NOT NULL.
- FOREIGN KEY (Khóa ngoại):	Dùng để thiết lập khóa ngoại trên bảng, tham chiếu đến bảng khác thông qua giá trị của cột được liên kết. Giá trị của cột được liên kết phải là duy nhất trong bảng kia.
- CHECK:	Bảo đảm tất cả giá trị trong cột thỏa mãn điều kiện nào đó. Đây là hình thức sử dụng phổ biến để kiểm tra tính hợp lệ của dữ liệu (validate data)

Một số lưu ý đối với ràng buộc CHECK:

- Không thể định nghĩa trong VIEW
- Các điều kiện thiết lập phải tham chiếu đến cột trong cùng 1 bảng dùng để khai báo ràng buộc, không thể tham chiếu tới các cột ở bảng khác. Trường hợp muốn tham chiếu đến bảng khác thì có thể dùng Function để trích xuất dữ liệu.
- Không thể sử dụng subquery (truy vấn con) trong định nghĩa điều kiện
- Chúng ta có thể khai báo ràng buộc trong câu lệnh CREATE TABLE (tạo mới bảng) hoặc ALTER TABLE (Sửa đổi bảng)

https://viblo.asia/p/rang-buoc-constraint-trong-sql-eW65GAnJZDO

Ví dụ:

**NOT NULLL**

Tạo, Sửa:

```sql
    CREATE TABLE Persons (
        ID int NOT NULL,
        LastName varchar(255) NOT NULL,
        FirstName varchar(255) NOT NULL,
        Age int
    );

    alter table test_table modify Age int not null;
```

**UNIQUE**

Tạo:

```sql
CREATE TABLE Persons (
    ID int NOT NULL UNIQUE,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int
);
```
Dùng với ALTER TABLE
Tạo
```sql
ALTER TABLE Persons
ADD UNIQUE (ID);
```
Đặt tên ràng buộc UNIQUE
```sql
ALTER TABLE Persons
ADD CONSTRAINT UC_Person UNIQUE (ID,LastName);
```

Xóa:
```sql
ALTER TABLE Persons
DROP INDEX UC_Person;
```
**PRIMARY KEY**

Tạo:

```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (ID)
);
```


Đặt tên cho khóa lúc tạo
```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT PK_Person PRIMARY KEY (ID,LastName)
);
```

Dùng với ALTER TABLE

Tạo:
```sql
ALTER TABLE Persons
ADD PRIMARY KEY (ID);
```
Đặt tên khóa chính:
```sql
ALTER TABLE Persons
ADD CONSTRAINT PK_Person PRIMARY KEY (ID,LastName);
```
Xóa khóa chính:
```sql
ALTER TABLE Persons
DROP PRIMARY KEY;
```


**FOREIGN KEY**

Tạo khóa ngoại lúc tạo bảng:

```sql
CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    PersonID int,
    PRIMARY KEY (OrderID),
    FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);
```

Đặt tên khóa ngoại:
```sql
CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    PersonID int,
    PRIMARY KEY (OrderID),
    CONSTRAINT FK_PersonOrder FOREIGN KEY (PersonID)
    REFERENCES Persons(ID)
);
```

Sử dụng với ALTER TABLE

Tạo khóa ngoại:
```sql
ALTER TABLE Orders
ADD FOREIGN KEY (PersonID) REFERENCES Persons(ID);
```

Đặt tên
```sql
ALTER TABLE Orders
ADD CONSTRAINT FK_PersonOrder
FOREIGN KEY (PersonID) REFERENCES Persons(ID);
```

Xóa khóa ngoại

```sql
ALTER TABLE Orders
DROP FOREIGN KEY FK_PersonOrder;
```
**CHECK**

Quan sát câu lệnh SQL sau sẽ tạo ràng buộc CHECK trên cột Age ngay khi bảng Persons được tạo ra. Ràng buộc CHECK đảm bảo rằng bạn sẽ không thể có bất kỳ người nào dưới 18 tuổi.

```SQL
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CHECK (Age>=18)
);
```
Đặt tên ràng buộc CHECK
```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255),
    CONSTRAINT CHK_Person CHECK (Age>=18 AND City='Sandnes')
);
```
Dùng với ALTER TABLE

Tạo:
```sql
ALTER TABLE Persons
ADD CHECK (Age>=18);
```

Đặt tên:
```sql
ALTER TABLE Persons
ADD CONSTRAINT CHK_PersonAge CHECK (Age>=18 AND City='Sandnes');
```
Xóa:
```sql
ALTER TABLE Persons
DROP CHECK CHK_PersonAge;
```
**DEFAULT**
Thêm ràng buộc mặc định, nếu không nhập tên thành phố thì sẽ hiển thị thành phố mặc định là Sandnes
```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255) DEFAULT 'Sandnes'
);
```
Dùng với ALTER TABLE
Tạo:
```sql
ALTER TABLE Persons
ALTER City SET DEFAULT 'Sandnes';
```
Xóa:
```sql
ALTER TABLE Persons
ALTER City DROP DEFAULT;
```

**INDEX**

Ràng buộc INDEX để người dùng truy vấn nhanh hơn

Tạo INDEX syntax

```
CREATE INDEX index_name
ON table_name (column1, column2, ...);
```
Tạo UNIQUE INDEX syntax
```
CREATE UNIQUE INDEX index_name
ON table_name (column1, column2, ...);
```
Ví dụ:
```sql
CREATE INDEX idx_lastname
ON Persons (LastName);
```

```sql
CREATE INDEX idx_pname
ON Persons (LastName, FirstName);
```
Xóa INDEX
```sql
ALTER TABLE table_name
DROP INDEX index_name;
```

#### AUTO INCREMENT Field

AUTO_INCREMENT nói nôm na có nghĩa là tăng tự động, có nghĩa là nếu bạn thiết lập một field nào đó là tăng tự động thì khi bạn thêm record mới bạn không cần phải truyền data cho nó và nó sẽ tự lấy giá trị lớn nhất tăng lên 1. Tuy nhiên không phải lúc nào nó cũng lấy giá trị lớn nhất mà sẽ tuân theo những tính chất sau đây:

- AUTO_INCREMENT chỉ thiết lập được cho kiểu INT và mỗi bảng chỉ có một field duy nhất, nghĩa là nếu bạn thiết lập 2 fields là AUTO_INCREMENT thì sẽ bị lỗi ngay.
  Khi bạn thêm dữ liệu nếu bạn có truyền data thì nó sẽ lấy data đó thay vì tăng tự động, ngược lại nó sẽ lấy giá trị lớn nhất hiện tại và tăng lên 1(giá trị lớn nhất này lưu trong config của table chứ không phải là id lớn nhất trong các records).
- Khi bạn xóa một record thì sẽ bị khuyết mất một giá trị, lúc này nếu bạn thêm thì nó sẽ không lấp vào vị trí này mà nó tuân theo quy luật trên.
- Giả sử giá trị 120 là lớn nhất, bạn xóa đi 120 thì lúc này lớn nhất là 119. Lúc này nếu ban thêm mới thì nó sẽ lấy 121 chứ không phải là 120 vì giá trị lớn nhất nó lưu trong config của table.
- Thông thường ta sử dụng AUTO_INCREMENT cho Primary Key khi viết ứng dụng website
- Mặc định AUTO_INCREMENT sẽ có giá trị đầu tiên là 1

Để tạo AUTO_INCREMENT thì ta thêm từ khóa AUTO_INCREMENT đằng sau field muốn tạo trong lệnh tạo bảng (Create Table). Thông thường chúng ta dùng cho khóa chính nên trong các ví dụ dưới đây tôi sử dụng cho field ID.

```sql
CREATE TABLE Users(
    id INT(11) NOT NULL PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(50) NOT NULL UNIQUE,
    email VARCHAR (50) NOT NULL UNIQUE
);
```

Thay đổi giá trị Auto_increment

```sql
ALTER TABLE Users AUTO_INCREMENT = 1000
```
