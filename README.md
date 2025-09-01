[index.html](https://github.com/user-attachments/files/22083478/index.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Oficina Fácil PWA</title>
<link rel="manifest" href="manifest.webmanifest">
<meta name="theme-color" content="#0ea5e9">
<link rel="icon" href="icons/icon-192.png" sizes="192x192">
<link rel="apple-touch-icon" href="icons/icon-192.png">
<link rel="stylesheet" href="styles.css">
</head>
<body>
<header class="topbar">
<h1>🔧 Oficina Fácil</h1>
</header>
<main class="container">
<section class="card">
<h2>Novo Serviço</h2>
<form id="serviceForm">
<div class="grid">
<label class="field"><span>Placa *</span><input type="text" id="plate" placeholder="ABC1D23" required maxlength="7"/></label>
<label class="field"><span>Valor (R$) *</span><input type="text" id="value" placeholder="150,00" inputmode="decimal" required/></label>
</div>
<label class="field"><span>Serviço realizado *</span><textarea id="service" rows="3" required></textarea></label>
<label class="field"><span>Foto (opcional)</span><input type="file" id="photo" accept="image/*" capture="environment"></label>
<div class="actions">
<button type="submit" class="btn">Salvar</button>
<button type="reset" class="btn ghost">Limpar</button>
</div>
</form>
</section>
<section class="card">
<h2>Registros</h2>
<input id="search" type="search" placeholder="Buscar por placa..." />
<div id="list" class="list"></div>
<p id="emptyState" class="muted" hidden>Nenhum registro ainda.</p>
<div class="actions">
<button id="exportBtn" class="btn ghost">Exportar JSON</button>
<input type="file" id="importFile" style="display:none">
<button id="importBtn" class="btn ghost">Importar JSON</button>
</div>
</section>
</main>
<footer class="footer">
<span>Todos os registros ficam no celular</span>
</footer>
<script src="app.js"></script>
</body>
</html>
