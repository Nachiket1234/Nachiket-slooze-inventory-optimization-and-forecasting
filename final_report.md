Slooze Inventory, Sales & Purchase Analysis
Demand Forecasting and Inventory Optimization
Overview
Analysis of 2016 wine & spirits retail data (~1M sales, ~2.4M purchases) reveals strong concentration (top products/vendors), pronounced weekend seasonality, reliable supply chain (avg 7.6-day lead time), and sharp post-holiday demand collapse (Jan high → Feb low).
Key Insights

Sales Concentration: Top 10 products (mostly premium vodka/rum/whiskey) drive ~30–40% of revenue. Top 5 vendors (Diageo, Martignetti, Jim Beam, Pernod Ricard, Bacardi) account for >70% of purchase value.
ABC Classification: 1,502 A-items (19.6% of products) generate 80% of sales value → prioritize tight control here.
Seasonality: Friday/Saturday peak ~50–100% higher than weekdays → stock extra heading into weekends.
Demand Regime Shift: January boom (~2.2M units, $30M) → February collapse (~256k units, $3.3M) → post-holiday slowdown + incomplete data.
Forecasting (Advanced Models): Transformer outperformed (RMSE ~5,278 units) → stable low-demand forecast (~25–30k units/day post-Feb). LSTM+Attention best captured residual weekly waves.
Supply Chain Efficiency: Lead times 6–9 days (reliable). Payment terms ~35 days consistent. Freight <1% overall, but outliers exist.
Vendor Performance: Diageo dominant + reliable (7.5 days lead). Martignetti high volume but slightly slower (7.8 days). ULTRA BEVERAGE high volume but slowest lead (8.4 days).

Recommendations

Inventory Policy (A-Class Focus)
Reorder when stock hits ROP (~daily demand × 7.6 + safety buffer).
Order in EOQ batches to minimize costs.
Maintain ~5,300 units daily safety stock (company-wide) + 20–30% weekend boost on Fri/Sat.

Demand Planning
Use Transformer forecast as base (~25–30k units/day ongoing).
Manually boost for weekends (historical + Attention model pattern).
Recalculate monthly with new data to capture seasonality.

Supplier Optimization
Prioritize: Diageo, Jim Beam, Brown-Forman, Moet Hennessy (high volume + low lead time).
Negotiate: Martignetti, Ultra Beverage, M S Walker (high volume but slower lead/payment).
Monitor: High freight % vendors (e.g., Laird & Co, Zorvino) for cost savings.

Process Improvements
Reduce C-class inventory to free capital (currently overstocked).
Automate ROP/EOQ alerts for A-items.
Track per-store demand variation for localized stocking.


Overall Impact
Implementation could reduce stockouts/overstock, cut holding costs 15–25%, and improve cash flow via targeted supplier negotiations → higher profitability and customer satisfaction.