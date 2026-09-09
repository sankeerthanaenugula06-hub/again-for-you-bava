# again-for-you-bava
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For You Bava ❤️</title>

    <style>
        body {
            margin: 0;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            background: #fff0f5;
            font-family: Arial, sans-serif;
        }

        .page {
            display: none;
            width: 100%;
            justify-content: center;
            align-items: center;
        }

        .page.active {
            display: flex;
        }

        .box {
            background: white;
            padding: 45px 30px;
            border-radius: 25px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
            width: 85%;
            max-width: 500px;
        }

        .emoji {
            font-size: 75px;
        }

        h1 {
            font-size: 42px;
            color: #e91e63;
        }

        h2 {
            font-size: 30px;
            color: #333;
        }

        .next {
            margin-top: 25px;
            padding: 14px 35px;
            border: none;
            border-radius: 30px;
            background: #e91e63;
            color: white;
            font-size: 20px;
            font-weight: bold;
            cursor: pointer;
        }

        .next:hover {
            transform: scale(1.05);
        }

        .prank {
            color: red;
            font-size: 45px;
            font-weight: 900;
        }
    </style>
</head>

<body>

    <!-- PAGE 1 -->
    <section class="page active" id="page1">
        <div class="box">
            <div class="emoji">💌</div>

            <h1>For You Bava ❤️</h1>

            <p>Something special is waiting for you... 😌</p>

            <button class="next" onclick="goToPage(2)">
                Next 💕
            </button>
        </div>
    </section>

    <!-- PAGE 2 - PRANK -->
    <section class="page" id="page2">
        <div class="box">
            <div class="emoji">😂</div>

            <h1 class="prank">
                DON'T BE A FOOL!!
            </h1>

            <h2>
                IT'S JUST A JOKE! 😜❤️
            </h2>
        </div>
    </section>

    <script>
        function goToPage(pageNumber) {
            document.querySelectorAll(".page").forEach(function(page) {
                page.classList.remove("active");
            });

            var nextPage = document.getElementById("page" + pageNumber);

            if (nextPage) {
                nextPage.classList.add("active");
            }
        }
    </script>

</body>
</html>
