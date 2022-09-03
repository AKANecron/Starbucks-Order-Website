<!-- Submitted By: Dhruv Kakadiya
Subitted On:25-07-2022
Instructor:Maninder Kaur Tatla 
https://kakadidh.dev.fast.sheridanc.on.ca/Assignments/-->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A5-Dhruv-Kakadiya</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<img src="images/starbucks.png" width=150px class="img">

<div class="float-container">

    <div class="float-child">
        <div class="green">
        <h1>Make Your Coffee:</h1>
        <form action="order.php" method="post">
            <label><h3>Pick your size: </h3>
                <select name="size" id="size">
                    <option value="">None</option>
                    <option value="short">SHORT</option>
                    <option value="tall">TALL</option>
                    <option value="grande">GRANDE</option>
                    <option value="venti">VENTI</option>
                </select>
            </label>

            <label> <h3>Add sugar: </h3> <input type="number" name="sugar"> </label>

            <label> <h3>Add cream:</h3> <input type="number" name="cream"> </label>

            <label> <h3>Add coffee: </h3> <input type="number" name="coffee"></label> <br> <br>

            <input type="submit" value="submit">

        </form>
        </div>
    </div>
  
    <div class="float-child">
    <h1>Your Bill Info:</h1><br>
    </div>

</div>
</body>
</html>