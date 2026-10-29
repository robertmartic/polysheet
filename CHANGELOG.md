# Changelog

## 0.2.2

- Updates now use PolyStudio's digitally signed update channel and verified official download server.
- Automatic checks run at most once every 24–30 hours; manual checks remain available immediately.
- Update downloads reject redirects, invalid signatures and unexpected application or package information.
- This bridge release lets existing installations move to the new update service while preserving workbooks, settings and installation choices.

## 0.2.1
- Open built-in offline Help from the header or with F1, without changing pending workbook input.
- Browse 55 practical help topics grouped into nine categories, including tools, formulas, worksheet management, import/export and updates.
- Search across tool names, shortcuts and instructions, including common Croatian search aliases. Direct tool matches appear before incidental text matches.
- Read steps and formula examples directly inside the app, with keyboard navigation and light/dark support.

## 0.2.0
- Work with multiple worksheets: add, rename, duplicate, reorder and delete sheets. Native saves, recovery and Undo/Redo preserve the whole workbook.
- Use references between sheets, including quoted names. Renaming, deletion and structural edits adjust references; circular dependencies remain visible.
- Fill Down (Ctrl+D), Fill Right (Ctrl+R) and drag the selection handle downward or right to extend formulas with mixed and absolute references.
- Added ROUND, IF, AND, OR, comparisons, boolean constants and quoted formula text.
- Import and export basic XLSX workbooks with values, supported formulas, basic formatting, dimensions and worksheets. Import opens a new unsaved native workbook; export writes a separate copy.
- Clear compatibility notices describe unsupported Excel features. Original XLSX files remain available; external workbook content and macros are never executed.
- Keep More accessible at narrow toolbar widths and retain readable tooltips in both themes.

## 0.1.6
- Insert and delete rows or columns from the new Structure group, using the selected range to choose the affected rows or columns.
- Formula references and ranges adjust with structural changes, including absolute references. Fully deleted references show #REF!.
- Cell formatting and custom dimensions move with the affected cells. Undo/Redo restores the entire structural operation.
- Insertions that would push existing content, formatting or custom dimensions outside the supported grid are rejected without partial changes.
- Tooltips now use matching light/dark surfaces and readable text, fixing low-contrast labels in the dark theme.

## 0.1.5
- Compact local vector tools, grouped for Search, Clipboard, Font / Format, Alignment and Data.
- Bold, Italic and alignment reflect the full selected range, including mixed formatting.
- Consistent tooltips, accessible control names and visible keyboard focus in both themes.
- More opens tools that do not fit the available toolbar width; commands preserve the worksheet selection.

## 0.1.4
- Find and replace cell input and formula source, with case-sensitive and entire-cell options. Replace all can be undone in one step.
- Auto fit selected columns from displayed values, or double-click a column divider.
- Use Ctrl+F to find, Ctrl+H to replace and Ctrl+G to go to a cell.
- Highlight selected row and column headers and show selection dimensions.

## 0.1.3
- Preserve pending cell and formula-bar input when changing selection or resizing columns and rows.
- Cancel pending cuts on Undo/Redo and preserve cell formatting when pasting plain tabular text.
- Retry temporary clipboard contention and show a clear message when it remains busy.
- Detect files changed or removed outside PolySheet and direct saving to Save as to protect both copies.
- Preserve pending input in recovery copies and retain unreadable recovery files for inspection.
- Added optional PolyHUB integration for coordinated updates while preserving application save prompts.
- Coordinate setup, uninstall and update locking.

## 0.1.2
- Added Overview, Changelog and Updates tabs to About, matching the other Poly apps.
- Show an Update available action in the header when a newer release is found.
- Made update checks, last-update details and storage management easier to find.

## 0.1.1
- Updated the PolySheet logo and Windows application, document and installer icons.

## 0.1.0
- Create and safely save local .polys workbooks with one worksheet.
- Edit cells and ranges, copy and move data, undo and redo changes.
- Calculate basic arithmetic and SUM, AVERAGE, MIN, MAX and COUNT with relative and absolute references.
- Import and export CSV with explicit settings and text preservation.
- Format numbers and text, resize rows and columns, and choose light or dark appearance.
- Recover unsaved work after an interrupted session.
- Install for your Windows account and check for application updates.
