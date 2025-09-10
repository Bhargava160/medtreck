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


Navigation Menu
Bhargava160
medtreck

Code
Issues
Pull requests
Actions
Projects
Wiki
Security
Insights
Commit e87dd9d
Bhargava160
Bhargava160
authored
1 hour ago
Verified
Add files via upload
main
1 parent 
21985c2
 commit 
e87dd9d
File tree
Filter files…
a.html
doctor.html
get-started.html
login.html
register.html
5 files changed
+495
-0
lines changed
Search within code
 
‎a.html
+111
Lines changed: 111 additions & 0 deletions
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,111 @@
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
‎doctor.html
+123
Lines changed: 123 additions & 0 deletions
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,123 @@
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Register – MedTrack</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" />
  <link rel="stylesheet" href="css/style.css" />
</head>
<body>
  
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container">
      <a class="navbar-brand" href="index.html">MedTrack</a>
    </div>
  </nav>
  
  <div class="container form-container mt-5">
    <h2>Register</h2>
    <form id="registerForm">
      <div class="mb-3">
        <label for="name" class="form-label">Full Name</label>
        <input type="text" name="name" class="form-control" id="name" placeholder="ANKIT SINGH" required />
      </div>
      <div class="mb-3">
        <label for="email" class="form-label">Email Address</label>
        <input type="email" name="email" class="form-control" id="email" placeholder="name@example.com" required />
      </div>
      <div class="mb-3">
        <label for="password" class="form-label">Password</label>
        <input type="password" name="password" class="form-control" id="password" required />
      </div>
      <div class="mb-3">
        <label for="role" class="form-label">Register as</label>
        <select name="role" id="role" class="form-select" required>
          <option value="">Select role</option>
          <option value="patient">Patient</option>
          <option value="doctor">Doctor</option>
        </select>
      </div>
      
      <div id="doctorFields" style="display:none;">
        <div class="mb-3">
          <label for="specialization" class="form-label">Specialization</label>
          <input type="text" name="specialization" class="form-control" id="specialization" placeholder="Cardiologist, Neurologist, etc." />
        </div>
        <div class="mb-3">
          <label for="license" class="form-label">Medical License Number</label>
          <input type="text" name="license" class="form-control" id="license" placeholder="e.g. DMC123456" />
        </div>
        <div class="mb-3">
          <label for="experience" class="form-label">Years of Experience</label>
          <input type="number" name="experience" class="form-control" id="experience" placeholder="e.g. 5" />
        </div>
      </div>
      <button type="submit" class="btn btn-primary w-100">Create Account</button>
    </form>
    <p class="text-center mt-3">
      Already have an account? <a href="login.html">Login here</a>
    </p>
  </div>
  <footer class="bg-dark text-white text-center p-3 mt-5">
    <p>&copy; 2025 MedTrack. All rights reserved.</p>
  </footer>
  
  <script>
    const roleSelect = document.getElementById("role");
    const doctorFields = document.getElementById("doctorFields");
    roleSelect.addEventListener("change", function () {
      if (this.value === "doctor") {
        doctorFields.style.display = "block";
      } else {
        doctorFields.style.display = "none";
      }
    });
    document.getElementById("registerForm").addEventListener("submit", async function (e) {
      e.preventDefault();
      const formData = {
        name: document.getElementById("name").value,
        email: document.getElementById("email").value,
        password: document.getElementById("password").value,
        role: document.getElementById("role").value,
        specialization: document.getElementById("specialization").value,
        license: document.getElementById("license").value,
        experience: document.getElementById("experience").value,
      };
      //
      try {
        const res = await fetch("http://localhost:5000/api/auth/register", {
          method: "POST",
          headers: { "Content-Type": "application/json" },
          body: JSON.stringify(formData),
        });
        const data = await res.json();
        alert(data.msg || "Registration successful!");
      } catch (error) {
        console.error("Error:", error);
        alert("Something went wrong. Please try again.");
      }
    });
  </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Get Started – MedTrack</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" />
  <link rel="stylesheet" href="css/style.css" />
  <style>
    .get-started {
      padding: 80px 0;
      text-align: center;
    }

    .card-option {
      border-radius: 12px;
      padding: 30px;
      transition: all 0.3s ease;
      border: 1px solid #000000;
    }

    .card-option:hover {
      box-shadow: 0px 8px 20px rgba(0, 123, 255, 0.15);
      transform: translateY(-5px);
    }

    .card-option h3 {
      color: #ff0000;
    }
  </style>
