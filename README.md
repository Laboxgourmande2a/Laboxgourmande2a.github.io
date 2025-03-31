<!DOCTYPE html>
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
    <form>
        <div class="section">
            <h3>Choisissez votre Box :</h3>
            <label><input type="radio" name="box" value="mini"> Mini (10 pancakes avec 1 nappage et 1 topping)</label><br>
            <label><input type="radio" name="box" value="solo"> Solo (20 pancakes avec 1 nappage et 2 toppings ou fruits)</label><br>
            <label><input type="radio" name="box" value="duo"> Duo (40 pancakes avec 2 nappages et 2 toppings et/ou fruits)</label>
        </div>

        <div class="section">
            <h3>Suppléments Gourmands +1€ :</h3>
            <label><input type="checkbox" name="topping" value="Kinder Bueno"> Kinder Bueno</label><br>
            <label><input type="checkbox" name="topping" value="Kinder Bueno White"> Kinder Bueno White</label><br>
            <label><input type="checkbox" name="topping" value="Oreo"> Oreo</label><br>
            <label><input type="checkbox" name="topping" value="Speculoos"> Spéculoos</label><br>
            <label><input type="checkbox" name="topping" value="M&Ms"> M&Ms</label><br>
            <label><input type="checkbox" name="topping" value="Snickers"> Snickers</label><br>
            <label><input type="checkbox" name="topping" value="Kit Kat"> Kit Kat</label><br>
            <label><input type="checkbox" name="topping" value="Lion"> Lion</label><br>
            <label><input type="checkbox" name="topping" value="Granola"> Granola</label><br>
            <label><input type="checkbox" name="topping" value="Eclats de noisette"> Eclats de noisette</label><br>
            <label><input type="checkbox" name="topping" value="Sucre glace"> Sucre glace</label><br>
        </div>

        <div class="section">
            <h3>Nappages +0.50€ :</h3>
            <label><input type="checkbox" name="nappage" value="Nutella"> Nutella</label><br>
            <label><input type="checkbox" name="nappage" value="Caramel beurre salé"> Caramel beurre salé</label><br>
            <label><input type="checkbox" name="nappage" value="Chocolat noir"> Chocolat noir</label><br>
            <label><input type="checkbox" name="nappage" value="Crème pistache"> Crème pistache</label><br>
            <label><input type="checkbox" name="nappage" value="Crème spéculoos"> Crème spéculoos</label><br>
            <label><input type="checkbox" name="nappage" value="Sirop d'érable"> Sirop d'érable</label><br>
            <label><input type="checkbox" name="nappage" value="Chocolat blanc"> Chocolat blanc</label><br>
        </div>

        <div class="section">
            <h3>Fruits (pouvant varier selon les saisons) +1€ :</h3>
            <label><input type="checkbox" name="fruit" value="Fraise"> Fraise</label><br>
            <label><input type="checkbox" name="fruit" value="Banane"> Banane</label><br>
            <label><input type="checkbox" name="fruit" value="Kiwi"> Kiwi</label><br>
            <label><input type="checkbox" name="fruit" value="Framboise"> Framboise</label><br>
            <label><input type="checkbox" name="fruit" value="Myrtille"> Myrtille</label><br>
            <label><input type="checkbox" name="fruit" value="Poire"> Poire</label><br>
            <label><input type="checkbox" name="fruit" value="Melon"> Melon</label><br>
            <label><input type="checkbox" name="fruit" value="Mangue"> Mangue</label><br>
        </div>

        <div class="section">
            <h3>Nom et téléphone :</h3>
            <input type="text" name="nom" placeholder="Votre nom" required>
        </div>
     
      <div class="section">
            <h3>Numéro de téléphone :</h3>
            <input type="text" name="Numéro de téléphone" placeholder="Votre numéro de téléphone" required>
        </div>

        <div class="section">
            <h3>Adresse de livraison :</h3>
            <textarea name="Adresse de livraison" placeholder="Votre adresse de livraison" rows="3"></textarea>
        </div>

        <button type="submit" class="submit-btn">Valider la commande</button>
    </form>
</body>
</html>
