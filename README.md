<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DivoraSplit Dashboard - Home</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <div id="hamburger">☰</div>
        <h2>DivoraSplit Dashboard</h2>
        <div class="auth-buttons">
            <a href="signup.html" class="auth-btn">Sign Up</a>
            <a href="login.html" class="auth-btn">Log In</a>
        </div>
    </header>
    <nav id="navigation-menu">
        <ul>
            <li><a href="index.html" data-emoji="🏠">Home</a></li>
            <li><a href="profile.html" data-emoji="👤">Profile</a>
                <ul class="sub-menu">
                    <li><a href="view-profile.html">View Profile</a></li>
                    <li><a href="edit-profile.html">Edit Profile</a></li>
                    <li><a href="settings.html">Settings</a></li>
                    <li><a href="logout.html">Logout</a></li>
                </ul>
            </li>
            <li><a href="balance.html" data-emoji="🏦">Balance</a>
                <ul class="sub-menu">
                    <li><a href="wallet-overview.html">Wallet Overview</a></li>
                    <li><a href="transaction-history.html">Transaction History</a></li>
                </ul>
            </li>
            <li><a href="deposit.html" data-emoji="➕">Deposit</a>
                <ul class="sub-menu">
                    <li><a href="bank-transfer.html">Bank Transfer</a></li>
                    <li><a href="crypto-wallet.html">Crypto Wallet</a></li>
                </ul>
            </li>
            <li><a href="withdrawals.html" data-emoji="💵">Withdrawals</a>
                <ul class="sub-menu">
                    <li><a href="bank-withdrawal.html">Bank Withdrawal</a></li>
                    <li><a href="crypto-withdrawal.html">Crypto Withdrawal</a></li>
                </ul>
            </li>
            <li><a href="firms.html" data-emoji="🏦">Firms</a>
                <ul class="sub-menu">
                    <li><a href="popular-firms.html">Popular</a></li>
                    <li><a href="favorite-firms.html">Favourite (0/5)</a></li>
                    <li><a href="new-firms.html">New Added</a></li>
                    <li><a href="all-firms.html">All</a></li>
                </ul>
            </li>
            <li><a href="challenges.html" data-emoji="🎯">Challenges</a>
                <ul class="sub-menu">
                    <li><a href="fx-challenges.html">Assets FX</a></li>
                    <li><a href="account-size.html">Size Account</a></li>
                    <li><a href="steps-challenges.html">Steps</a></li>
                    <li><a href="discount-challenges.html">Apply Discount</a></li>
                    <li><a href="bookmarks-challenges.html">Bookmarks</a></li>
                </ul>
            </li>
            <li><a href="offers.html" data-emoji="🎁">Offers</a>
                <ul class="sub-menu">
                    <li><a href="september-offers.html">September Offers</a></li>
                    <li><a href="exclusive-offers.html">Exclusive Offers</a></li>
                    <li><a href="all-offers.html">All Current Offers</a></li>
                </ul>
            </li>
            <li><a href="reviews.html" data-emoji="⭐">Review</a>
                <ul class="sub-menu">
                    <li><a href="all-reviews.html">All Reviews</a></li>
                    <li><a href="funded-reviews.html">Funded Reviews</a></li>
                    <li><a href="paidout-reviews.html">Paid Out Reviews</a></li>
                </ul>
            </li>
            <li><a href="cofunding.html" data-emoji="🤝">Co-Funding</a>
                <ul class="sub-menu">
                    <li><a href="create-cofunding.html">Create Co-Funding Request</a></li>
                    <li><a href="cofunding.html?state=pending">Pending</a></li>
                    <li><a href="cofunding.html?state=active">Active</a></li>
                    <li><a href="cofunding.html?state=accepted">Accepted</a></li>
                    <li><a href="cofunding.html?state=canceled">Canceled</a></li>
                </ul>
            </li>
        </ul>
    </nav>
    <div id="main-content">
        <h1>Welcome to DivoraSplit</h1>
        <p>Current Date and Time: <span id="date-time">01:42 PM WAT, Wednesday, September 10, 2025</span></p>
        <div class="settings-section">
            <h2>Getting Started</h2>
            <p>New here? Click <a href="signup.html">Sign Up</a> to unlock limitless trading opportunities. Already a member? Explore <a href="challenges.html">Challenges</a>, <a href="firms.html">Firms</a>, or <a href="cofunding.html">Co-Funding</a> to begin.</p>
        </div>
    </div>
    <script src="script.js"></script>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            function updateDateTime() {
                const now = new Date();
                const options = { hour: '2-digit', minute: '2-digit', hour12: true, weekday: 'long', year: 'numeric', month: 'long', day: 'numeric', timeZone: 'Africa/Lagos' };
                document.getElementById('date-time').textContent = now.toLocaleString('en-US', options) + ' WAT';
            }
            updateDateTime();
            setInterval(updateDateTime, 60000);

            function isLoggedIn() {
                return localStorage.getItem('isLoggedIn') === 'true';
            }

            function redirectToLogin(url) {
                const targetUrl = url || window.location.href;
                localStorage.setItem('redirectAfterLogin', targetUrl);
                window.location.href = 'login.html';
            }

            document.querySelectorAll('#navigation-menu a').forEach(link => {
                link.addEventListener('click', (e) => {
                    const href = link.getAttribute('href');
                    const protectedPages = ['profile.html', 'balance.html', 'deposit.html', 'withdrawals.html', 
                                           'firms.html', 'challenges.html', 'offers.html', 'reviews.html', 'cofunding.html',
                                           'view-profile.html', 'edit-profile.html', 'settings.html', 'wallet-overview.html',
                                           'transaction-history.html', 'bank-transfer.html', 'crypto-wallet.html',
                                           'bank-withdrawal.html', 'crypto-withdrawal.html', 'popular-firms.html',
                                           'favorite-firms.html', 'new-firms.html', 'all-firms.html', 'fx-challenges.html',
                                           'account-size.html', 'steps-challenges.html', 'discount-challenges.html',
                                           'bookmarks-challenges.html', 'september-offers.html', 'exclusive-offers.html',
                                           'all-offers.html', 'all-reviews.html', 'funded-reviews.html', 'paidout-reviews.html',
                                           'create-cofunding.html'];

                    if (protectedPages.includes(href) && !isLoggedIn()) {
                        e.preventDefault();
                        redirectToLogin(href);
                    } else if (href === 'logout.html' && isLoggedIn()) {
                        e.preventDefault();
                        if (confirm('Are you sure you want to log out?')) {
                            localStorage.removeItem('isLoggedIn');
                            localStorage.removeItem('redirectAfterLogin');
                            alert('You have been signed out successfully.');
                            window.location.href = 'index.html';
                        }
                    }
                });
            });
        });
    </script>
</body>
</html>
