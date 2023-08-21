<?php

$name = $_POST['name'];
$email = $_POST['email'];
$sub = $_POST['sub'];
$message = $_POST['message'];


//db connection
//$variable_name=mysqli_connect("server_name","username", "password","database_name")
$db = mysqli_connect("localhost", "root", "" ,"tandra");


    $insert_query = "INSERT INTO form (name,email,message,sub) 
    VALUES ('$name','$email','$sub', '$message)";

    mysqli_query($db, $insert_query);

    echo "registratoin successfull";


?>
