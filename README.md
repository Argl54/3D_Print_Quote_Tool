# 3D Print Quote Tool

A private, browser-only calculator for estimating the full cost of one or more 3D prints from G-code and producing a customer-ready quote.

## Features

- Upload one or more G-code files at once.
- Set the run quantity independently for each uploaded G-code file.
- Detect filament usage and printer time from common slicer comments.
- Include material, electricity, depreciation, maintenance, overhead, labor, packaging, shipping, fees, failure allowance, and profit.
- Enter a customer or project name and optional order description.
- Print or save a clean customer quote without exposing internal costs or profit.

## Use it

1. Double-click `3D print calculator.html` to open it in a web browser.
2. Drop in one or more `.gcode` files, or select several files at once.
3. Check the per-file details and combined filament weight and print time.
4. Enter a customer or project name for the quote, then use the **Runs** control beside each uploaded file to set how many times that specific G-code file should run.
5. Enter material, electricity, printer depreciation, maintenance, shop overhead, design/prep/slicing/post-processing/admin labor, packaging, shipping, marketplace fees, failure allowance, and profit markup.
6. Use **Print / Save PDF** in the suggested customer price box to open the clean customer quote in the print dialog. The PDF shows the customer/project name, date, order description, total print runs, print time, working time, and final price. Internal rates, costs, and profit are excluded.

The quote updates automatically when you upload files, change runs, or edit costs and time. An optional order description replaces the automatic supplied-file summary. Print quantity counts runs, not individual pieces on a build plate. Working time includes design, preparation, slicing, post-processing for each run, and admin time; enter these times yourself because G-code cannot determine them. Printer time is shown separately. Clearing files resets the uploaded weight and print time. For a clean PDF, turn off browser headers and footers in the print dialog.

## Privacy

G-code is read only inside the browser and is not uploaded anywhere. The calculator has no server, analytics, or external script dependency. Saved settings remain in the browser's local storage on the device where they were saved. Do not enter sensitive personal information into customer or project fields unless you are comfortable storing it locally in that browser.

Multiple files are combined into one project quote; adding more files later appends them to the current batch, and duplicate selections are ignored. Each uploaded file has its own run quantity, so repeating one file does not repeat the other files. Because slicers write G-code comments differently, always verify the detected filament weight and print time for every file.

## Pricing model notes

The calculator separates direct production costs from selling costs. Printer depreciation is calculated from purchase price divided by expected printer life; maintenance and overhead are hourly allowances. Each file's run quantity multiplies its material, print time, post-processing, packaging, and machine costs while design and admin time are counted once. Payment or marketplace fees are applied to the calculated selling price, and a minimum order charge prevents very small jobs from being underpriced.

These additions reflect common cost-based pricing guidance that recommends including machine depreciation, labor, overhead, packaging, shipping, failure risk, and platform fees—not just filament: [3D printing pricing overview](https://scienceinsights.org/how-to-price-3d-prints-materials-labor-profit/), [Etsy fee basics](https://help.etsy.com/hc/en-us/articles/360035902374-Etsy-Fee-Basics), and [manufacturing cost categories](https://en.wikipedia.org/wiki/Manufacturing_cost).

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for the full text.
