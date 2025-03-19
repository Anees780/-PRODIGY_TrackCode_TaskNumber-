# -PRODIGY_TrackCode_TaskNumber-
Web Development
Task 1
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            padding-top: 80px; /* Space for fixed navigation */
        }

        .nav-bar {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(0, 0, 0, 0.7);
            padding: 1rem 0;
            transition: all 0.3s ease;
            z-index: 1000;
        }

        .nav-bar.scrolled {
            background: #ffffff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .nav-bar ul {
            list-style: none;
            display: flex;
            justify-content: center;
            margin: 0;
            padding: 0;
        }

        .nav-bar li {
            margin: 0 20px;
        }

        .nav-bar a {
            color: white;
            text-decoration: none;
            font-size: 1.1rem;
            transition: color 0.3s, transform 0.2s;
        }

        .nav-bar.scrolled a {
            color: #333;
        }

        .nav-bar a:hover {
            color: #007bff;
            transform: translateY(-2px);
        }

        /* Content section for demonstration */
        .content {
            height: 2000px;
            padding: 20px;
            text-align: center;
        }
    </style>
</head>
<body>
    <nav class="nav-bar" id="navBar">
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <div class="content">
        <h1>Scroll Down to See Navigation Effect</h1>
        <p>(Sample content for demonstration)</p>
    </div>

    <script>
        // Scroll effect for navigation
        window.addEventListener('scroll', function() {
            const navBar = document.getElementById('navBar');
            if (window.scrollY > 50) {
                navBar.classList.add('scrolled');
            } else {
                navBar.classList.remove('scrolled');
            }
        });

        // Hover effect for menu items
        document.querySelectorAll('.nav-bar a').forEach(link => {
            link.addEventListener('mouseover', function() {
                this.style.transition = 'all 0.3s ease';
            });
            
            link.addEventListener('mouseout', function() {
                this.style.transform = 'translateY(0)';
            });
        });
    </script>
</body>
</html>
