<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>DivoraSplit - Co-Funding Requests</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f6f8;
      margin: 0;
      padding: 20px;
    }
    h1 {
      text-align: center;
      margin-bottom: 20px;
    }
    .request {
      background: white;
      padding: 15px;
      margin-bottom: 15px;
      border-radius: 10px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }
    .status {
      font-weight: bold;
      margin-top: 10px;
    }
    .pending { color: orange; }
    .active { color: green; }
    .accepted { color: blue; }
    .canceled { color: red; }
    .actions button {
      margin: 5px 5px 0 0;
      padding: 6px 12px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .accept { background: #28a745; color: white; }
    .decline { background: #dc3545; color: white; }
    .view { background: #007bff; color: white; }
  </style>
</head>
<body>
  <h1>🤝 Co-Funding Requests</h1>
  <div id="requests"></div>

  <script>
    // Replace with your MockAPI.io endpoint after setup
    const API_URL = "https://YOUR-MOCKAPI-ENDPOINT/cofunding";

    // Helper to render each request
    function renderRequest(r) {
      return `
        <div class="request">
          <h3>${r.propFirm} – ${r.accountSize} (Price: $${r.accountPrice})</h3>
          <p><strong>Requester:</strong> ${r.requester}</p>
          <p><strong>Contribution Split:</strong> ${r.contributionSplit}</p>
          <p><strong>Requester Locked:</strong> $${r.requesterLocked}</p>
          <p><strong>Partner Locked:</strong> ${r.partnerLocked !== null ? "$" + r.partnerLocked : "Pending"}</p>
          <p><strong>Profit Split Agreement:</strong> ${r.contributionSplit}</p>
          <p class="status ${r.status.toLowerCase()}">Status: ${r.status}</p>
          <p>${r.note}</p>
          <div class="actions">
            ${r.status === "Pending" ? `
              <button class="accept">Accept & Lock Funds</button>
              <button class="decline">Decline</button>
            ` : ""}
            ${r.status === "Active" ? `
              <button class="view">View Agreement</button>
              <button class="view">Chat with Partner</button>
            ` : ""}
            ${r.status === "Accepted" ? `
              <button class="view">View Details</button>
            ` : ""}
          </div>
        </div>
      `;
    }

    // Fetch and display
    fetch(API_URL)
      .then(res => res.json())
      .then(data => {
        document.getElementById("requests").innerHTML = data.map(renderRequest).join("");
      })
      .catch(err => {
        console.error("Error fetching data:", err);
      });
  </script>
</body>
</html>
