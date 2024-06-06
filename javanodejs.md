# I. Java:
## 1. Biến và kiểu dữ liệu:
### a. Biến:
```java
public class Bien {
    public static float PI = 3.14f;  //Đây là biến static
    int n;                           //Đây là biến instance
    
    public Bien () {
        char c = 'c';                //Đây là biến local
    }
} 
```
- **Biến local**:
**Định nghĩa:** là biến được khai báo bên trong một phương thức, khối lệnh hoặc cấu trúc lệnh.
**Phạm vi:** chỉ được truy cập từ bên trong phương thức hoặc khối lệnh nơi nó được khai báo. Khi phương thức hoặc khối lệnh đó kết thúc, biến local sẽ bị hủy.
**Khởi tạo:** phải được khởi tạo trước khi sử dụng. 
- **Biến Instance**:
**Định nghĩa:** là biến được khai báo bên trong một lớp, nhưng bên ngoài bất kỳ phương thức, khối lệnh hoặc cấu trúc lệnh nào. 
**Phạm vi:** có phạm vi từ khi đối tượng được tạo ra cho đến khi đối tượng bị thu gom rác (garbage collected). Biến instance có thể được truy cập bởi tất cả các phương thức của lớp đó.
**Khởi tạo:** có thể được khởi tạo trực tiếp khi khai báo hoặc thông qua các khối khởi tạo, hàm khởi tạo. Nếu không được khởi tạo, biến instance sẽ được khởi tạo với giá trị mặc định (ví dụ: 0 cho số nguyên, null cho đối tượng, false cho boolean).
- **Biến Static**:
**Định nghĩa:** là biến được khai báo với từ khóa static bên trong một lớp. Biến này không thuộc về bất kỳ đối tượng cụ thể nào mà thuộc về chính lớp đó.
**Phạm vi:** có phạm vi toàn cục trong lớp và có thể được truy cập bởi tất cả các đối tượng của lớp đó. Nó cũng có thể được truy cập mà không cần tạo một đối tượng của lớp.
**Khởi tạo:** có thể được khởi tạo khi khai báo hoặc trong khối khởi tạo static. Nếu không được khởi tạo, nó sẽ nhận giá trị mặc định tương tự như biến instance.
### b. Kiểu dữ liệu:
kiểu dữ liệu|Mô tả
------------|-----
byte        | Dùng để lưu dữ liệu kiểu số nguyên có kích thước một byte (8 bít). Phạm vi biểu diễn giá trị từ -128 đến 127. Giá trị mặc định là 0.
char        | Dùng để lưu dữ liệu kiểu kí tự hoặc số nguyên không âm có kích thước 2 byte (16 bít). Phạm vi biểu diễn giá trị từ 0 đến u\ffff. Giá trị mặc định là 0.
boolean     | Dùng để lưu dữ liệu chỉ có hai trạng thái đúng hoặc sai (độ lớn chỉ có 1 bít). Phạm vi biểu diễn giá trị là {“True”, “False”}. Giá trị mặc định là False.
short       | Dùng để lưu dữ liệu có kiểu số nguyên, kích cỡ 2 byte (16 bít). Phạm vi biểu diễn giá trị từ - 32768 đến 32767. Giá trị mặc định là 0.
int         | Dùng để lưu dữ liệu có kiểu số nguyên, kích cỡ 4 byte (32 bít). Phạm vi biểu diễn giá trị từ -2,147,483,648 đến 2,147,483,647. Giá trị mặc định là 0.
long        | Dùng để lưu dữ liệu có kiểu số nguyên có kích thước lên đến 8 byte. Giá trị mặc định là 0L.
float       | Dùng để lưu dữ liệu có kiểu số thực, kích cỡ 4 byte (32 bít). Giá trị mặc định là 0.0F.
double      | Dùng để lưu dữ liệu có kiểu số thực có kích thước lên đến 8 byte. Giá trị mặc định là 0.00D.
## 2. Các toán tử:

**Toán tử số học:**
Toán tử|Mô tả|
-------|-----|
\+ |Trả về giá trị là tổng của hai toán hạng	
\- |Trả về kết quả là hiệu của hai toán hạng.	
\* |Trả về giá trị là tích của hai toán hạng.	
/ |Trả về giá trị là thương của phép chia.	
%      |Giá trị trả về là phần dư của phép chia	
++     |Tăng giá trị của biến lên 1. Ví dụ a++ tương đương với a = a + 1	
--     |Giảm giá trị của biến 1 đơn vị. Ví dụ a-- tương đương với a = a - 1	
+=     |Cộng các giá trị của toán hạng bên trái vào toán hạng bên phải và gán giá trị trả về vào toán hạng bên trái. Ví dụ c += a tương đương c = c + a
-=     |Trừ các giá trị của toán hạng bên trái vào toán toán hạng bên phải và gán giá trị trả về vào toán hạng bên trái. Ví dụ c -= a tương đương với c = c - a
*=     |Nhân các giá trị của toán hạng bên trái với toán toán hạng bên phải và gán giá trị trả về vào toán hạng bên trái. Ví dụ c *= a tương đương với c = c * a
/=     |Chia giá trị của toán hạng bên trái cho toán toán hạng bên phải và gán giá trị trả về vào toán hạng bên trái. Ví dụ c /= a tương đương với c = c/a
%=     |Chia giá trị của toán hạng bên trái cho toán toán hạng bên phải và gán giá trị số dư vào toán hạng bên trái. Ví dụ c %= a tương đương với c = c%a

