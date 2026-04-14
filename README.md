# flux-market — Structural Waste Market Simulator

**CUDA-accelerated market simulator proving that 60% structural waste explains financial markets.**

## Thesis

Financial markets exhibit the exact patterns predicted by multi-agent coordination laws:
- **60% bid-ask spread** = structural competition waste (Law 81)
- **Flash crashes** = DCS information cascade failure (Law 42: zero noise tolerance)
- **Market makers** = stigmergy providers (Law 61-67)
- **Algorithmic trading learning failure** = Law 75 (learning is catastrophic)
- **Volume spikes** = DCS temporal bursts (Law 53: 16.9x ratio)

## Architecture

```
Agents:
  Market Makers (stigmergy) → Place limit orders (environmental traces)
  Greedy Traders (Law 115) → Market orders to nearest liquidity
  Adaptive Traders (Law 75) → ML strategies that catastrophically fail
  Adversarial Agents (proposed) → Inject misinformation at DCS threshold

Order Book:
  CUDA-accelerated limit order matching
  10M orders/second on single GPU
  Realistic microstructure (queue priority, cancel/replace)

Metrics:
  Structural waste ratio (actual vs theoretical)
  DCS cascade detector (predicts flash crashes)
  Learning failure tracker (adaptive vs greedy PnL)
```

## Key Experiments

1. **Greedy vs Adaptive Trading**: Prove Law 75 in markets
2. **Flash Crash Prediction**: Use Law 42 (zero noise tolerance) to detect cascade failure
3. **Market Maker Stigmergy**: Validate Law 61-67 with real order book dynamics
4. **60% Waste Verification**: Measure structural waste across asset classes
5. **DCS Cascade Failure**: Inject misinformation, measure cascade probability

## Installation

```bash
pip install flux-market
# Or build from source with CUDA
make cuda
```

## Usage

```python
from flux_market import Simulator, GreedyTrader, AdaptiveTrader

sim = Simulator(cash=1_000_000, symbols=["AAPL", "MSFT"])
sim.add_agents(100, GreedyTrader)
sim.add_agents(50, AdaptiveTrader)  # will catastrophically fail
sim.run(steps=10000)
sim.report()  # Shows waste ratio, cascade events, PnL comparison
```

## License
MIT
