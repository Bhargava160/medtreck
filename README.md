<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>MedTrack – Digital Health Record Tracker</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" />
  <style>
    body {
      background-color: #92f41b;
    }
    .hero {
      padding: 100px 0;
    }
  </style>
</head>
<body>
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container">
      <a class="navbar-brand" href="#">MedTrack</a>
      <div>
        <a href="login.html" class="btn btn-light me-2">Login</a>
        <a href="register.html" class="btn btn-outline-light">Register</a>
      </div>
    </div>
  </nav>

  <section class="hero text-center">
    <div class="container">
      <h1 class="display-4">Your Digital Health Companion</h1>
      <p class="lead">Securely store, manage, and share your health records with MedTrack</p>
      <a href="get-started.html" class="btn btn-primary btn-lg mt-3">Get Started</a>
    </div>
  </section>

  <footer class="bg-dark text-white text-center p-3">
    <p>&copy; 2025 MedTrack. All rights reserved.</p>
  </footer>
  <script>
    


function showAlert(message, type = 'success') {
  const alertBox = document.createElement('div');
  alertBox.className = `alert alert-${type}`;
  alertBox.innerText = message;
  alertBox.style.marginTop = '10px';
  document.body.prepend(alertBox);

  setTimeout(() => alertBox.remove(), 3000);
}


document.addEventListener('DOMContentLoaded', () => {
  const loginForm = document.getElementById('loginForm');
  const registerForm = document.getElementById('registerForm');
  const uploadInput = document.getElementById('recordUpload');
  const filePreview = document.getElementById('filePreview');

  if (loginForm) {
    loginForm.addEventListener('submit', (e) => {
      e.preventDefault();

      const email = loginForm.email.value.trim();
      const password = loginForm.password.value;

      if (!email || !password) {
        showAlert('Please fill in all fields', 'danger');
        return;
      }

      
      showAlert('Login successful (mock)', 'success');
    });
  }

  if (registerForm) {
    registerForm.addEventListener('submit', (e) => {
      e.preventDefault();

      const name = registerForm.name.value.trim();
      const email = registerForm.email.value.trim();
      const password = registerForm.password.value;
      const role = registerForm.role.value;

      if (!name || !email || !password || !role) {
        showAlert('Please fill all fields', 'danger');
        return;
      }

      
      showAlert(`Registered as ${role}`, 'success');
    });
  }

  if (uploadInput && filePreview) {
    uploadInput.addEventListener('change', () => {
      const file = uploadInput.files[0];
      if (file) {
        filePreview.innerText = `Selected file: ${file.name}`;
      } else {
        filePreview.innerText = '';
      }
    });
  }
});

  </script>
</body>
</html>