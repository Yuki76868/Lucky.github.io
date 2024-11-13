<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>今天吃点啥</title>
    <style>
:root {
  --color-1: #8dbf8b;
  --color-2: #fcf1d8;
  --color-3: #fadc9c;
  --color-4: #f09e56;
}

body {
  background: linear-gradient(90deg, var(--color-1) 0%, var(--color-1) 25%, var(--color-2) 25%, var(--color-2) 50%, var(--color-3) 50%, var(--color-3) 75%, var(--color-4) 75%, var(--color-4) 100%);
}
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8ff;
            margin: 0;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }
        h1 {
            color: #333;
            text-align: center;
        }
        #result {
            font-size: 1.5em;
            color: #d9534f;
            margin-top: 20px;
            padding: 10px 20px;
            border: 2px solid #d9534f;
            border-radius: 10px;
            background-color: #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        #refreshButton {
            margin-top: 20px;
            padding: 10px 20px;
            border: none;
            border-radius: 10px;
            background-color: #d9534f;
            color: #fff;
            font-size: 1em;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        #refreshButton:hover {
            background-color: #c9302c;
        }
    </style>
</head>
<body>
    <h1>今天吃点啥</h1>
    <p id="result"></p >
    <button id="refreshButton">我不</button>
    <script>
        function getRandomItem(array) {
            var randomIndex = Math.floor(Math.random() * array.length);
            return array[randomIndex];
        }

        var foodList = [
            "汉堡",
            "披萨",
            "寿司",
            "炸鸡",
            "火锅",
            "沙拉",
            "面条",
            "炒饭",
            "蛋糕",
            "冰淇淋"
        ];

        function selectRandomFood() {
            var randomFood = getRandomItem(foodList);
            document.getElementById("result").innerText = "" + randomFood;
        }

        window.onload = function() {
            selectRandomFood();
        };

        document.getElementById("refreshButton").addEventListener("click", function() {
            selectRandomFood();
        });
    </script>
</body>
</html>
