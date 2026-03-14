<?php
session_start();
include "config.php";

if(isset($_POST['login'])){

$username = $_POST['username'];
$password = $_POST['password'];

$sql = "SELECT * FROM users WHERE username='$username' AND password='$password'";
$result = $conn->query($sql);

if($result->num_rows > 0){
    $_SESSION['username'] = $username;
    header("Location: dashboard.php");
}else{
    echo "Login Failed";
}

}
?>

<h2>Login</h2>

<form method="POST">

Username:<br>
<input type="text" name="username"><br><br>

Password:<br>
<input type="password" name="password"><br><br>

<button name="login">Login</button>

</form>
