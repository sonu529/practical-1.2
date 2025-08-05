<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Responsive Banking UI</title>
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f0f2f5;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 20px;
    }
    .banking-container {
      background: white;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      max-width: 400px;
      width: 100%;
      padding: 30px 25px;
      text-align: center;
    }
    .balance-display {
      background: #4a90e2;
      color: rgb(226, 221, 221);
      font-size: 1.5rem;
      font-weight: bold;
      padding: 20px;
      border-radius: 10px;
      margin-bottom: 30px;
    }
    .actions {
      display: flex;
      justify-content: space-between;
      gap: 15px;
      margin-bottom: 30px;
    }
    button {
      flex: 1;
      padding: 15px 0;
      font-size: 1rem;
      font-weight: 600;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    button.deposit {
      background-color: #27ae60;
      color: white;
    }
    button.deposit:hover {
      background-color: #219150;
    }
    button.withdraw {
      background-color: #e74c3c;
      color: white;
    }
    button.withdraw:hover {
      background-color: #c0392b;
    }
    @media (max-width: 480px) {
      .actions {
        flex-direction: column;
      }
      button {
        width: 100%;
      }
    }
  </style>
</head>
<body>
  <div class="banking-container" role="main" aria-label="Banking interface">
    <div class="balance-display" aria-live="polite">
      Available balance: 0$
    </div>
    <div class="actions">
      <button class="deposit" type="button" aria-label="Deposit">Deposit</button>
      <button class="withdraw" type="button" aria-label="Withdraw">Withdraw</button>
    </div>
  </div>
</body>
</html>
