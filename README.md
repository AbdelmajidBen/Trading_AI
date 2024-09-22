# Crypto Portfolio Manager

This project uses a combination of financial market data, optimization techniques, and AI-based analysis to manage and rebalance a cryptocurrency portfolio. It integrates with **Coinbase** to fetch real-time portfolio data and **OpenAI** to analyze and optimize the current allocation based on market conditions.

## Features

- **Portfolio Allocation:** Optimizes portfolio allocation using historical and real-time cryptocurrency market data.
- **Real-Time Market Data:** Fetches current prices, volume, and market capitalization using the **Yahoo Finance (yfinance)** API.
- **AI-Driven Market Analysis:** Leverages **OpenAI** to evaluate market conditions and suggest new portfolio allocations.
- **Portfolio Rebalancing:** Automatically executes trades to match target portfolio allocation based on AI and market data.
- **Supports Cryptocurrencies:** BTC, ETH, XRP, LTC, ADA (can be extended).

## Requirements

To install the necessary dependencies, use the following:

```bash
pip install -r requirements.txt
```

**Dependencies:**

- `yfinance==0.2.18`
- `pandas==1.5.3`
- `numpy==1.23.5`
- `scipy==1.10.1`
- `coinbase==2.1.0`
- `openai==0.27.8`

## Setup

### Coinbase API
1. Create a Coinbase account.
2. Obtain your **API_KEY** and **API_SECRET** from your Coinbase account's API section.
3. Add your **API_KEY** and **API_SECRET** in the respective variables in the script.

### OpenAI API
1. Get your OpenAI API key by creating an account at [OpenAI](https://beta.openai.com/signup/).
2. Set your OpenAI API key in the script (`openai.api_key = 'your-key-here'`).

> **Note:** You might need to deposit at least $5 in your OpenAI account to enable API access.

### Running the Program

The main script to run is:

```bash
python crypto_portfolio_manager.py
```

This will:
1. Fetch your current portfolio allocation from `trading_strategy.py`.
2. Get the latest market data for the selected cryptocurrencies.
3. Analyze the market conditions with **OpenAI** and suggest a new portfolio allocation.
4. Update your trading strategy based on the AI’s suggestions.
5. Execute trades to rebalance the portfolio to the new allocation.

### Example Output

```bash
Optimal Portfolio Allocation (with real-time adjustments):
BTC: 40.12%
ETH: 30.24%
XRP: 15.08%
LTC: 8.12%
ADA: 6.44%
```

## Trading Strategy Script

The `trading_strategy.py` script is dynamically updated based on AI recommendations. You can define custom trading logic and strategy, which the AI can then analyze and optimize.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
