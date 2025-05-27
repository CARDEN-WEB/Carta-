<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Una Carta de Amor</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="tree-container">
    <div class="tree"></div>
    <div class="heart-message" id="message">
      <h1>💖 Para ti, mi amor 💖</h1>
      <p>
        Como un árbol que florece con el sol, mi amor por ti crece cada día más.
        Tus palabras son mis raíces, tu sonrisa mi luz, y tu amor... mi razón de ser.
      </p>
      <p>
        Gracias por existir. Eres mi hogar, mi calma y mi inspiración.
        Te amo más de lo que las palabras pueden decir.
      </p>
      <p>Con todo mi amor, 🌳💌</p>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
body {
  margin: 0;
  font-family: 'Georgia', serif;
  background: linear-gradient(to top, #fceabb, #f8b500);
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  overflow: hidden;
}

.tree-container {
  position: relative;
  width: 300px;
  height: 400px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.tree {
  width: 100px;
  height: 150px;
  background: #2e7d32;
  border-radius: 0 0 50px 50px;
  animation: growTree 3s ease-in-out forwards;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
}

@keyframes growTree {
  0% {
    transform: scaleY(0);
    opacity: 0;
  }
  100% {
    transform: scaleY(1);
    opacity: 1;
  }
}

.heart-message {
  opacity: 0;
  transform: translateY(20px);
  text-align: center;
  padding: 20px;
  border-radius: 20px;
  background: #fff8f0;
  box-shadow: 0 4px 20px rgba(0,0,0,0.2);
  transition: all 1.2s ease;
  margin-top: 20px;
}

.heart-message h1 {
  font-size: 1.5rem;
  color: #c62828;
}

.heart-message p {
  font-size: 1rem;
  color: #4e342e;
  margin-top: 0.5em;
}
window.addEventListener("load", () => {
  setTimeout(() => {
    const message = document.getElementById("message");
    message.style.opacity = "1";
    message.style.transform = "translateY(0)";
  }, 3000); // Aparece después de que "crece" el árbol
});