</head>
<body>

  
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container">
      <a class="navbar-brand" href="index.html">MedTrack</a>
    </div>
  </nav>

  <section class="get-started container">
    <h1 class="mb-4">Get Started with MedTrack</h1>
    <p class="lead mb-5">Choose how you'd like to use the platform</p>

    <div class="row justify-content-center">
      <div class="col-md-5 mb-4">
        <div class="card-option">
          <h3>I'm a Patient</h3>
          <p>Upload and manage your health records digitally, and share with doctors when needed.</p>
          <a href="register.html" class="btn btn-primary">Register as Patient</a>
        </div>
      </div>

      <div class="col-md-5 mb-4">
        <div class="card-option">
          <h3>I'm a Doctor</h3>
          <p>Access shared patient records with consent and leave treatment notes.</p>
          <a href="register.html" class="btn btn-outline-primary">Register as Doctor</a>
        </div>
      </div>
    </div>
  </section>

  <footer class="bg-dark text-white text-center p-3">
    <p>&copy; 2025 MedTrack. All rights reserved.</p>
  </footer>

</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Login – MedTrack</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" />
  <link rel="stylesheet" href="css/style.css" />
</head>
<style>
    


.form-container {
  max-width: 450px;
  margin: 60px auto;
  padding: 30px 25px;
  background-color: #af1717;
  border-radius: 10px;
  box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.05);
}

.form-container h2 {
  text-align: center;
  margin-bottom: 25px;
  font-weight: bold;
  color: #1cbc0b;
}

.form-label {
  font-weight: 500;
}

.form-select,
.form-control {
  border-radius: 5px;
}

.btn-primary {
  background-color: #18da38;
  border-color: #000901;
}

.btn-primary:hover {
  background-color: #da20ae;
}


footer {
  margin-top: 80px;
}

</style>
<body>

  
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container">
      <a class="navbar-brand" href="index.html">MedTrack</a>
    </div>
  </nav>

  <div class="container form-container mt-5">
    <h2>Login</h2>
    <form id="loginForm">
      <div class="mb-3">
        <label for="email" class="form-label">Email address</label>
        <input type="email" name="email" class="form-control" id="email" placeholder="name@example.com" required />
      </div>

      <div class="mb-3">
        <label for="password" class="form-label">Password</label>
        <input type="password" name="password" class="form-control" id="password" required />
      </div>

      <div class="mb-3">
        <label for="role" class="form-label">Login as</label>
        <select name="role" id="role" class="form-select" required>
          <option value="patient">Patient</option>
          <option value="doctor">Doctor</option>
        </select>
      </div>

      <button type="submit" class="btn btn-primary w-100">Login</button>
    </form>

    <p class="text-center mt-3">
      Don't have an account? <a href="register.html">Register here</a>
    </p>
  </div>

  <footer class="bg-dark text-white text-center p-3 mt-5">
    <p>&copy; 2025 MedTrack. All rights reserved.</p>
  </footer>

  <script src="js/script.js"></script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Register – MedTrack</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" />
  <link rel="stylesheet" href="css/style.css" />
</head>
<body>

  
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container">
      <a class="navbar-brand" href="index.html">MedTrack</a>
    </div>
  </nav>

  
  <div class="container form-container mt-5">
    <h2>Register</h2>
    <form id="registerForm">
      <div class="mb-3">
        <label for="name" class="form-label">Full Name</label>
        <input type="text" name="name" class="form-control" id="name" placeholder="Ankit Singh" required />
      </div>

      <div class="mb-3">
        <label for="email" class="form-label">Email Address</label>
        <input type="email" name="email" class="form-control" id="email" placeholder="name@example.com" required />
      </div>

      <div class="mb-3">
        <label for="password" class="form-label">Password</label>
        <input type="password" name="password" class="form-control" id="password" required />
      </div>

      <div class="mb-3">
        <label for="role" class="form-label">Register as</label>
        <select name="role" id="role" class="form-select" required>
          <option value="">Select role</option>
          <option value="patient">Patient</option>
          <option value="doctor">Doctor</option>
        </select>
      </div>

      
      <div id="doctorFields" style="display: none;">
        <div class="mb-3">
          <label for="specialization" class="form-label">Specialization</label>
          <input type="text" name="specialization" class="form-control" id="specialization" placeholder="e.g. Cardiologist" />
        </div>

        <div class="mb-3">
          <label for="license" class="form-label">Medical License Number</label>
          <input type="text" name="license" class="form-control" id="license" placeholder="e.g. DMC123456" />
        </div>

        <div class="mb-3">
          <label for="experience" class="form-label">Years of Experience</label>
          <input type="number" name="experience" class="form-control" id="experience" placeholder="e.g. 5" />
        </div>
      </div>

      <button type="submit" class="btn btn-primary w-100">Create Account</button>
    </form>

    <p class="text-center mt-3">
      Already have an account? <a href="login.html">Login here</a>
    </p>
  </div>

  <footer class="bg-dark text-white text-center p-3 mt-5">
    <p>&copy; 2025 MedTrack. All rights reserved.</p>
  </footer>

  <script>
    const roleSelect = document.getElementById("role");
    const doctorFields = document.getElementById("doctorFields");

    
    roleSelect.addEventListener("change", function () {
      if (this.value === "doctor") {
        doctorFields.style.display = "block";
      } else {
        doctorFields.style.display = "none";
      }
    });
  </script>
</body>
</html>