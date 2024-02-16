# So sánh giữ Dart và Swift

Dart và Swift là hai ngôn ngữ lập trình yêu thích của tôi, và bài viết này tôi sẽ só sánh điểm giống và khác nhau giữa Dart và Swift nhằm múc đích:

- Chỉ ra chi tiết các điểm khác biệt giữa 2 ngôn ngữ

- Để cho các bạn có thể chuyển từ ngôn ngữ này sang ngôn ngữ khác (hoặc sử dụng cả hai).

### Một số đinh nghĩa

- Dart thường được dùng cho [Flutter](https://flutter.dev/) (Một Framework của Google để xây dựng các ứng dụng native tuyệt đẹp chỉ bằng 1 mã duy nhất)

- Swift thường được dùng cho SDK của Apple để phát triển các ưng dụng trên IOS, macOS, tvOS và watchOS.

Các so sánh sau đây được thực hiện trên các tính năng chính của cả hai ngôn ngữ (từ Dart 2.1 và Swift 4.2) Khi có các phần liên quan đến từng tính năng chuyên sâu nằm ngoài phạm vi của bài viết này, tôi sẽ đính kèm các tài liệu tham khảo để các bạn có thể đọc thêm.

1. Bảng so sánh
--------------------------------------------------------------

![](table_comparison_dart_vs_swift.png)

2. Variables
--------------------------------------------------------------

### Variable declaration

Dart:

```java
String name;
int age;
double height;
```

Switf:

```Swift
var name = 'Andrea';
var age = 34;
var height = 1.84;
```

### Variable initialization

Dart:

```java
var name = 'Andrea';
var age = 34;
var height = 1.84;
```

Switf:

```Swift
var name = "Andrea"
var age = 34
var height = 1.84
```

3. Type inference
--------------------------------------------------------------

### Type inference

Có thể được viết như này trong Dart:

```java
var arguments = {'argA': 'hello', 'argB': 42}; // Map<String, Object>
```

Và kiểu của `arguments` sẽ tự động được định nghĩa bở compiler.

Trong Swift được viết tưng tự:

```swift
var arguments = [ "argA": "hello", "argB": 42 ] // [ String : Any ]
```

***Một số chi tiết***

[Dart documentation](https://www.dartlang.org/guides/language/sound-dart#type-inference):

> The analyzer can infer types for fields, methods, local variables, and most generic type arguments. When the analyzer doesn't have enough information to infer a specific type, it uses the dynamic type.

[Và của Swift](https://docs.swift.org/swift-book/ReferenceManual/Types.html):

> Swift uses type inference extensively, allowing you to omit the type or part of the type of many variables and expressions in your code. For example, instead of writing `var x: Int = 0`, you can write `var x = 0`, omitting the type completely---the compiler correctly infers that `x` names a value of type `Int`.

### Dynamic types

Một variable có thể là bất kỳ kiểu dữ liệu nào khi được khai báo với từ khóa `dynamic` với Dart và `Any` đối với Switf

Kiểu Dynamic thường được dùng khi đọc data từ SON

4. Mutable / immutable variables
--------------------------------------------------------------

Variables có thể được khai báo là ***mutable*** hoặc ***immutable***.

### Mutable

Khi khai báo variables kiểu Mutable, thì cả hai ngôn ngữ đều sử dụng từ khóa `var`

Dart

```java
var a = 10; // int
a = 20; // ok
```

Swift

```swift
var a = 10 // Int
a = 20 // ok
```

### Immutable

Khi khai báo variables kiểu Immutable, Dart sử dụng `final`, và Swift sử dụng `let`.

Dart

```java
final a = 10;
a = 20; // 'a': a final variable, can only be set once.
```

Swift

```swift
let a = 10
a = 20 // Cannot assign to value: 'a' is a 'let' constant
```

Trong [Dart documentation](https://www.dartlang.org/guides/language/language-tour#final-and-const) có định nghĩa hai từ khóa, `final` và `cost`, hoạt động như sau:

> If you never intend to change a variable, use final or const, either instead of var or in addition to a type. A final variable can be set only once; a const variable is a compile-time constant. (Const variables are implicitly final.) A final top-level or class variable is initialized the first time it’s used.

Và được giải thích kỹ hơn trong bài viết trên [website của Dart](https://news.dartlang.org/2012/06/const-static-final-oh-my.html)

> `final` means single-assignment. A final variable or field must have an initializer. Once assigned a value, a `final` variable’s value cannot be changed. final modifies variables.

Sử dụng `final` để định nghĩa Immutable variables trong Dart

Trong Swift, chúng được định nghĩa constants với từ khóa `let`

> A constant declaration introduces a constant named value into your program. Constant declarations are declared using the let keyword and have the following form:

```swift
let constant name: type = expression
```

> A constant declaration defines an immutable binding between the constant name and the value of the initializer expression; after the value of a constant is set, it cannot be changed.

Đọc thêm: [Swift Declarations](https://docs.swift.org/swift-book/ReferenceManual/Declarations.html)

5. Functions
--------------------------------------------------------------

Functions là first-class citizens trong Swift và Dart

Điều này có nghĩa là giống như các objecs, functions có thể truyền dưới dạng arguments và được lưu dưới dạng properties hoặc kết quả trả về.

Bước đầu so sánh, chúng ta sẽ khởi tạo các functions không có arguments.

Trong Dart, các kiểu trả về được đặt trước tên của method:

```java
void foo();
int bar();
```

Trong Swift, chúng ta sử dụng `-> T` làm ký hiệu hậu tố. Điều này không bắt buộc nếu nó trả về giá trị `void`:

```Swift
func foo()
func bar() -> Int
```

Đọc thêm:

- [Dart Functions](https://www.dartlang.org/guides/language/language-tour#functions)

- [Swift Functions](https://docs.swift.org/swift-book/LanguageGuide/Functions.html)

6. Named và un-named parameters
--------------------------------------------------------------

Cả hai ngôn ngữ đều hỗ trợ ***named*** và ***un-named*** parameters

### Named

Trong Dart, chúng ta định nghĩa named parameters trong dấu (`{}`):

```java
void foo({String name, int age, double height});
foo(name: 'Andrea', age: 34, height: 1.84);
```

Trong Swift, named parameters là mặc định:

```swift
func foo(name: String, age: Int, height: Double)
foo(name: "Andrea", age: 34, height: 1.84)
```

### Un-named

Trong Dart, chúng ta định nghĩa un-named parameters bằng cách bỏ dấu (`{}`):

```java
void foo(String name, int age, double height);
foo('Andrea', 34, 1.84);
```

Trong Swift, chúng ta định nghĩa un-named parameters bằng cách sử dụng dấu (`_`):

```swift
func foo(_ name: String, _ age: Int, _ height: Double)
foo("Andrea", 34, 1.84)
```

Đọc thêm: [Function Argument Labels and Parameter Names](https://docs.swift.org/swift-book/LanguageGuide/Functions.html#ID166) trong Swift.

7. Optional và default parameters
--------------------------------------------------------------

Cả hai ngôn ngữ đều hỗ trợ ***default parameters***

> In Swift, you can define a default value for any parameter in a function by assigning a value to the parameter after that parameter’s type. If a default value is defined, you can omit that parameter when calling the function.

```swift
func foo(name: String, age: Int = 0, height: Double = 0.0)
foo(name: "Andrea", age: 34) // name: "Andrea", age: 34, height: 0.0
```

Đọc thêm: - [Default Parameter Values trong Swift.](https://docs.swift.org/swift-book/LanguageGuide/Functions.html#ID169)

Trong Dart, optional parameters có thể là positional hoặc named, nhưng không thể là cả 2.

```java
// positional optional parameters
void foo(String name, [int age = 0, double height = 0.0]);
foo('Andrea', 34); // name: 'Andrea', age: 34, height: 0.0
// named optional parameters
void foo({String name, int age = 0, double height = 0.0});
foo(name: 'Andrea', age: 34); // name: 'Andrea', age: 34, height: 0.0
```

Đọc thêm: [Optional parameters trong Dart.](https://www.dartlang.org/guides/language/language-tour#optional-parameters)

8. Closures
--------------------------------------------------------------

Là first-class objecs, functions có thể được chuyền dưới dạng arguments cho các functions khác, hoặc gán cho các variables.
