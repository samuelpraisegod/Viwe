-- Table for Prop Firms
CREATE TABLE prop_firms (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    website VARCHAR(255),
    broker VARCHAR(100),
    platform VARCHAR(100), -- e.g. MT4, MT5, cTrader
    headquarters VARCHAR(100),
    founded_year INT,
    description TEXT,
    affiliate_link VARCHAR(255), -- your unique link
    logo_url VARCHAR(255),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Table for Account Types / Challenges
CREATE TABLE firm_accounts (
    id INT AUTO_INCREMENT PRIMARY KEY,
    prop_firm_id INT,
    account_size VARCHAR(50), -- e.g. $10k, $50k, $100k
    price DECIMAL(10,2),      -- challenge fee
    profit_split VARCHAR(20), -- e.g. 80/20
    profit_target VARCHAR(50), -- e.g. 10%
    max_drawdown VARCHAR(50), -- e.g. 12%
    daily_drawdown VARCHAR(50), -- e.g. 5%
    scaling_plan VARCHAR(100), -- e.g. "up to $2M"
    FOREIGN KEY (prop_firm_id) REFERENCES prop_firms(id)
);

-- Table for Reviews & Ratings
CREATE TABLE firm_reviews (
    id INT AUTO_INCREMENT PRIMARY KEY,
    prop_firm_id INT,
    user_name VARCHAR(100),
    rating INT,               -- 1-5 stars
    review TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (prop_firm_id) REFERENCES prop_firms(id)
);
