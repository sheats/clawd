# Hummingbot Strategies V2

**Source:** https://hummingbot.org/strategies/
**Saved:** 2025-01-25

## What is a Hummingbot Strategy?

Like a computer program, an algorithmic trading strategy is a set of automated processes that executes repeatedly:

- **Data Collection:** Gathering real-time data from various sources
- **Data Processing:** Analyzing data to identify patterns and make decisions
- **Order Execution:** Placing and cancelling orders based on processed data

A Hummingbot strategy loads market data directly from centralized and decentralized exchanges, adaptable to the unique features of each trading venue's WebSocket/REST APIs and nodes.

Each clock tick, a strategy loads real-time order book snapshots, user balances, order status and other real-time data from trading pairs on these venues and executes the logic defined in the strategy, parametrized by a pre-defined user configuration.

## V2 Framework (Recommended)

Starting in 2023, Hummingbot Foundation introduced the V2 Framework. It allows you to build powerful, dynamic strategies using Lego-like components.

### Two Ways to Define Strategies:

**Scripts:** A simple Python file that contains all strategy logic. Good for prototyping.

**Controllers:** Strategy logic is abstracted into a Controller, which may use Executors and other components for greater modularization. Controllers can be backtested and deployed using Dashboard, and a single loader Script may deploy and manage multiple Controller configurations.

### When to Use Script vs Controller:

| Script | Controller |
|--------|------------|
| Strategy is relatively simple | Want to manage risk and diversify portfolio in different controllers |
| Logic is very standard across different trading pairs | Strategy is complex and you want to isolate decision making |
| Strategy only trades on one trading pair | Want to try multiple configs in the same bot |
| Getting started with Executors | Strategy trades on multiple trading pairs |
| Prototyping a strategy | Familiar with Strategy V2 and how controllers interact |

## V1 Framework (Legacy)

When it launched in 2019, Hummingbot pioneered the concept of configurable templates for algo trading strategies, such as market making strategies based on the Avellaneda & Stoikov paper.

These V1 strategies are still supported but new development focuses on V2.

## Learning Resources

- **Botcamp:** https://www.botcamp.xyz - official training and certification for Hummingbot
- Teaches you how to design and deploy advanced algo trading and market making strategies using the V2 framework
