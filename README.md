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
      flex-wrap: wrap;
    }
    .tab {
      background: #fff;
      border: 1px solid #ccc;
      padding: 10px 20px;
      cursor: pointer;
      margin: 5px;
      border-radius: 5px;
    }
    .tab.active {
      background: #007bff;
      color: #fff;
      font-weight: bold;
    }
    .cards {
      max-width: 850px;
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
    <div class="tab active">Pending Requests</div>
    <div class="tab">Active Requests</div>
    <div class="tab">Accepted Requests</div>
    <div class="tab">Canceled Requests</div>
  </div>

  <!-- Request Cards -->
  <div class="cards">

    <!-- Pending -->
    <div class="card">
      <div class="status pending">🟡 Pending Request</div>
      <p><strong>Prop Firm:</strong> FTMO</p>
      <p><strong>Account Size:</strong> $1,000</p>
      <p><strong>Account Price:</strong> $15</p>
      <p><strong>Requester:</strong> Mr A</p>
      <p><strong>Contribution (50%):</strong> $7.50 each</p>
      <p><strong>Profit Split Agreement:</strong> 50/50</p>
      <p><strong>Requester Locked Amount:</strong> $7.50</p>
      <p><strong>Partner Locked Amount:</strong> Pending</p>
      <p><strong>Requirement:</strong> You must have at least <b>$7.50</b> available balance to accept</p>
      <div class="actions">
        <button class="accept">Accept & Lock Funds</button>
        <button class="decline">Decline</button>
      </div>
    </div>

    <!-- Active -->
    <div class="card">
      <div class="status active">🟢 Active Request</div>
      <p><strong>Prop Firm:</strong> FTMO</p>
      <p><strong>Account Size:</strong> $1,000</p>
      <p><strong>Account Price:</strong> $15</p>
      <p><strong>Requester:</strong> Mr A</p>
      <p><strong>Contribution (50%):</strong> $7.50 each</p>
      <p><strong>Profit Split Agreement:</strong> 50/50</p>
      <p><strong>Requester Locked Amount:</strong> $7.50</p>
      <p><strong>Partner Locked Amount:</strong> $7.50</p>
      <p>✅ Both contributions merged → <b>$15</b> account purchased successfully</p>
      <div class="actions">
        <button class="view">View Agreement</button>
        <button class="view">Chat with Partner</button>
      </div>
    </div>

    <!-- Accepted -->
    <div class="card">
      <div class="status accepted">✅ Accepted Request</div>
      <p><strong>Prop Firm:</strong> MyForexFunds</p>
      <p><strong>Account Size:</strong> $2,000</p>
      <p><strong>Account Price:</strong> $30</p>
      <p><strong>Requester:</strong> Mr A</p>
      <p><strong>Contribution (50%):</strong> $15 each</p>
      <p><strong>Profit Split Agreement:</strong> 60/40</p>
      <p><strong>Requester Locked Amount:</strong> $15</p>
      <p><strong>Partner Locked Amount:</strong> $15</p>
      <p>🔒 Account purchase scheduled after verification</p>
      <div class="actions">
        <button class="view">View Details</button>
      </div>
    </div>

    <!-- Canceled -->
    <div class="card">
      <div class="status canceled">🔴 Canceled Request</div>
      <p><strong>Prop Firm:</strong> E8 Funding</p>
      <p><strong>Account Size:</strong> $5,000</p>
      <p><strong>Account Price:</strong> $50</p>
      <p><strong>Requester:</strong> Mr A</p>
      <p><strong>Contribution (50%):</strong> $25 each</p>
      <p><strong>Profit Split Agreement:</strong> 70/30</p>
      <p><strong>Requester Locked Amount:</strong> Refunded ($25)</p>
      <p><strong>Partner Locked Amount:</strong> Not Provided</p>
      <p><strong>Status:</strong> Request canceled (Partner declined / Insufficient balance)</p>
    </div>

  </div>

</body>
</html>
