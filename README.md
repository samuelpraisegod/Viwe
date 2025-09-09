<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Sign Up - DivoraSplit</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #0d6efd, #6610f2);
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .signup-container {
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.15);
      width: 350px;
      text-align: center;
    }
    .signup-container h1 {
      margin-bottom: 10px;
      font-size: 24px;
      color: #333;
    }
    .signup-container p {
      margin-bottom: 20px;
      font-size: 14px;
      color: #666;
    }
    .btn {
      width: 100%;
      padding: 10px;
      margin: 8px 0;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      font-size: 14px;
    }
    .btn-google {
      background: #db4437;
      color: white;
    }
    .btn-email {
      background: #0d6efd;
      color: white;
    }
    .input-field {
      width: 100%;
      padding: 10px;
      margin: 8px 0;
      border: 1px solid #ccc;
      border-radius: 6px;
      font-size: 14px;
    }
    .terms {
      font-size: 12px;
      color: #555;
      margin: 10px 0;
      text-align: left;
    }
    .terms a {
      color: #0d6efd;
      text-decoration: none;
    }
    .checkbox {
      display: flex;
      align-items: center;
      margin-bottom: 15px;
      font-size: 12px;
      color: #555;
      text-align: left;
    }
    .checkbox input {
      margin-right: 6px;
    }
    .link {
      margin-top: 15px;
      font-size: 13px;
    }
    .link a {
      color: #0d6efd;
      text-decoration: none;
    }
  </style>
</head>
<body>
  <div class="signup-container">
    <h1>Create Account</h1>
    <p>Unlock limitless trading opportunities</p>
    
    <button class="btn btn-google">Sign up with Google</button>
    <p>or Sign up with Email</p>
    
    <form>
      <input type="text" class="input-field" placeholder="Full Name" required>
      <input type="email" class="input-field" placeholder="Email" required>
      <input type="password" class="input-field" placeholder="Password" required>
      
      <p class="terms">
        By signing up, you agree to our <a href="#">Terms of Use</a> and <a href="#">Privacy Policy</a>.
      </p>
      
      <div class="checkbox">
        <input type="checkbox" id="consent">
        <label for="consent">I consent to receive marketing emails.</label>
      </div>
      
      <button type="submit" class="btn btn-email">Sign Up</button>
    </form>
    
    <div class="link">
      Already have an account? <a href="#">Log in</a>
    </div>
  </div>
</body>
</html>
