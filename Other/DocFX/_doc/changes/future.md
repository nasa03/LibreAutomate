## Version 1..0 (2024-)

### Editor
More features in code snippets:
- Snippet code can contain multiple fields that can be selected with `Tab` or `Enter`. When leaving an edited field, updates text of related fields.
- Formats the inserted snippet code.
- The **Snippets** tool can import Visual Studio and VSCode snippets.
- Surround with snippet (menu **Edit > Selection > Surround** or toolbar button).
- Snippet context detected automatically.
- A snippet can add `/*/ meta comments /*/`.

Formats code when completing current statement (adding `;`, `{  }` etc). This feature can be disabled in **Options**.

Adds `;` when starting a statement. Later deletes if don't need. This feature can be disabled in **Options**.

You can use `Backspace` to exit current multiline `{ block }` when the text cursor is in the last line of the block and that line is blank. Previously `Ctrl+Enter` worked in a similar way.

Changes in code editor feature "statement completion on `Enter` before `)` or `]`":
- Can be disabled: **Options > Code editor > Statement completion > Enter before )**.
- Removed: `Esc` key prevents it.
- Added: space before prevents it. Other ways: comma before; `Shift+Enter`.
- After statement completion, next **Undo** command undoes the change and adds new line without statement completion.
- Related: Now the "complete statement anywhere" hotkey (`Ctrl+Enter` etc) can be set in **Options**.

If there is selected text and you type `(`, `[` or `{`, surrounds that text like `(selected)` or `{ selected }`.

Drag and drop a non-script file from the **Files** panel to the code editor: can add `/*/ meta comments /*/`.

Several small improvements. Removed some low-value features.

Fixed bugs:
- Debugger settings: does not work **not**.
- And more.

### Library
New classes:
- .

New members:
- **wnd.IsMatch** overload for multiple windows.
- **string.Split**, **ReadOnlySpan\<char\>.Split** and **ReadOnlySpan\<char\>.SplitAny** overloads that return **StartEnd[]**.
- **ReadOnlySpan\<char\>.Split** and **ReadOnlySpan\<char\>.SplitAny** overloads that return **string[]**.

New parameters:
- **string.Lines**: *preferMore* (include the last empty line), *rareNewlines*.
- **string.LineCount**: *rareNewlines*.

Improved:
- .

Fixed bugs:
- When used in a single-file app or portable LA, **folders.NetRuntimeDesktopBS** returns `null`, and **folders.NetRuntimeDesktop** throws exception.

### Breaking changes
