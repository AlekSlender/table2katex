Hi everyone!

As you know, Dynalist doesn't natively support tables, which can be a bit tricky when we need to organize structured data in our documents. While Markdown blocks or inline formatting work for simple lists, displaying clean grids usually requires workarounds.

To solve this for my own workflow, I built a small, standalone HTML utility called table2katex. I’m sharing it here with the community in case anyone else finds it useful. It runs entirely locally in your browser, with no external dependencies or server-side tracking.



🌟 Key Features & Customization

Multiple Source Formats: You can paste raw HTML (<table>), LaTeX (\begin{tabular}), or tabular data copied directly from spreadsheets like Excel or Google Sheets (TSV / tab-separated). It also includes an Auto-detect mode.

Granular Border Control: Choose between full borders, horizontal-only lines, vertical-only lines, or no borders at all.

Visual Grid Options: Toggle inner grid lines between every row or make headers bold automatically.

Typography & Sizing: Select between Serif and Sans-serif fonts, and adjust the table font size (\small, \footnotesize, \scriptsize) to fit neatly inside your Dynalist nodes.

Multi-language Interface: Fully translated into English, Spanish, French, German, Russian, and Chinese.

One-Click Clipboard Integration: Automatically copies the generated KaTeX string to your clipboard upon conversion so you can paste it directly into Dynalist.

⚠️ Limitations & Known Constraints

While KaTeX is powerful, it has strict layout boundaries compared to a full browser rendering engine. Please keep the following in mind:



Not Directly Editable: Once inserted into Dynalist, the table is rendered as a math block, meaning its cells are not interactive or editable on the fly. If you need to change a data point later, you have to locate it within the raw KaTeX source code inside the node. For small tables this is quick and easy, but it can become tedious for large datasets.

No Advanced HTML Styling: Complex cell backgrounds, custom padding, cell merging (beyond basic column spans), or rich colors inside the source table cannot be translated into KaTeX natively. Text formatting inside cells is largely stripped down to plain text.

KaTeX Macro Limitations: KaTeX uses LaTeX array syntax (\begin{array}{c|c|c}). Highly specialized LaTeX table packages (like booktabs rules or multirow) are automatically stripped or simplified during parsing to prevent rendering crashes.

Horizontal Scrolling: Very wide tables with many columns will stretch your Dynalist layout, requiring horizontal scrolling depending on your screen size or view mode.

Local Execution: It is a single .html file. You can simply download it, double-click it to open it in any modern browser, and use it completely offline.

📥 How to use it

Download or copy the code below (save it as table2katex.html on your computer).

Open it in your web browser.

Paste your table on the left panel, tweak your preferred formatting options, and click Convert.

Paste the resulting block ($$...$$) directly into any Dynalist bullet point!
