<?php
$conn = new mysqli("localhost", "brian", "q", "motor_de_busqueda");
$result = $conn->query("SELECT * FROM seccion1");

$cadena = "";
while($rs = $result->fetch_array()) {
    if ($cadena != "") {
    $cadena .= ",";}
    $cadena .= '{"id":"'.$rs["ID"].'",';
    $cadena .= '"pregunta":"'.$rs["pregunta"].'",';
    $cadena .= '"respuesta":"'.$rs["respuesta"].'",';
    $cadena .= '"links":"'. $rs["links"].'"}'; 
}
$cadena ='{"datos":['.$cadena.']}';
$conn->close();

echo($cadena);
?>