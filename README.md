@echo off
echo Criando o site Lumora 2.0...
(
echo ^<!DOCTYPE html^>
echo ^<html lang="pt-BR"^>
echo ^<head^>
echo   ^<meta charset="UTF-8" /^>
echo   ^<meta name="viewport" content="width=device-width, initial-scale=1"^>
echo   ^<title>Lumora • Casa & Decoração^</title^>
echo   ^<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@picocss/pico@1/css/pico.min.css"^>
echo   ^<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet"^>
echo   ^<style^>
echo     body {font-family: 'Poppins', sans-serif;background-color: #f8f8f8;color: #333;}
echo     nav strong {color:#bfa56a;font-size:1.3rem;}
echo     .hero {text-align:center;padding:5rem 1rem;background:linear-gradient(135deg,#fafafa,#e8e8e8);border-radius:12px;}
echo     .product-card {background:#fff;border-radius:10px;padding:1rem;box-shadow:0 3px 10px rgba(0,0,0,0.1);}
echo   ^</style^>
echo ^</head^>
echo ^<body^>
echo   ^<nav class="container-fluid"^>
echo     ^<ul^>^<li^>^<strong^>Lumora^</strong^>^</li^>^</ul^>
echo     ^<ul^>^<li^>^<a href="#"^>Início^</a^>^</li^>^<li^>^<a href="#produtos"^>Coleção^</a^>^</li^>^</ul^>
echo   ^</nav^>
echo   ^<main class="container"^>
echo     ^<section class="hero"^>
echo       ^<h1^>Seu lar, seu estilo.^</h1^>
echo       ^<p^>Descubra a elegância em cada detalhe com a coleção Lumora.^</p^>
echo     ^</section^>
echo   ^</main^>
echo ^</body^>
echo ^</html^>
) > index.html

echo Compactando arquivo...
powershell Compress-Archive -Path index.html -DestinationPath lumora.zip -Force
echo.
echo ✅ Arquivo lumora.zip criado com sucesso!
pa
