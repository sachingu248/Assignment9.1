```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Dashboard</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #f1f5f9;
        }

        header {
            background: #1e293b;
            color: white;
            padding: 20px;
            text-align: center;
        }

        .layout {
            display: grid;
            grid-template-columns: 1fr;
            gap: 15px;
            padding: 15px;
        }

        aside, main {
            padding: 20px;
            border-radius: 8px;
        }

        aside {
            background: #334155;
            color: white;
        }

        main {
            background: white;
            min-width: 0;
        }

        .cards {
            display: grid;
            grid-template-columns: 1fr;
            gap: 15px;
        }

        .card {
            background: #dbeafe;
            padding: 20px;
            border-radius: 8px;
            overflow-wrap: anywhere;
        }

        footer {
            background: #1e293b;
            color: white;
            text-align: center;
            padding: 15px;
        }

        /* Tablet */
        @media (min-width: 600px) {
            .layout {
                grid-template-columns: 180px 1fr;
            }

            .cards {
                grid-template-columns: repeat(2, minmax(0, 1fr));
            }
        }

        /* Desktop */
        @media (min-width: 900px) {
            .layout {
                grid-template-columns: 230px 1fr;
                gap: 25px;
                padding: 25px;
            }

            .cards {
                grid-template-columns: repeat(4, minmax(0, 1fr));
            }
        }
    </style>
</head>
<body>

<header>
    <h1>My Dashboard</h1>
</header>

<div class="layout">
    <aside>
        <h3>Menu</h3>
        <p>Dashboard</p>
        <p>Students</p>
        <p>Courses</p>
        <p>Settings</p>
    </aside>

    <main>
        <h2>Overview</h2>
        <div class="cards">
            <div class="card">Students: 1200</div>
            <div class="card">Courses: 35</div>
            <div class="card">Assignments: 18</div>
            <div class="card">Pending Tasks: 7</div>
        </div>
    </main>
</div>

<footer>© 2026 My Dashboard</footer>

</body>
</html>
```
