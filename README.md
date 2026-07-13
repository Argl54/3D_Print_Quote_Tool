# 3D Print Cost Calculator

An easy, private, single-file calculator for estimating the full cost of a 3D print from G-code.

## Use it

1. Double-click `index.html` to open it in a web browser.
2. Drop in a `.gcode` file.
3. Check the detected filament weight and print time.
4. Enter material, electricity, printer depreciation, maintenance, shop overhead, design/prep/slicing/post-processing/admin labor, packaging, shipping, marketplace fees, quantity, failure allowance, and profit markup.
5. Use **Print / Save PDF** to make a customer-friendly quote.

The G-code is read only inside the browser and is not uploaded anywhere. Settings can be saved on that device. Because slicers write G-code comments differently, always verify the detected filament weight and print time.

## Pricing model notes

The calculator now separates direct production costs from selling costs. Printer depreciation is calculated from purchase price divided by expected printer life; maintenance and overhead are hourly allowances. Quantity multiplies per-piece material, print, post-processing, packaging, and machine costs while design and admin time are counted once. Payment or marketplace fees are applied to the calculated selling price, and a minimum order charge prevents very small jobs from being underpriced.

These additions reflect common cost-based pricing guidance that recommends including machine depreciation, labor, overhead, packaging, shipping, failure risk, and platform fees - not just filament: [3D printing pricing overview](https://scienceinsights.org/how-to-price-3d-prints-materials-labor-profit/), [Etsy fee basics](https://help.etsy.com/hc/en-us/articles/360035902374-Etsy-Fee-Basics), and [manufacturing cost categories](https://en.wikipedia.org/wiki/Manufacturing_cost).
