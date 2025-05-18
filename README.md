# supreme-octo-garbanzo
arte plásticas 
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Mi Galería de Arte</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: #f7f7f7;
    }
    header {
      background-color: #333;
      color: white;
      padding: 20px;
      text-align: center;
    }
    h1 {
      margin: 0;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 15px;
      padding: 20px;
    }
    .gallery img {
      width: 100%;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }
    .upload {
      text-align: center;
      margin: 30px;
    }
    input[type="file"] {
      display: none;
    }
    label.upload-btn {
      background-color: #333;
      color: white;
      padding: 10px 20px;
      border-radius: 8px;
      cursor: pointer;
    }
    footer {
      background-color: #333;
      color: white;
      padding: 20px;
      text-align: center;
    }
    form {
      max-width: 400px;
      margin: auto;
      padding: 20px;
    }
    input, textarea {
      width: 100%;
      margin: 10px 0;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 6px;
    }
    button {
      padding: 10px 20px;
      border: none;
      background-color: #444;
      color: white;
      border-radius: 6px;
      cursor: pointer;
    }
  </style>
</head>
<body>

<header>
  <h1>Mi Galería de Arte</h1>
  <p>Descubre mis dibujos y pinturas</p>
</header>

<section class="gallery" id="gallery">
  <!-- Aquí puedes añadir tus imágenes -->
  <img src="https://via.placeholder.com/300x200?text=Dibujo+1" alt="Dibujo 1">
  <img src="https://via.placeholder.com/300x200?text=Dibujo+2" alt="Dibujo 2">
  <img src="https://via.placeholder.com/300x200?text=Dibujo+3" alt="Dibujo 3">
</section>

<section class="upload">
  <label class="upload-btn" for="uploadInput">Subir nuevo dibujo</label>
  <input type="file" id="uploadInput" accept="image/*">
</section>

<section>
  <form>
    <h2>Contacto</h2>
    <input type="text" placeholder="Tu nombre" required>
    <input type="email" placeholder="Tu correo" required>
    <textarea rows="4" placeholder="Mensaje..."></textarea>
    <button type="submit">Enviar</button>
  </form>
</section>

<footer>
  © 2025 Tu Nombre | Web creada con ayuda de <a href="http://gptonline.ai/es" style="color: #ccc;">gptonline.ai/es</a>
</footer>

<script>
  const uploadInput = document.getElementById('uploadInput');
  const gallery = document.getElementById('gallery');

  uploadInput.addEventListener('change', (e) => {
    const file = e.target.files[0];
    if (file && file.type.startsWith('image/')) {
      const reader = new FileReader();
      reader.onload = () => {
        const img = document.createElement('img');
        img.src = reader.result;
        gallery.appendChild(img);
      };
      reader.readAsDataURL(file);
    }
  });
</script>

</body>
</html>
