<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Commande Pancakes</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: auto;
            padding: 20px;
            background-color: #f8f8f8;
        }
        h2 {
            text-align: center;
        }
        .section {
            margin-bottom: 20px;
            padding: 15px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .submit-btn {
            display: block;
            width: 100%;
            padding: 10px;
            background: #ff9900;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
        }
        .submit-btn:hover {
            background: #e68a00;
        }
    </style>
</head>
<body>
    <h2>Commande de Pancakes</h2>
    <form id="commandeForm">
        <div class="section">
            <h3>Informations personnelles :</h3>
            <label>Nom : <input type="text" name="nom" required></label><br>
            <label>Téléphone : <input type="tel" name="telephone" required></label><br>
            <label>Adresse de livraison : <input type="text" name="adresse" required></label>
        </div>

        <div class="section">
            <h3>Choisissez votre Box :</h3>
            <label><input type="radio" name="box" value="mini" required> Mini (10 pancakes avec 1 nappage et 1 topping)</label><br>
            <label><input type="radio" name="box" value="solo"> Solo (20 pancakes avec 1 nappage et 2 toppings ou fruits)</label><br>
            <label><input type="radio" name="box" value="duo"> Duo (40 pancakes avec 2 nappages et 2 toppings et/ou fruits)</label>
        </div>

        <div class="section">
            <h3>Suppléments Gourmands :</h3>
            <div id="toppings">
                <label><input type="checkbox" name="topping" value="Kinder Bueno"> Kinder Bueno</label><br>
                <label><input type="checkbox" name="topping" value="Kinder Bueno White"> Kinder Bueno White</label><br>
                <label><input type="checkbox" name="topping" value="Spéculoos"> Spéculoos</label><br>
                <label><input type="checkbox" name="topping" value="Oreo"> Oreo</label><br>
                <label><input type="checkbox" name="topping" value="Kit Kat"> Kit Kat</label><br>
                <label><input type="checkbox" name="topping" value="M&Ms"> M&Ms</label><br>
                <label><input type="checkbox" name="topping" value="Lion"> Lion</label><br>
                <label><input type="checkbox" name="topping" value="Snickers"> Snickers</label><br>
                <label><input type="checkbox" name="topping" value="Granola"> Granola</label><br>
                <label><input type="checkbox" name="topping" value="Éclats de noisette"> Éclats de noisette</label><br>
                <label><input type="checkbox" name="topping" value="Sucre glace"> Sucre glace</label><br>
            </div>
        </div>

        <div class="section">
            <h3>Nappages :</h3>
            <div id="nappages">
                <label><input type="checkbox" name="nappage" value="Nutella"> Nutella</label><br>
                <label><input type="checkbox" name="nappage" value="Caramel"> Caramel beurre salé</label><br>
                <label><input type="checkbox" name="nappage" value="Crème pistache"> Crème pistache</label><br>
                <label><input type="checkbox" name="nappage" value="Crème spéculoos"> Crème spéculoos</label><br>
                <label><input type="checkbox" name="nappage" value="Sirop d’érable"> Sirop d’érable</label><br>
                <label><input type="checkbox" name="nappage" value="Chocolat noir"> Chocolat noir</label><br>
                <label><input type="checkbox" name="nappage" value="Chocolat blanc"> Chocolat blanc</label><br>
            </div>
        </div>

        <div class="section">
            <h3>Fruits :</h3>
            <div id="fruits">
                <label><input type="checkbox" name="fruit" value="Fraise"> Fraise</label><br>
                <label><input type="checkbox" name="fruit" value="Banane"> Banane</label><br>
                <label><input type="checkbox" name="fruit" value="Kiwi"> Kiwi</label><br>
                <label><input type="checkbox" name="fruit" value="Framboise"> Framboise</label><br>
                <label><input type="checkbox" name="fruit" value="Poire"> Poire</label><br>
                <label><input type="checkbox" name="fruit" value="Myrtille"> Myrtille</label><br>
                <label><input type="checkbox" name="fruit" value="Melon"> Melon</label><br>
                <label><input type="checkbox" name="fruit" value="Mangue"> Mangue</label><br>
            </div>
        </div>

        <button type="submit" class="submit-btn">Valider la commande</button>
    </form>

    <script>
        document.getElementById("commandeForm").addEventListener("submit", function(event) {
            event.preventDefault();
            alert("Votre commande a été envoyée !");
        });
    </script>
</body>
</html>
