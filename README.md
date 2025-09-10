import React, { useEffect, useState } from "react";

export default function PropFirmList() { const [firms, setFirms] = useState([]); const [selectedFirm, setSelectedFirm] = useState(null);

useEffect(() => { // Fetch all prop firms from your API fetch("http://localhost:3000/api/firms") .then((res) => res.json()) .then((data) => setFirms(data)); }, []);

const viewFirmDetails = async (id) => { const res = await fetch(http://localhost:3000/api/firms/${id}); const data = await res.json(); setSelectedFirm(data); };

return ( <div className="p-6 bg-gray-50 min-h-screen"> <h1 className="text-3xl font-bold mb-6 text-center">Prop Firm Directory</h1>

{/* Firm list */}
  {!selectedFirm && (
    <div className="grid md:grid-cols-3 gap-6">
      {firms.map((firm) => (
        <div
          key={firm.id}
          className="bg-white shadow-md rounded-2xl p-4 flex flex-col items-center hover:shadow-lg transition cursor-pointer"
          onClick={() => viewFirmDetails(firm.id)}
        >
          <img
            src={firm.logo_url}
            alt={firm.name}
            className="w-24 h-24 object-contain mb-4"
          />
          <h2 className="text-xl font-semibold mb-2">{firm.name}</h2>
          <p className="text-gray-600 text-sm mb-4 text-center">
            {firm.description?.slice(0, 100)}...
          </p>
          <button className="bg-blue-600 text-white px-4 py-2 rounded-xl">
            View Details
          </button>
        </div>
      ))}
    </div>
  )}

  {/* Firm details */}
  {selectedFirm && (
    <div className="max-w-3xl mx-auto bg-white shadow-lg rounded-2xl p-6">
      <button
        onClick={() => setSelectedFirm(null)}
        className="mb-4 text-blue-600 hover:underline"
      >
        ← Back to list
      </button>
      <div className="flex items-center gap-4 mb-4">
        <img
          src={selectedFirm.logo_url}
          alt={selectedFirm.name}
          className="w-20 h-20 object-contain"
        />
        <div>
          <h2 className="text-2xl font-bold">{selectedFirm.name}</h2>
          <p className="text-gray-500">Broker: {selectedFirm.broker}</p>
          <p className="text-gray-500">Platform: {selectedFirm.platform}</p>
        </div>
      </div>

      <p className="mb-4 text-gray-700">{selectedFirm.description}</p>

      <h3 className="text-xl font-semibold mb-2">Available Accounts</h3>
      <div className="space-y-3">
        {selectedFirm.accounts?.map((acc) => (
          <div
            key={acc.id}
            className="p-4 border rounded-xl bg-gray-50"
          >
            <p><strong>Account Size:</strong> {acc.account_size}</p>
            <p><strong>Price:</strong> ${acc.price}</p>
            <p><strong>Profit Split:</strong> {acc.profit_split}</p>
            <p><strong>Profit Target:</strong> {acc.profit_target}</p>
            <p><strong>Max Drawdown:</strong> {acc.max_drawdown}</p>
            <p><strong>Daily Drawdown:</strong> {acc.daily_drawdown}</p>
            <p><strong>Scaling Plan:</strong> {acc.scaling_plan}</p>
          </div>
        ))}
      </div>

      <a
        href={selectedFirm.affiliate_link}
        target="_blank"
        rel="noopener noreferrer"
        className="mt-6 inline-block bg-green-600 text-white px-6 py-3 rounded-xl shadow hover:bg-green-700"
      >
        Sign Up with {selectedFirm.name}
      </a>
    </div>
  )}
</div>

); }

