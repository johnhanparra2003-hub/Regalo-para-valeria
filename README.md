# Regalo-para-valeria
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Un Detalle Para Ti</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #2c3e50;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            color: white;
            font-family: 'Georgia', serif;
        }

        .contenedor-rosa {
            position: relative;
            text-align: center;
        }

        .rosa-principal {
            width: 150px;
            height: auto;
            animation: aparecer 2s ease-out;
            filter: drop-shadow(0 0 20px rgba(255, 105, 180, 0.8));
        }

        .mensaje {
            margin-top: 20px;
            font-size: 1.5rem;
            opacity: 0;
            animation: aparecerTexto 2s ease-out 1s forwards;
            line-height: 1.8;
        }

        @keyframes aparecer {
            from { opacity: 0; transform: scale(0.5); }
            to { opacity: 1; transform: scale(1); }
        }

        @keyframes aparecerTexto {
            to { opacity: 1; }
        }

        .petalo {
            position: fixed;
            top: -10px;
            background-color: #ff69b4;
            border-radius: 50%;
            opacity: 0.8;
            pointer-events: none;
            animation: caer linear infinite;
            box-shadow: 0 0 10px rgba(255, 105, 180, 0.6);
        }

        @keyframes caer {
            0% {
                top: -10px;
                transform: translateX(0) rotate(0deg);
            }
            100% {
                top: 100vh;
                transform: translateX(100px) rotate(360deg);
            }
        }
    </style>
</head>
<body>

    <div class="contenedor-rosa">
        <svg width="150" height="150" viewBox="0 0 150 150" class="rosa-principal">
            <g transform="translate(75, 75)">
                <!-- Pétalos externos rojos -->
                <ellipse cx="0" cy="-35" rx="18" ry="28" fill="#dc143c" transform="rotate(0)"/>
                <ellipse cx="0" cy="-35" rx="18" ry="28" fill="#dc143c" transform="rotate(45)"/>
                <ellipse cx="0" cy="-35" rx="18" ry="28" fill="#dc143c" transform="rotate(90)"/>
                <ellipse cx="0" cy="-35" rx="18" ry="28" fill="#dc143c" transform="rotate(135)"/>
                <ellipse cx="0" cy="-35" rx="18" ry="28" fill="#dc143c" transform="rotate(180)"/>
                <ellipse cx="0" cy="-35" rx="18" ry="28" fill="#dc143c" transform="rotate(225)"/>
                <ellipse cx="0" cy="-35" rx="18" ry="28" fill="#dc143c" transform="rotate(270)"/>
                <ellipse cx="0" cy="-35" rx="18" ry="28" fill="#dc143c" transform="rotate(315)"/>
                
                <!-- Pétalos internos rosa oscuro -->
                <ellipse cx="0" cy="-25" rx="15" ry="22" fill="#ff1493" transform="rotate(22.5)"/>
                <ellipse cx="0" cy="-25" rx="15" ry="22" fill="#ff1493" transform="rotate(67.5)"/>
                <ellipse cx="0" cy="-25" rx="15" ry="22" fill="#ff1493" transform="rotate(112.5)"/>
                <ellipse cx="0" cy="-25" rx="15" ry="22" fill="#ff1493" transform="rotate(157.5)"/>
                <ellipse cx="0" cy="-25" rx="15" ry="22" fill="#ff1493" transform="rotate(202.5)"/>
                <ellipse cx="0" cy="-25" rx="15" ry="22" fill="#ff1493" transform="rotate(247.5)"/>
                <ellipse cx="0" cy="-25" rx="15" ry="22" fill="#ff1493" transform="rotate(292.5)"/>
                <ellipse cx="0" cy="-25" rx="15" ry="22" fill="#ff1493" transform="rotate(337.5)"/>
                
                <!-- Centro de la rosa -->
                <circle cx="0" cy="0" r="12" fill="#ffb6c1"/>
                <circle cx="0" cy="0" r="8" fill="#ffc0cb"/>
            </g>
        </svg>
        
        <div class="mensaje">
            <p>He cambiado las flores amarillas por rosas,</p>
            <p>porque son tan especiales como tú.</p>
            <p>Te amo, Valeria 💕</p>
            <p><strong>Con todo mi cariño</strong></p>
        </div>
    </div>

    <script>
        function crearPetalo() {
            const petalo = document.createElement('div');
            petalo.classList.add('petalo');
            
            petalo.style.left = Math.random() * 100 + "vw";
            
            const size = Math.random() * 15 + 8 + "px";
            petalo.style.width = size;
            petalo.style.height = size;
            
            petalo.style.animationDuration = Math.random() * 3 + 2 + "s";
            
            document.body.appendChild(petalo);

            setTimeout(() => {
                petalo.remove();
            }, 5000);
        }

        setInterval(crearPetalo, 300);
    </script>

</body>
</html>
