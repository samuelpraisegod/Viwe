<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Co-Funding Dashboard</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f6f9;
      margin: 0;
      padding: 20px;
    }
    h2 {
      color: #333;
    }
    .tabs {
      display: flex;
      gap: 15px;
      margin-bottom: 20px;
    }
    .tab {
      padding: 10px 20px;
      background: #e0e0e0;
      border-radius: 6px;
      cursor: pointer;
      font-weight: bold;
    }
    .tab.active {
      background: #007bff;
      color: white;
    }
    .card {
      background: white;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      margin-bottom: 15px;
    }
    .status {
      font-weight: bold;
      margin-top: 10px;
    }
    .status.pending { color: orange; }
    .status.active { color: green; }
    .status.accepted { color: blue; }
    .status.canceled { color: red; }
    .actions button {
      padding: 8px 14px;
      margin-right: 10px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
    }
    .accept { background: #28a745; color: white; }
    .decline { background: #dc3545; color: white; }
    .view { background: #007bff; color: white; }
  </style>
</head>
<body>

  <h2>🤝 Co-Funding Requests</h2>

  <!-- Tabs -->
  <div class="tabs">
    <div class="tab active">Pending Requests</div>
    <div class="tab">Active Requests</div>
    <div class="tab">Accepted Requests</div>
    <div class="tab">Canceled Requests</div>
  </div>

  <!-- Pending Request (Private) -->
  <div class="card">
    <h3>Prop Firm: FTMO</h3>
    <p><strong>Account Size:</strong> $1,000</p>
    <p><strong>Account Price:</strong> $15</p>
    <p><strong>Requester:</strong> Mr A</p>
    <p><strong>Contribution Split:</strong> $7.50 each</p>
    <p><strong>Requester Locked Amount:</strong> $7.50</p>
    <p><strong>Partner Required:</strong> $7.50 (must accept & lock)</p>
    <p><strong>Profit Split Agreement:</strong> 50/50</p>
    <p class="status pending">🟡 Status: Pending (Private – only Mr A & tagged partner can see)</p>
    <div class="actions">
      <button class="accept">Accept & Lock Funds</button>
      <button class="decline">Decline</button>
    </div>
  </div>

  <!-- Active Request -->
  <div class="card">
    <h3>Prop Firm: FTMO</h3>
    <p><strong>Account Size:</strong> $1,000</p>
    <p><strong>Account Price:</strong> $15</p>
    <p><strong>Both Contributions Locked:</strong> $7.50 + $7.50</p>
    <p><strong>Profit Split Agreement:</strong> 50/50</p>
    <p class="status active">🟢 Status: Active (Account Purchased)</p>
    <div class="actions">
      <button class="view">View Agreement</button>
      <button class="view">Chat with Partner</button>
    </div>
  </div>

  <!-- Accepted Request -->
  <div class="card">
    <h3>Prop Firm: MyForexFunds</h3>
    <p><strong>Account Size:</strong> $2,000</p>
    <p><strong>Account Price:</strong> $30</p>
    <p><strong>Contribution Split:</strong> $15 each</p>
    <p><strong>Locked Amounts:</strong> $15 + $15</p>
    <p><strong>Profit Split Agreement:</strong> 60/40</p>
    <p class="status accepted">✅ Status: Accepted (Waiting for system purchase)</p>
    <div class="actions">
      <button class="view">View Details</button>
    </div>
  </div>

  <!-- Canceled Request -->
  <div class="card">
    <h3>Prop Firm: E8 Funding</h3>
    <p><strong>Account Size:</strong> $5,000</p>
    <p><strong>Account Price:</strong> $50</p>
    <p><strong>Requester:</strong> Mr A</p>
    <p><strong>Contribution:</strong> $25</p>
    <p><strong>Locked Amount:</strong> Refunded</p>
    <p><strong>Profit Split Agreement:</strong> 70/30</p>
    <p class="status canceled">🔴 Status: Canceled (Partner declined or insufficient balance)</p>
  </div>

</body>
</html>
