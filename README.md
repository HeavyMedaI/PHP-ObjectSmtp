PHP-SmtpObject
===============

PHP SMPT Mail Object with PHPMailer Object

Example Using

<?php

    require_once "Smtp.Object.php";

    $Smtp = new ObjectSmtp;

    $Smtp::debug(3);

    $Smtp::set(); # Auto Config from Contstant Variables

    $Smtp::is_html(false);

    $Smtp::from("info@example.com"); # From E-mail address

    $Smtp::fromname("Name Surname"); # From Name

    $Smtp::sender("noreply@example.com"); # Sender E-mail address

    $Smtp::add_address("to1@example.com", "Name Surname"); # Receiver1 informations

    $Smtp::add_address("to2@example.com", "Name Surname"); # Receiver2 informations

    $Smtp::add_address("to3@example.com", "Name Surname"); # Receiver3 informations

    $Smtp::subject("Message Subject");

    $Smtp::body("Message Body");

    $Smtp::altbody("Message Alt Body(Ex. Copyright footer)");

    # $Smtp::send(); # Returns Boolean true|false

    if(!$Smtp::send()){

        var_dump($Smtp::error_info()); # or only $Smtp::ErrorInfo(); (var_dump)

    }

?>
