<hr>
<p align="center">
wait im loaded 💵🛠
</p>
<hr>

<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Zamiana liter</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #222;
            color: white;
            font-size: 4rem;
            font-family: Arial, sans-serif;
        }
        .wrapper {
            display: flex;
            position: relative;
            width: 100px;
            height: 60px;
        }
        .letter {
            position: absolute;
            transition: transform 0.5s ease-in-out, opacity 0.25s ease-in-out;
        }
        .p { left: 0; }
        .k { right: 0; }

        .swap .p {
            transform: translateX(50px) scale(1.2) rotate(180deg);
            opacity: 0;
        }
        .swap .k {
            transform: translateX(-50px) scale(1.2) rotate(-180deg);
            opacity: 0;
        }

        .swap-reverse .p {
            transform: translateX(0) scale(1) rotate(0);
            opacity: 1;
        }
        .swap-reverse .k {
            transform: translateX(0) scale(1) rotate(0);
            opacity: 1;
        }
    </style>
</head>
<body>
    <div class="wrapper">
        <span class="letter p">p</span>
        <span class="letter k">k</span>
    </div>

    <script>
        const wrapper = document.querySelector('.wrapper');
        let swapped = false;

        setInterval(() => {
            if (swapped) {
                wrapper.classList.remove('swap');
                wrapper.classList.add('swap-reverse');
            } else {
                wrapper.classList.add('swap');
                wrapper.classList.remove('swap-reverse');
            }
            swapped = !swapped;
        }, 1000);
    </script>
</body>
</html>
