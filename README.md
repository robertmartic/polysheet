# PolySheet

Version 0.1.2. A local spreadsheet workspace for Windows x64, with an English interface and light/dark themes. Free and unlocked; no account or document upload.

Run PolySheet.exe from the portable folder, or use PolySheet-0.1.2-setup.exe.

Create one-sheet workbooks in .polys format. Edit directly (double-click, F2 or type) or through the formula bar; press Enter to apply, Escape to cancel. Shift+arrows or drag selects a range. Resize columns/rows by dragging header boundaries. Use Home for clipboard and basic formatting. Save stores the full workbook; CSV export is a separate operation.

Supported: + - * /, parentheses, SUM, AVERAGE, MIN, MAX, COUNT; A1 and mixed/absolute references; rectangular ranges. English function names. A workbook retains its number/formula culture. Decimal comma uses semicolon function arguments; decimal point uses comma arguments. No IF, dates as numeric values, cross-sheet references, external sources, macros or XLSX in this release.

Numbers use binary floating point. Display rounding does not change stored values. Errors remain visible; unsupported formulas never silently become zero. Aggregations ignore nonnumeric values; errors propagate. Empty SUM/MIN/MAX/COUNT return 0; empty AVERAGE returns #DIV/0!. Arithmetic treats blank references as 0 and rejects text and booleans. Use an initial apostrophe to enter literal text such as '00123 or '=SUM(A1:A2).

Copy adjusts relative references. Cut/paste moves cells and updates references, including absolute references. A move that would split a referenced range is rejected; copy instead. Further document edits cancel a pending cut. Lossless clipboard behavior is within the same window; other apps/windows receive displayed tabular values. External pasted text never executes formulas. Empty pasted fields clear destination content. Undo/Redo restores a whole edit or paste.

CSV import defaults to text, preserving leading zeros. Optional numeric conversion can remove leading zeros. UTF-8 and Windows-1250, comma/semicolon/tab separators, escaped quotes and multiline fields are supported. CSV export writes computed values using the workbook culture and UTF-8 BOM; formulas, formatting, dimensions and type metadata are lost. Safe text prefixing is enabled by default and may add an apostrophe when read elsewhere.

Limits: 10,000 rows, 100 columns, 100,000 populated/formatted cells; 64 MB native file/CSV input, 32,767 characters per cell. Formulas: 8,192 characters, 256 expression atoms, nesting depth 64, bounded total calculation work. Exceeding the calculation budget shows #LIMIT!. Very large selections and files may take longer. Undo history is bounded. Dates remain text. No printing in 0.1.2.

Shortcuts: Ctrl+N/O/S, Ctrl+Shift+S, Ctrl+Z/Y, Ctrl+C/X/V, Ctrl+B/I, F2, Delete, arrows, Shift+arrows, Tab, Enter, Home, Page Up/Down.

Recovery checkpoints every 15 seconds include pending cell input. Copies are encrypted for the current Windows user and offered as new unsaved workbooks after interruption. Recovery is best effort and does not replace saving.

See docs/INSTALLATION.md and docs/UPDATES.md. Included licenses and notices remain applicable. Download the latest release at https://github.com/robertmartic/polysheet/releases/latest.
