# Learn-php7-basic

<?php

//Funções arrays
	//is_array..testando se a variável é um array
$usuario = array("nome"=> "Adriano", "idade"=> 24, "altura"=> 1.74);
$usuario["cidade"] = "Salvador"; 	

$agata = "Buuu";
if(is_array($agata)):
	echo "É um array";
else:
	echo "Não é um array";
endif;
echo "<hr>";
	//in_array...verifica se o valor existe no array
echo in_array("Salvador", $usuario);
echo "<hr>";
//=================================================================================================	
	//arrey_keys...retorna um novo array com as chaves(indices) do array passado como parametros
$keys = array_keys($usuario);
print_r($keys);
echo "<hr>";
	//array_values...  retorna um novo array com os valores do array passado com parametro
$values = array_values($usuario);
print_r($values);
echo "<hr>";
//================================================================================================	
	//aray_merge...agrega os valores de dois array
$mat = array("caderno", "caneta", "notebook");
$disciplinas = array("redes","l.programacao","ingles");

$semestre = array_merge($mat, $disciplinas);

print_r($semestre);
echo "<hr>";
//=================================================================================================	
	//aray_pop...exclui a ultima posição do array, com o echo ele mostra o elemnto excluso
print_r($mat);
echo "<br>";
echo array_pop($mat);
echo "<br>";
print_r ($mat);
echo "<hr>";
	//array_shift...exclui a primeira posição do array
print_r($mat);
echo "<br>";
echo array_shift($mat);
echo "<br>";
print_r($mat);
echo "<hr>";
//====================================================================================================
	//array_unshift...adciona um ou mais elemento no inicio do array
$cel = array("nokia", "LG", "Samsung");
print_r($cel);
echo "<br>";
array_unshift($cel, "motorola", "sony");
print_r($cel);
echo "<hr>";
	//array_push...adciona um ou mais elementos no final do array
array_push($cel, "LGK10", "J7", "Moto5+");
print_r($cel);
echo "<hr>";
//======================================================================================================
	//array_combine....mescla dos array
$roupas = array("camisa", "calça", "tênis");
$color = array("vermelha", "azul", "branco");

$moda = array_combine($roupas, $color);
print_r($moda);
echo "<hr>";
//=======================================================================================================
	//array_sum...soma os valores do array
$calcular = array(5, 3, 14.9, 98);
echo array_sum($calcular);
echo "<hr>";
//=======================================================================================================
	//explode....transforma uma string num array
$chave = "001 abc 999";
$cripto = explode(' ', $chave);
print_r($cripto);
echo "<hr>";
	//implode...transforma um array em string
$return = implode(" ", $cripto);
echo $return;