**Các toán tử quan hệ:**
Toán tử|Mô tả
-------|-----
 ==|Toán tử này kiểm tra sự tương đương của hai toán hạng
 !=|Toán tử này kiểm tra sự khác nhau của hai toán hạng
 \> |Kiểm tra giá trị của toán hạng bên phải lớn hơn toán hạng bên trái hay không
 < |Kiểm tra giá trị của toán hạng bên phải có nhỏ hơn toán hạng bên trái hay không
 \>=|Kiểm tra giá trị của toán hạng bên phải có lớn hơn hoặc bằng toán hạng bên trái hay không
 <=|Kiểm tra giá trị của toán hạng bên phải có nhỏ hơn hoặc bằng toán hạng bên trái hay không

Các toán tử logic:
Toán tử|Mô tả
-------|-----
&&     |Trả về một giá trị “Đúng” (True) nếu chỉ khi cả hai toán tử có giá trị “True”
\|\|   |Trả về giá trị “True” nếu ít nhất một giá trị là True
^      |Trả về giá trị True nếu và chỉ nếu chỉ một trong các giá trị là True, các trường hợp còn lại cho giá trị False (sai)
!      |Toán hạng đơn tử NOT. Chuyển giá trị từ True sang False và ngược lại.

**Toán tử điều kiện:**

```java
<biểu thức 1> ? <biểu thức 2> : <biểu thức 3>;
```

biểu thức 1: biểu thức logic. Trả về giá trị True hoặc False.
biểu thức 2: là giá trị trả về nếu biểu thức 1 là True.
biểu thức 3: là giá trị trả về nếu biểu thức 1 là False.
## 3. Các câu lệnh điều kiện:
### a. Mệnh đề if else:
```java
if (condition) {
    // khối lệnh này được thực thi
    // nếu condition = true
} else {
    // khối lệnh này được thực thi
    // nếu condition = false
}  
```
### b. Mệnh đề switch case:
```java
switch (bieu_thuc) {    
case gia_tri_1:
    // Khối lệnh 1
    break;  //tùy chọn
case gia_tri_2:    
    // Khối lệnh 2
    break;  //tùy chọn
......    
case gia_tri_n:    
    // Khối lệnh n
    break;  //tùy chọn    
default:     
    // Khối lệnh này được thực thi 
    // nếu tất cả các điều kiện trên không thỏa mãn 
}   
```

## 4. Vòng lặp:
### a. Vòng lặp For:
```java
for (khoi_tao_bien ; check_dieu_kien ; tang/giam_bien) {  
    // Khối lệnh được thực thi
} 
```
Ví dụ:
```java
for(int i = 0; i < 10; i++){
    System.out.println(i);
}
```
Kết quả sẽ in ra 10 là i từ 0 tới 9.

Vòng lặp for cải tiến:
```java
for (Type var : array) {  
    // Khối lệnh được thực thi
} 
```
Ví dụ:
```java
int arr[] = { 12, 23, 44, 56, 78 };
        for (int i : arr) {
            System.out.println(i);
        }
```
Kết quả:
```
12
23
44
56
78
```
### b. Vòng lặp While:
```java
while(condition) {  
    // Khối lệnh được lặp lại cho đến khi condition = False
}
```
Ví dụ:
```java
  int i = 1;
  while (i <= 10) {
   System.out.println(i);
   i++;
  }
```
Kết quả:
```
1
2
3
4
5
6
7
8
9
10
```
### c. Vòng lặp Do-While:
```java
do {  
    // Khối lệnh được thực thi
} while(condition); 
```
Ví dụ:
```java
int a = 1, sum = 0;
        do {
            sum += a;
            a++;
        } while (a <= 5);
        System.out.println("Sum of 1 to 5  is " + sum);
```
Biến a được khởi tạo với giá trị 1, sau đó nó vừa được dùng làm biến chạy (tăng lên 1 sau mỗi lần lặp) vừa được dùng để cộng dồn vào biến sum. Tại thời điểm kết thúc, chương trình sẽ in ra Sum of 1 to 5 is 15.
Kết quả:
```
Sum of 1 to 5 is 15
```

## 5. Mảng:
### a. Mảng 1 chiều trong java:
```java
int[] arr = new int[10]
```
Đây là cách khai báo mảng số nguyên 1 chiều gồm 10 phần tử trong mảng.
### b. Mảng 2 chiều trong java:
```java
int[][] arr = new int[10][9]
```
Đây là cách khai báo mảng 2 chiều gồm 10 hàng và 9 cột.
```java
for (int i = 0; i < arr.length; i++) {
    for (int j = 0; j < arr[i].length; j++) {
                arr[i][j] = i * j; // Ví dụ gán giá trị bằng tích của chỉ số hàng và cột
    }
}
for (int i = 0; i < arr.length; i++) {
    for (int j = 0; j < arr[i].length; j++) {
                System.out.print(arr[i][j] + " ");
    }
    System.out.println(); // Xuống dòng sau mỗi hàng
}
```
Kết quả sẽ là:
```
0 0 0 0 0 0 0 0 0 
0 1 2 3 4 5 6 7 8 
0 2 4 6 8 10 12 14 16 
0 3 6 9 12 15 18 21 24 
0 4 8 12 16 20 24 28 32 
0 5 10 15 20 25 30 35 40 
0 6 12 18 24 30 36 42 48 
0 7 14 21 28 35 42 49 56 
0 8 16 24 32 40 48 56 64 
0 9 18 27 36 45 54 63 72 
```
## 6. Các tính chất của Java OOPs:
## 7. Các khái niệm của Java OOPs:

# II. Nodejs: