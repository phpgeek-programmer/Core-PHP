# Memulai untuk menggunakan PHP
Hello world menggunakan PHP

```php
<html>  
<head>  
  <title>My First PHP Program</title>  
</head>  
<body>  

<?php  
  echo "Hello Everybody!";  
?>  
</body>
```

Script php diawali dengan tanda  

```php
<?php
```

dan diakhiri dengan tanda  
```php
?>
```

Untuk belajar lebih banyak mengenai php, tulislah ini kedalam file bernama info.php  
```php
<?php
  phpinfo();
?>
```
simpan di tempat yang bisa diakses oleh web server apache dan cobalah buka dengan web browser.

## Komentar
Contoh komentar dalam kode php
```php
<?php
     /*
      * This is our first style of comment.
      */
     echo "Style 1";

     //
     // This is our second style of comment.  It is "single line"
     //
     echo "Style 2";

     #
     # This third style is also "single line."
     #
     echo "Style 3";
?>
```

## Menyimpan data ke Variabel
```php
<?php
  $varname = "moo";               // ok
  $var______Name = "oink";        // ok
  $__12345var = 12345;            // ok
  $12345__var = 12345;             // NOT ok - starts w/ number
  $école = "Rue St. Jacques";      // ok - é is an extended char
  $ = "car";                   // NOT ok - has invalid chars
?>
```

## Tipe Data Dasar PHP
### Angka
```php
<?php

   $abc = 123;       // decimal
   $def = -123;
   $ghi = 0173;      // octal, value is 123 in decimal
   $jkl = -0173;     // octal, value is -123 in decimal
   $mno = 0x7b;      // hexadecimal, 123
   $pqr = -0x7B;     // hexadecimal, -123
```

contoh menggunanakan data floating point

```php
<?php
    $floatvar1 = 7.555;
    $floatvar2 = 6.43e2;          // same as 643.0
    $floatvar3 = 1.3e+4;          // same as 13000.0;
    $floatvar4 = 5.555e-4;        // same as 0.0005555;
    $floatvar5 = 1000000000000;   // too big for int ==> float
?>
```

### String
String bisa menggunakan single quote
```php
<?php echo 'This is a single-quoted string.'; ?>
```
maupun double quote
```php
<?php echo "This is a double-quoted string."; ?>
```

### Notasi Heredoc
Notasi ini digunakan agar output yang dihasilkan sesuai dengan format yang diinginkan. Output ini bisa dilihat dari browser dengan klik kanan > view code.

```php
<?php

   echo <<<HTML

   <p align='center'>
     This is an example of text being input using the heredoc
     Notation in PHP.  It is nice, because I can pretty much
     type <em>freely</em> without having to worry about how
     to fit it all into a double-quoted string.
   </p>

HTML;
```

### Boolean
Tipe data boolean hanya akan berisi nilai True atau False
```php
<?php
$apple = TRUE;
   $orange = fAlSe;
   $cat = tRUe;
   $dog = False;

?>
```

## Fungsi-fungsi Penting
### nl2br
berfungsi untuk mengkonversi sembarang karakter baris baru ke dalam tag
```html
<br/>
```

### var_dump
berfungsi untuk mencetak tipe dan nilai dari variabel ke layar.

### print_r
berfungsi sama seperti var_dump, tetapi lebih mudah dibaca oleh manusia. Ia juga bisa menerima parameter.

### var_export
berfungsi untuk menampilkan isi suatu variabel tapi tampilannya sudah diformat sehinggal lebih mudah dibaca oleh manusia.

```php
<?php

  $arr = array(1, 2, 3, 4);
  var_export($arr);

?>
```
menghasilkan output sebagai berikut

```
array (
  0 => 1,
  1 => 2,
  2 => 3,
  3 => 4,
)
```


