
## Project 3: Stock Market Correlation Network

**File:** `Graph_Theory.ipynb`

This notebook applies graph theory to visualize the correlation structure of the stock market. The network provides an intuitive way to see which stocks tend to move together.

### Concepts Covered:
* **Correlation Analysis**: The Pearson correlation matrix is computed from the daily log returns of a basket of technology and consumer stocks (`TSLA`, `AMZN`, `AAPL`, etc.).
* **Graph Theory**:
    * **Nodes**: Each stock is represented as a node in the network.
    * **Edges**: An edge connects two nodes if their correlation exceeds a specified threshold (e.g., 0.4).
    * **Edge Weight**: The thickness of the edge is proportional to the correlation strength, visually highlighting stronger relationships.
* **Network Visualization**: The `networkx` and `matplotlib` libraries are used to draw the final graph, revealing clusters of highly correlated stocks.



---

## Requirements

To run these notebooks, you will need Python 3 and the following libraries:

* `numpy`
* `pandas`
* `matplotlib`
* `scipy`
* `yfinance`
* `networkx`

You can install all required libraries with a single command:
```bash
pip install numpy pandas matplotlib scipy yfinance networkx
