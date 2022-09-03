<!-- Submitted By: Dhruv Kakadiya
     Subitted On:25-07-2022
     Instructor:Maninder Kaur Tatla -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Document</title>
</head>
<body>

<img src="images/starbucks.png" width=150px class="img">

<div class="float-container">

    <div class="float-child">
        <div class="green">
        <h1>Make Your Coffee:</h1>
        <form action="order.php" method="post">

            <?php 
            if($_POST['size']==''){
                echo'
                <label><h3>Pick your size: </h3>
                <select name="size" id="size" >
                    <option value="">None</option>
                    <option value="short">SHORT</option>
                    <option value="tall">TALL</option>
                    <option value="grande">GRANDE</option>
                    <option value="venti">VENTI</option>
                </select>
                </label><br> <p>Please select size of cup</p>';
            }else{
                echo'
                <label><h3>Pick your size: </h3>
                <select name="size" id="size" >
                    <option value="">None</option>
                    <option value="short">SHORT</option>
                    <option value="tall">TALL</option>
                    <option value="grande">GRANDE</option>
                    <option value="venti">VENTI</option>
                </select>
                </label>';
            }

            if($_POST['sugar']<0 || $_POST['sugar']>5){
                echo '<label> <h3>Add sugar: </h3> <input type="number" name="sugar"> </label> <br> <p>0-5 sugar only available</p>';
            }else{
                echo '<label> <h3>Add sugar: </h3> <input type="number" name="sugar"> </label>';
            }

            if($_POST['cream']<0 || $_POST['cream']>5){
                echo '<label> <h3>Add cream:</h3> <input type="number" name="cream"> </label> <br> <p>0-5 cream only available</p>';
            }else{
                echo '<label> <h3>Add cream:</h3> <input type="number" name="cream"> </label>';
            }

            if($_POST['coffee']<0){
                echo '<label> <h3>Add coffee: </h3> <input type="number" name="coffee"></label> <br> <p>Do you mean no cup of coffee? LOL xD</p> <br> <br>';
            }else if($_POST['coffee']==''){
                echo '<label> <h3>Add coffee: </h3> <input type="number" name="coffee"></label> <br> <p>Please enter the number of coffee you want</p> <br> <br>';
            }else{
                echo '<label> <h3>Add coffee: </h3> <input type="number" name="coffee"></label> <br> <br>';
            }

            echo '<input type="submit" value="submit">';
            ?>

            </form>
        </div>
    </div>
  
    <div class="float-child">

        <h1>Your Bill Info:</h1><br>
        <?php
            $coffee = $_POST['coffee'];
            $sugar=0;
            $cream=0;
            switch($_POST['size']){
                case 'short':
                    $price=2.55;
                    $sum=0;
                    echo "<img src='images/cup.jpeg' width='45'> <br>";
                    for($x=0; $x<$_POST['sugar']; $x++){
                        echo "<img src='images/sugar.jpeg' width='30'>";
                        echo "   ";
                        $sugar++;
                        if($sugar>4){
                            break;
                        }
                    }
                    echo "<br>";
                    for($x=0; $x<$_POST['cream']; $x++){
                        echo "<img src='images/cream.jpeg' width='30'>";
                        echo "   ";
                        $cream++;
                        if($cream>4){
                            break;
                        }
                    }
                    echo "<br> <br> <br>";
                    for($x=0; $x<$_POST['coffee']; $x++){
                        $sum = $price * $coffee;
                    }
                    $tax = number_format(((13/100)*$sum),2);
                    $total = number_format(($sum+$tax),2);
                    $sum = number_format($sum,2);
                    echo "Short coffee*$coffee : $ $sum <br> <br>";
                    echo "Tax : $ $tax <br>";
                    echo '<hr width="200px">';
                    echo "Total : $ $total";
                    break;
                case 'tall':
                    $price=3.99;
                    $sum=0;
                    echo "<img src='images/cup.jpeg' width='65'> <br>";
                    for($x=0; $x<$_POST['sugar']; $x++){
                        echo "<img src='images/sugar.jpeg' width='30'>";
                        echo "   ";
                        $sugar++;
                        if($sugar>4){
                            break;
                        }
                    }
                    echo "<br>";
                    for($x=0; $x<$_POST['cream']; $x++){
                        echo "<img src='images/cream.jpeg' width='30'>";
                        echo "   ";
                        $cream++;
                        if($cream>4){
                            break;
                        }
                    }
                    echo "<br> <br> <br>";
                    for($x=0; $x<$_POST['coffee']; $x++){
                        $sum = $price * $coffee;
                    }
                    $tax = number_format(((13/100)*$sum),2);
                    $total = number_format(($sum+$tax),2);
                    $sum = number_format($sum,2);
                    echo "Tall coffee*$coffee : $ $sum <br> <br>";
                    echo "Tax : $ $tax <br>";
                    echo '<hr width="200px">';
                    echo "Total : $ $total";
                    break;
                case 'grande':
                    $price=5.55;
                    $sum=0;
                    echo "<img src='images/cup.jpeg' width='85'> <br>";
                    for($x=0; $x<$_POST['sugar']; $x++){
                        echo "<img src='images/sugar.jpeg' width='30'>";
                        echo "   ";
                        $sugar++;
                        if($sugar>4){
                            break;
                        }
                    }
                    echo "<br>";
                    for($x=0; $x<$_POST['cream']; $x++){
                        echo "<img src='images/cream.jpeg' width='30'>";
                        echo "   ";
                        $cream++;
                        if($cream>4){
                            break;
                        }
                    }
                    echo "<br> <br> <br>";
                    for($x=0; $x<$_POST['coffee']; $x++){
                        $sum = $price * $coffee;
                    }
                    $tax = number_format(((13/100)*$sum),2);
                    $total = number_format(($sum+$tax),2);
                    $sum = number_format($sum,2);
                    echo "Grande Coffee*$coffee : $ $sum <br> <br>";
                    echo "Tax : $ $tax <br>";
                    echo '<hr width="200px">';
                    echo "Total : $ $total";
                    break;
                case 'venti':
                    $price=6.99;
                    $sum=0;
                    echo "<img src='images/cup.jpeg' width='100'> <br>";
                    for($x=0; $x<$_POST['sugar']; $x++){
                        echo "<img src='images/sugar.jpeg' width='30'>";
                        echo "   ";
                        $sugar++;
                        if($sugar>4){
                            break;
                        }
                    }
                    echo "<br>";
                    for($x=0; $x<$_POST['cream']; $x++){
                        echo "<img src='images/cream.jpeg' width='30'>";
                        echo "   ";
                        $cream++;
                        if($cream>4){
                            break;
                        }
                    }
                    echo "<br> <br> <br>";
                    for($x=0; $x<$_POST['coffee']; $x++){
                        $sum = $price * $coffee;
                    }
                    $tax = number_format(((13/100)*$sum),2);
                    $total = number_format(($sum+$tax),2);
                    $sum = number_format($sum,2);
                    echo "Venti coffee*$coffee : $ $sum <br> <br>";
                    echo "Tax : $ $tax <br>";
                    echo '<hr width="200px">';
                    echo "Total : $ $total";
                    break;
            }        
        ?>
    </div>

</div>
</body>
</html>

