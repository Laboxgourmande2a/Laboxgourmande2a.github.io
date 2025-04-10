<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Commande Pancakes</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            max-width: 600px;
            margin: auto;
            padding: 20px;
            background-color: #fff3e6;
        }
        h2 {
            text-align: center;
            color: #d35400;
        }
        .section {
            margin-bottom: 20px;
            padding: 15px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        label {
            display: block;
            margin: 5px 0;
        }
        .submit-btn {
            display: block;
            width: 100%;
            padding: 12px;
            background: #d35400;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            cursor: pointer;
        }
        .submit-btn:hover {
            background: #a84300;
        }
    </style>
</head>
<body>
    <h2>Commande de Pancakes</h2>
    <form id="commandeForm">
        <div class="section">
            <h3>Informations personnelles :</h3>
            <label>Nom : <input type="text" name="nom" required></label>
            <label>Téléphone : <input type="tel" name="telephone" required></label>
            <label>Adresse de livraison : <input type="text" name="adresse" required></label>
        </div>

        <div class="section">
            <h3>Choisissez votre Box :</h3>
            <label><input type="radio" name="box" value="mini" required> Mini (10 pancakes avec 1 nappage et 1 topping ou 1 fruit)</label>
            <label><input type="radio" name="box" value="solo"> Solo (20 pancakes avec 1 nappage + 1 fruit et 1 topping ou 2 fruits ou 2 toppings)</label>
            <label><input type="radio" name="box" value="duo"> Duo (40 pancakes avec 2 nappages et 2 fruits et 2 toppings)</label>
        </div>

        <div class="section">
            <h3>Suppléments Gourmands :</h3>
            <div id="toppings">
                <label><input type="checkbox" name="topping" value="Kinder Bueno"> Kinder Bueno</label>
                <label><input type="checkbox" name="topping" value="Spéculoos"> Spéculoos</label>
                <label><input type="checkbox" name="topping" value="Oreo"> Oreo</label>
                <label><input type="checkbox" name="topping" value="Kit Kat"> Kit Kat</label>
                <label><input type="checkbox" name="topping" value="M&Ms"> M&Ms</label>
                <label><input type="checkbox" name="topping" value="Éclats de noisette"> Éclats de noisette</label>
                <label><input type="checkbox" name="topping" value="Sucre glace"> Sucre glace</label>
            </div>
        </div>

        <div class="section">
            <h3>Fruits :</h3>
            <div id="fruits">
                <label><input type="checkbox" name="fruit" value="Fraise"> Fraise</label>
                <label><input type="checkbox" name="fruit" value="Banane"> Banane</label>
                <label><input type="checkbox" name="fruit" value="Kiwi"> Kiwi</label>
                <label><input type="checkbox" name="fruit" value="Framboise"> Framboise</label>
                <label><input type="checkbox" name="fruit" value="Poire"> Poire</label>
                <label><input type="checkbox" name="fruit" value="Myrtille"> Myrtille</label>
                <label><input type="checkbox" name="fruit" value="Mangue"> Mangue</label>
            </div>
        </div>

        <div class="section">
            <h3>Nappages :</h3>
            <div id="nappages">
                <label><input type="checkbox" name="nappage" value="Nutella"> Nutella</label>
                <label><input type="checkbox" name="nappage" value="Caramel"> Caramel beurre salé</label>
                <label><input type="checkbox" name="nappage" value="Crème pistache"> Crème pistache</label>
                <label><input type="checkbox" name="nappage" value="Sirop d’érable"> Sirop d’érable</label>
                <label><input type="checkbox" name="nappage" value="Chocolat noir"> Chocolat noir</label>
                <label><input type="checkbox" name="nappage" value="Chocolat blanc"> Chocolat blanc</label>
            </div>
        </div>

        <button type="submit" class="submit-btn">Valider la commande</button>
    </form>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const boxChoices = document.querySelectorAll('input[name="box"]');
            const nappages = document.querySelectorAll('input[name="nappage"]');
            const toppings = document.querySelectorAll('input[name="topping"]');
            const fruits = document.querySelectorAll('input[name="fruit"]');

            function updateLimits() {
                let maxNappages = 0, maxToppings = 0, maxFruits = 0;
                const selectedBox = document.querySelector('input[name="box"]:checked');
                if (!selectedBox) return;
                
                if (selectedBox.value === 'mini') {
                    maxNappages = 1; maxToppings = 1; maxFruits = 1;
                } else if (selectedBox.value === 'solo') {
                    maxNappages = 1; maxToppings = 2; maxFruits = 2;
                } else if (selectedBox.value === 'duo') {
                    maxNappages = 2; maxToppings = 2; maxFruits = 2;
                }
                
                limitSelection(nappages, maxNappages);
                limitSelection(toppings, maxToppings);
                limitSelection(fruits, maxFruits);
            }
            
            function limitSelection(elements, max) {
                elements.forEach(el => el.addEventListener('change', function() {
                    const checked = [...elements].filter(e => e.checked);
                    if (checked.length > max) this.checked = false;
                }));
            }
            
            boxChoices.forEach(choice => choice.addEventListener('change', updateLimits));
        });
    </script>
</body>
</html>
