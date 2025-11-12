<?php
header('Content-type: text/html; charset=utf-8');


$mysqli = mysqli_connect($host, $user, $password, $db); 


if ($mysqli == false) { 
    print("Ошибка: Невозможно подключиться к MySQL ");

$host = 'localhost';
$db = 'fdkpgjvl_MyBasa';
$user = 'fdkpgjvl_MyBasa';
$password = 'Mariya2015';



 } else { 
$name = $_POST["name"];
$lastname = $_POST["lastname"];
$email = $_POST["email"];
$pass = $_POST["pass"]; 

$result = $mysqli->query("SELECT * FROM `users` WHERE 'email'='$email'");
/* var_dump($result); */
if ($result->num_rows != 0) {
    print('exist');

} else {
    print("ok");
$mysqli->query("INSERT INTO `user`(`name`, `lastname`, `email`, `pass`) VALUES ('$name', '$lasname', '$email', '$pass')");
}
