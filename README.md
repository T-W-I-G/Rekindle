<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rekindle</title>
    <link href="https://i.imgur.com/f1l3qXa.png" rel="stylesheet">
    <style>
        body {
            font-family: 'system-ui';
            margin: 0;
            padding: 0;
            background: #1c0000;
            color: #ffffff;
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: flex-start;
            height: 80vh;
            overflow: hidden;
        }
        .image-container {
            position: fixed;
            top: 0;
            left: 5%;  /* Adds left margin */
            width: 40%;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .image-container img {
            max-width: 100%;
            max-height: 100vh;
            width: auto;
            height: auto;
            object-fit: contain;
            margin-right: 5%; /* Adds right margin */
        }
        .content {
            flex: 1;
            padding: 20px;
            margin-left: 42%;
            height: 100vh;
            overflow-y: auto;
            text-align: center;
        }
        h1 {
            font-size: 36px;
            color: #c9c6c6;
            margin-bottom: 10px;
            text-align: center; /* Aligns text to the right */
            margin-right: 20px; /* Ensures consistent spacing */
        }
        p {
            font-size: 18px;
            line-height: 1.8;
            margin: 10px 20px;
            max-width: 800px;
        }
        a {
            color: red; /* Makes the link red */
            text-decoration: none; /* Removes the underline (optional) */
            text-align: center;
        }

        a:hover {
            color: darkred; /* Changes color when hovered (optional) */
        }

    </style>
</head>
<body>
    <script>
        document.addEventListener("DOMContentLoaded", function () {
            let elements = document.querySelectorAll(".zoom-effect");
    
            let observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add("visible");
                    } else {
                        entry.target.classList.remove("visible"); // Allows repeated zooming
                    }
                });
            }, { threshold: 0.1 }); // Lower threshold triggers animation sooner
    
            elements.forEach(element => {
                observer.observe(element);
            });
        });
    </script>    
    <div class="image-container">
        <img src="https://i.imgur.com/f1l3qXa.png" alt="Rekindle Banner" class="zoom-effect">
    </div>
    <div class="content">
        <h1>REKINDLE</h1>
        <p>Gathering the tree planting folk on the East coast to connect and celebrate through our long-awaited pre-season party</p>
        <p><strong>March 21, 2025<br>9PM - LATE<br>LOCATION: TBA</strong></p>
        <br>
        <a href="" target="_blank"><strong> - - - TICKETS AVAILABLE SOON - - - </strong></a>
        <br>
        <br>
        <p><strong>SCHEDULE</strong></p>
        <p><strong>8-11:</strong>
            <br>Market vendors
            <br>Art installations
            <br>Live music and dance performances
        <br>
        <br><strong>11-late:</strong>
            <br>Time to rave
            <br>DJ performances (stay tuned for line-up)</p>
        <br>
        <br> This event is <strong>BYOB</strong>
        <br>
        <br>
        <p>If you wish to contribute to this event in any way, please reach out through our Facebook page or via email!
        <br>__add email here__</p>
        <br>
        <br>
    </div>
</body>
</html>
