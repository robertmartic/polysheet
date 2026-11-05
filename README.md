# PolySheet

Version 0.3.1. A local spreadsheet workspace for Windows x64 with an English interface and light/dark themes. Free and unlocked; no account or document upload.

Run PolySheet.exe from the portable folder or use PolySheet-0.3.1-setup.exe. Download [Windows setup](https://downloads.polystudio.tools/polysheet/0.3.1/PolySheet-0.3.1-setup.exe) or the [portable ZIP](https://downloads.polystudio.tools/polysheet/0.3.1/PolySheet-0.3.1-win-x64.zip) from PolyStudio. The one-time 0.2.2 bridge is also available at https://github.com/robertmartic/polysheet/releases/tag/v0.2.2 for older installations.

Create workbooks in .polys format. Use the worksheet selector and Sheets… to add, rename, duplicate, reorder or delete sheets. Sheet changes participate in workbook-wide Undo/Redo. Renaming adjusts qualified references; deleting a sheet turns its references into #REF!. At least one sheet must remain.

Edit directly (double-click, F2 or type), or use the formula bar; Enter applies input and Escape cancels it. Shift+arrows or dragging selects a range. Resize rows/columns at header dividers. View > Auto fit sizes selected columns from displayed results; double-click a column divider for one column.

The Home toolbar groups Search, Clipboard, Font / Format, Alignment, Data, Structure and Fill. More opens whole groups that do not fit. Tab/Shift+Tab and left/right arrows navigate tools; Escape returns to the worksheet. Tooltips show names and available shortcuts. Formatting controls reflect the full selection, including mixed states.

Supported formulas: + - * /, parentheses, comparisons (= <> < > <= >=), SUM, AVERAGE, MIN, MAX, COUNT, ROUND, IF, AND, OR, COUNTIF, SUMIF, AVERAGEIF and IFERROR. TRUE/FALSE and quoted text are supported. References include A1, mixed/absolute references, rectangular ranges and references such as =Sheet2!A1 or ='Sales 2026'!$B$2. English function names are required. A workbook retains its input culture: decimal comma uses semicolon arguments; decimal point uses comma arguments.

Numbers use binary floating point. ROUND uses midpoint rounding away from zero; display rounding does not change stored values. IF evaluates only its selected branch. Errors remain visible; unsupported formulas never silently become zero. Aggregations consider numeric values and ignore text/booleans; errors propagate. Arithmetic treats blanks as zero and booleans as 0/1, and rejects text. Date and ISO Date formats store calendar dates explicitly. Start literal text with an apostrophe to preserve leading zeros or formula-like content.

Fill Down (Ctrl+D) copies the first selected row through the range; Fill Right (Ctrl+R) copies the first selected column. Drag the small selection corner down or right to repeat the source pattern. Formula offsets respect $ markers. Each fill is one Undo operation.

Structure inserts whole rows above or columns before the selected range; selection height/width determines the count. Deletion removes those whole rows/columns. Cells, formatting and custom dimensions move together, and references in every sheet adjust. Ranges expand or shrink as appropriate; fully removed/out-of-grid references become #REF!. Insertion that would discard stored edge data, formatting or custom dimensions is rejected.

Copy adjusts relative references. Cut/paste in the same sheet moves cells and updates references in every worksheet. Moves that split a referenced range are rejected. Editing, Undo/Redo or switching worksheets cancels a pending cut; switching leaves its snapshot available as a copy. Internal copies may be pasted between sheets. Other windows/apps receive displayed values. External plain-text paste retains destination formatting and does not execute formulas. Empty pasted fields clear content.

Find/Replace searches stored input and formula source in the active worksheet, with Match case and Match entire cell. Ctrl+F / Ctrl+H opens it; Replace all is one Undo operation. Ctrl+G focuses the cell address field.

CSV import defaults to literal text, preserving leading zeros. Optional numeric conversion can remove leading zeros. UTF-8/Windows-1250 and comma/semicolon/tab separators are supported. CSV export writes only the active sheet's computed values, using the workbook culture and UTF-8 BOM. Formulas, styles, other sheets and dimensions are not included. Safe text prefixing is enabled by default.

XLSX import opens a new unsaved workbook and preserves the original file. XLSX export writes a separate copy captured when export starts; save .polys independently. Basic values, supported formula source, bold/italic, left/center/right alignment, General/two-decimal Number/Percentage, dimensions and up to 32 worksheets are supported. Excel shared strings and ordinary shared formulas are recognized. Imported XLSX formulas use decimal-point/comma-argument input culture. Whole calendar dates, frozen panes, one simple filter and supported validation rules can be exchanged. Time and date-time values remain text where possible.

XLSX compatibility is limited. Macros, linked workbook data, charts, pivots, merges, complex filters and validation, print settings, conditional formatting and other advanced content are not preserved. Rich text and unsupported formats are simplified. Unsupported formula source is retained but may display an error; Excel recalculates exported formulas. Compatibility notices appear before import/export. Keep the original XLSX and use native .polys for ongoing work. Encrypted workbooks and strict-namespace XLSX are unsupported.

Limits: 32 sheets, 10,000 rows × 100 columns (A–CV) per sheet, 100,000 populated/formatted cells across the workbook, 64 MB native/CSV/XLSX input and 32,767 input characters per cell. XLSX expanded package limit: 128 MB total, 64 MB per part and 4,096 entries. Oversized/out-of-grid content is rejected rather than silently truncated. Formulas have an 8,192-character limit, 256 expression atoms, depth 64 and a shared calculation budget. Exceeding the budget displays #LIMIT!. Undo history is bounded. Printing, charts and pivot tables are outside this release.

Native single-sheet v1 files remain readable. Native v1 and v2 workbooks remain readable. Workbooks with new sheet options or typed dates use v3, which requires 0.3.0 or later. Recovery checkpoints every 15 seconds include all worksheets and pending input, encrypted for the current Windows user. Recovery is best effort and does not replace saving. External changes to an opened .polys file are protected; use Save as to preserve both versions.

Shortcuts include Ctrl+N/O/S, Ctrl+Shift+S, Ctrl+Z/Y, Ctrl+C/X/V, Ctrl+B/I, Ctrl+D/R, Ctrl+F/H/G, F2, Delete, arrows, Shift+arrows, Tab, Enter, Home and Page Up/Down.

See docs/INSTALLATION.md and docs/UPDATES.md. Included licenses and notices remain applicable.
Built-in Help: choose Help in the header or press F1. Browse nine categories or search tool names, shortcuts and instructions across all topics. Select a result to read steps and examples inside the app. Common Croatian search aliases are supported while instructions remain English. Ctrl+F focuses Help search, Down enters results, and Escape closes Help. Content is bundled and available offline; Help preserves pending input and does not modify the workbook.

Updates use digitally signed PolyStudio metadata and verified official download URLs. Automatic checks run at most once every 24–30 hours; use About > Updates to check immediately.

Click a column letter or row number to select the entire axis. Header dividers still resize. The Data tab has Sort, Filter and Data validation. Sort moves all cells inside the selected rectangle, with stable ties and relative formulas shifted with moved rows. References in other cells keep their addresses. Filters hide rows below the range header and show the visible count. Formulas and rectangular operations include hidden rows.

Select B2 and use View > Freeze panes to keep row 1 and column A visible. Choose Date or ISO Date to convert calendar inputs. Enter YYYY-MM-DD or a full date in the workbook locale. Rules support inline lists, numeric bounds and whole-date bounds. List cells offer an Allowed values menu. Empty input is allowed. Rule ranges accept literals and reject formulas.

XLSX interoperability covers a supported subset: one value/contains/numeric filter per sheet, normal frozen panes, whole dates from 1900 onward and simple inline-list or between rules. Complex criteria, formula-driven rules, multi-range rules, time arithmetic and lists exceeding Excel inline-list limits are reported when omitted or simplified.
