<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Co-Funding Requests</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f6f9;
      margin: 0;
      padding: 20px;
    }
    h1 {
      text-align: center;
      margin-bottom: 20px;
    }
    .tabs {
      display: flex;
      justify-content: center;
      margin-bottom: 20px;
    }
    .tab {
      background: #fff;
      border: 1px solid #ccc;
      padding: 10px 20px;
      cursor: pointer;
      margin: 0 5px;
      border-radius: 5px;
    }
    .tab.active {
      background: #007bff;
      color: #fff;
      font-weight: bold;
    }
    .cards {
      max-width: 800px;
      margin: auto;
    }
    .card {
      background: #fff;
      border-radius: 10px;
      padding: 20px;
      margin-bottom: 15px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }
    .status {
      font-weight: bold;
      padding: 5px 10px;
      border-radius: 5px;
      display: inline-block;
      margin-bottom: 10px;
    }
    .pending { background: #fff3cd; color: #856404; }
    .active { background: #d4edda; color: #155724; }
    .accepted { background: #cce5ff; color: #004085; }
    .canceled { background: #f8d7da; color: #721c24; }
    .actions button {
      padding: 6px 12px;
      margin-right: 5px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .accept { background: #28a745; color: #fff; }
    .decline { background: #dc3545; color: #fff; }
    .view { background: #007bff; color: #fff; }
  </style>
</head>
<body>

  <h1>🤝 Co-Funding Requests (Mr A)</h1>

  <!-- Tabs -->
  <div class="tabs">
    <div class="tab active">Pending</div>
    <div class="tab">Active</div>
    <div class="tab">Accepted</div>
    <div class="tab">Canceled</div>
  </div>

  <!-- Request Cards -->
  <div class="cards">

    <!-- Pending -->
    <div class="card">
      <div class="status pending">🟡 Pending</div>
      <p><strong>Request ID:</strong> CF-2025-001</p>
      <p><strong>Requester:</strong> Mr A</p>
      <p><strong>Account Size:</strong> $10,000</p>
      <p><strong>Contribution:</strong> $5,000</p>
      <p><strong>Profit Split:</strong> 50/50</p>
      <p><strong>Created On:</strong> Sept 9, 2025</p>
      <div class="actions">
        <button class="accept">Accept</button>
        <button class="decline">Decline</button>
      </div>
    </div>

    <!-- Active -->
    <div class="card">
      <div class="status active">🟢 Active</div>
      <p><strong>Request ID:</strong> CF-2025-002</p>
      <p><strong>Requester:</strong> Mr A</p>
      <p><strong>Account Size:</strong> $20,000</p>
      <p><strong>Contribution:</strong> $10,000</p>
      <p><strong>Profit Split:</strong> 60/40</p>
      <p><strong>Started On:</strong> Sept 1, 2025</p>
      <div class="actions">
        <button class="view">View Agreement</button>
        <button class="view">Chat</button>
      </div>
    </div>

    <!-- Accepted -->
    <div class="card">
      <div class="status accepted">✅ Accepted</div>
      <p><strong>Request ID:</strong> CF-2025-003</p>
      <p><strong>Requester:</strong> Mr A</p>
      <p><strong>Account Size:</strong> $5,000</p>
      <p><strong>Contribution:</strong> $2,500</p>
      <p><strong>Profit Split:</strong> 50/50</p>
      <p><strong>Accepted On:</strong> Aug 28, 2025</p>
      <div class="actions">
        <button class="view">View Details</button>
      </div>
    </div>

    <!-- Canceled -->
    <div class="card">
      <div class="status canceled">🔴 Canceled</div>
      <p><strong>Request ID:</strong> CF-2025-004</p>
      <p><strong>Requester:</strong> Mr A</p>
      <p><strong>Account Size:</strong> $15,000</p>
      <p><strong>Contribution:</strong> $7,500</p>
      <p><strong>Profit Split:</strong> 70/30</p>
      <p><strong>Canceled On:</strong> Sept 5, 2025</p>
      <p><strong>Reason:</strong> Request withdrawn by Mr A</p>
    </div>

  </div>

</body>
</html>
